<template>
    <main>
        <div class="main-container">
            <div class="text-container">
                <p id="hello">Olá Mundo!</p>
                <p id="iam">Sou <span class="name-span">João Pedro Soares</span></p>
                <p id="pres">Bem-vindo ao meu portfólio! Sou <span class="name-span">Desenvolvedor Front-End</span> e <span class="name-span">UX/UI Designer</span>, aqui você pode conhecer minha trajetória e explorar meus projetos. Tenho paixão por criar experiências digitais intuitivas, combinando design e desenvolvimento de forma eficiente. Fique à vontade para conferir meu trabalho!</p>
            </div>
        </div>
    </main>
</template>

<style scoped>
    *{
        background-color: #FFFAF8;
        box-sizing: border-box;
        padding: 0;
        margin: 0;
    }

    .main-container{
        flex-direction: column;
        width: 100vw;
        height: 100vw;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .text-container{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
    #hello{
        font-weight: 300;
        font-size: 35px;
    }
    #iam{
        font-weight: 200;
        font-size: 20px;
    }
    .name-span{
        font-weight: 600;
    }
    #pres{
        font-size: 15px;
        margin-top: 15px;
        font-weight: 200;
        text-align: center;
        max-width: 310px;
    }
</style>

<script lang="ts">

</script>