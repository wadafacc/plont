<template>
    <div class="header-container" id="navbar" @mouseover="showbg()" @mouseleave="hidebg()">
        <div class="logo">𓋼</div>
        <div class="nav">
            <!-- TODO: Design logo-->
            <a href="/products">products</a>
            <a href="/about">about</a>
        </div>
        <div id="bg"></div>
    </div>
</template>

<style src="~/styles/header.css"></style>

<script>
export default {
    methods:{
        showbg() {
            let bg = document.getElementById("bg");
            bg.style.height = "100%";
        },
        hidebg() {
            let bg = document.getElementById("bg");
            bg.style.height = "0%";
        }
    }
}
</script>