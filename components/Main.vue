<template>
    <div class="container">
        <div id="slogan" class="slogan" @mouseover="scramble()" data-val="no more boring cubes.">no more boring cubes.</div>
        <div class="sub">spice up your desk!</div>
    </div>
</template>


<style src="~/styles/main.css">
</style>

<script>
export default {
    methods:{
        scramble(){
            let e = document.getElementById("slogan");
            const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".toLowerCase().split("");
            let originalText = e.dataset.val.split("");
            let iterations = 0;

            let ival = setInterval(() => {
                e.innerHTML = e.innerHTML.split("")
                .map((l,i) => {
                    if (i < iterations) {
                        return originalText[i];
                    }

                    return letters[Math.floor(Math.random() * letters.length)]
                })
                .join("");

                if (iterations >= originalText.length) clearInterval(ival);

                iterations++;
            }, 40);

            // let i = 0;
            //     setInterval(() => {
            //         e.innerHTML = e.innerHTML.split("")
            //         .map(l => l = originalText[i])
            //         .join("");
            //         i++;
            //     }, 30);

        }
    }
}
</script>