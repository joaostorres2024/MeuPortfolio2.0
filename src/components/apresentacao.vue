<template>
    <main>
        <div class="main-container">
                <p id="hello">Olá Mundo!</p>
                <p id="iam">Sou <span class="name-span">João Pedro Soares</span></p>
                <p id="pres">Bem-vindo ao meu portfólio! Sou <span class="name-span">Desenvolvedor Front-End</span> e <span class="name-span">UX/UI Designer</span>, aqui você pode conhecer minha trajetória e explorar meus projetos. Tenho paixão por criar experiências digitais intuitivas, combinando design e desenvolvimento de forma eficiente. Fique à vontade para conferir meu trabalho!</p>
                <img id="imagem" :src="eu" alt="Minha imagem">
                <div class="redes-sociais">
            <ul class="redes-sociais-ul">
                <a href="https://www.linkedin.com/in/jo%C3%A3o-pedro-soares-torres-101a532b4/" target="_blank"><li class="iconni"><img class="icons-img" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBmaWxsPSIjMDAwIiBkPSJNMTkgM2EyIDIgMCAwIDEgMiAydjE0YTIgMiAwIDAgMS0yIDJINWEyIDIgMCAwIDEtMi0yVjVhMiAyIDAgMCAxIDItMnptLS41IDE1LjV2LTUuM2EzLjI2IDMuMjYgMCAwIDAtMy4yNi0zLjI2Yy0uODUgMC0xLjg0LjUyLTIuMzIgMS4zdi0xLjExaC0yLjc5djguMzdoMi43OXYtNC45M2MwLS43Ny42Mi0xLjQgMS4zOS0xLjRhMS40IDEuNCAwIDAgMSAxLjQgMS40djQuOTN6TTYuODggOC41NmExLjY4IDEuNjggMCAwIDAgMS42OC0xLjY4YzAtLjkzLS43NS0xLjY5LTEuNjgtMS42OWExLjY5IDEuNjkgMCAwIDAtMS42OSAxLjY5YzAgLjkzLjc2IDEuNjggMS42OSAxLjY4bTEuMzkgOS45NHYtOC4zN0g1LjV2OC4zN3oiLz48L3N2Zz4=" alt=""></li></a>
                <a href="https://github.com/joaostorres2024" target="_blank"><li class="iconsi"><img class="icons-img" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBmaWxsPSIjMDAwIiBkPSJNMTIgMkExMCAxMCAwIDAgMCAyIDEyYzAgNC40MiAyLjg3IDguMTcgNi44NCA5LjVjLjUuMDguNjYtLjIzLjY2LS41di0xLjY5Yy0yLjc3LjYtMy4zNi0xLjM0LTMuMzYtMS4zNGMtLjQ2LTEuMTYtMS4xMS0xLjQ3LTEuMTEtMS40N2MtLjkxLS42Mi4wNy0uNi4wNy0uNmMxIC4wNyAxLjUzIDEuMDMgMS41MyAxLjAzYy44NyAxLjUyIDIuMzQgMS4wNyAyLjkxLjgzYy4wOS0uNjUuMzUtMS4wOS42My0xLjM0Yy0yLjIyLS4yNS00LjU1LTEuMTEtNC41NS00LjkyYzAtMS4xMS4zOC0yIDEuMDMtMi43MWMtLjEtLjI1LS40NS0xLjI5LjEtMi42NGMwIDAgLjg0LS4yNyAyLjc1IDEuMDJjLjc5LS4yMiAxLjY1LS4zMyAyLjUtLjMzczEuNzEuMTEgMi41LjMzYzEuOTEtMS4yOSAyLjc1LTEuMDIgMi43NS0xLjAyYy41NSAxLjM1LjIgMi4zOS4xIDIuNjRjLjY1LjcxIDEuMDMgMS42IDEuMDMgMi43MWMwIDMuODItMi4zNCA0LjY2LTQuNTcgNC45MWMuMzYuMzEuNjkuOTIuNjkgMS44NVYyMWMwIC4yNy4xNi41OS42Ny41QzE5LjE0IDIwLjE2IDIyIDE2LjQyIDIyIDEyQTEwIDEwIDAgMCAwIDEyIDIiLz48L3N2Zz4=" alt=""></li></a>
                <a href="https://www.instagram.com/joaotrrs/" target="_blank"><li class="iconsi"><img class="icons-img" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBmaWxsPSIjMDAwIiBkPSJNNy44IDJoOC40QzE5LjQgMiAyMiA0LjYgMjIgNy44djguNGE1LjggNS44IDAgMCAxLTUuOCA1LjhINy44QzQuNiAyMiAyIDE5LjQgMiAxNi4yVjcuOEE1LjggNS44IDAgMCAxIDcuOCAybS0uMiAyQTMuNiAzLjYgMCAwIDAgNCA3LjZ2OC44QzQgMTguMzkgNS42MSAyMCA3LjYgMjBoOC44YTMuNiAzLjYgMCAwIDAgMy42LTMuNlY3LjZDMjAgNS42MSAxOC4zOSA0IDE2LjQgNHptOS42NSAxLjVhMS4yNSAxLjI1IDAgMCAxIDEuMjUgMS4yNUExLjI1IDEuMjUgMCAwIDEgMTcuMjUgOEExLjI1IDEuMjUgMCAwIDEgMTYgNi43NWExLjI1IDEuMjUgMCAwIDEgMS4yNS0xLjI1TTEyIDdhNSA1IDAgMCAxIDUgNWE1IDUgMCAwIDEtNSA1YTUgNSAwIDAgMS01LTVhNSA1IDAgMCAxIDUtNW0wIDJhMyAzIDAgMCAwLTMgM2EzIDMgMCAwIDAgMyAzYTMgMyAwIDAgMCAzLTNhMyAzIDAgMCAwLTMtMyIvPjwvc3ZnPg==" alt=""></li></a>
            </ul>
        </div>
        </div>
    </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import eu from '@/assets/eu.png';

export default defineComponent({
    name: 'Apresentacao',
    data() {
        return {
            eu,
        };
    },
});
</script>

<style scoped>
* {
    background-color: #FFFAF8;
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

.main-container {
    flex-direction: column;
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

#hello {
    font-weight: 300;
    font-size: 35px;
}

#iam {
    font-weight: 200;
    font-size: 20px;
}

.name-span {
    font-weight: 600;
}

#pres {
    font-size: 15px;
    margin-top: 15px;
    font-weight: 200;
    text-align: center;
    max-width: 310px;
}

#imagem{
    margin-top: 40px;
    width: 300px;
    animation: animacao 2S infinite;
}
.redes-sociais{
    margin-top: 40px;
    list-style-type: none;
    justify-content: center;
    width: 100vw;
    display: flex;
    align-items: center;
}
.redes-sociais ul{
    list-style-type: none;
    justify-content: center;
    align-items: center;
    display: flex;
}

.icons-img{
    width: 55px;
    padding: 0 10px;
}

@keyframes animacao {
    0%{
        transform: translateY(0px);
    }
    50%{
        transform: translateY(-10px);
    }
    100%{
        transform: translateY(0);
    }
}
</style>
