<template>
    <header>
        <section class="header-mobile">
            <div class="header-container">
            <p id="p-text1">João Pedro Soares Torres</p>
            <p id="p-text2">Desenvolvedor Front-End e UX/UI Designer</p>
        </div>
        <nav>
            <div class="menu">
                <img id="menu-icon" @click="toggleMenu" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI2NCIgaGVpZ2h0PSI2NCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBmaWxsPSIjMDAwIiBkPSJNMyAxOHYtMmgxOHYyem0wLTV2LTJoMTh2MnptMC01VjZoMTh2MnoiLz48L3N2Zz4=" alt="">
            </div>
        </nav> 
        </section>
        <section id="menu">
            <ul id="menu" :class="{ show: isMenuVisible }"> 
                <li><a href="#">SOBRE MIM</a></li>
                <li><a href="#">EXPERIÊNCIA</a></li> 
                <li><a href="#">CERTIFICADOS</a></li>
                <li><a href="#">PROJETOS</a></li>
                <li><a href="#">CONTATO </a></li>
            </ul>
        </section>
    </header>
</template>

<style scoped>
 .header-mobile{
    padding: 30px;
    justify-content: space-between;
    display: flex;
    width: 100vw;
    height: 100px;
 }
 #menu{
    width: 60px;
 }

 #p-text1{
    font-weight: 300;
    font-size: 20px;
 }
 #p-text2{
    font-weight: 300;
    font-size: 15px;
 }
</style>

<script lang="ts">

</script>