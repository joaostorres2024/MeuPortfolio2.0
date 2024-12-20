<template>
    <header>
        <section class="header-mobile">
            <div class="header-container">
                <p id="p-text1">João Pedro Soares Torres</p>
                <p id="p-text2">Desenvolvedor Front-End e UX/UI Designer</p>
            </div>
            <nav>
                <div class="menu">
                    <img id="menu-icon" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iLTUgLTcgMjQgMjQiPjxwYXRoIGZpbGw9IiMwMDAiIGQ9Ik0xIDBoNWExIDEgMCAxIDEgMCAySDFhMSAxIDAgMSAxIDAtMm03IDhoNWExIDEgMCAwIDEgMCAySDhhMSAxIDAgMSAxIDAtMk0xIDRoMTJhMSAxIDAgMCAxIDAgMkgxYTEgMSAwIDEgMSAwLTIiLz48L3N2Zz4=" alt="Menu Icon">
                </div>
            </nav> 
        </section>
        <!--HEADER DESKTOP-->
        <section class="header-desktop">
            <div class="header-container">
                <p id="p-text1">João Pedro Soares Torres</p>
                <p id="p-text2">Desenvolvedor Front-End e UX/UI Designer</p>
            </div>
            <nav>
                <div class="nav-container">
                    <ul>
                        <a href="/meu-portfolio-2-0/src/App.vue"><li>HOME</li></a>
                        <a href="#"><li>SOBRE MIM</li></a> 
                        <a href="#"><li>EXPERIÊNCIA</li></a>
                        <a href="#"><li>CERTIFICADOS</li></a>
                        <a href="#"><li>PROJETOS</li></a>
                        <a href="#"><li>CONTATO</li></a>
                    </ul>
                </div>
            </nav>
        </section>
        <section id="menu" :class="{ 'full-screen-menu': isMenuVisible, 'hide-menu': !isMenuVisible }">
            <ul class="menu-ul"> 
                <li><a href="/meu-portfolio-2-0/src/App.vue">HOME</a></li>
                <li><a href="#">SOBRE MIM</a></li>
                <li><a href="#">EXPERIÊNCIA</a></li> 
                <li><a href="#">CERTIFICADOS</a></li>
                <li><a href="#">PROJETOS</a></li>
                <li><a href="#">CONTATO</a></li>
                <li class="moon"><img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBmaWxsPSIjZmZmIiBkPSJNMTIgMjJjNS41MjMgMCAxMC00LjQ3NyAxMC0xMGMwLS40NjMtLjY5NC0uNTQtLjkzMy0uMTQzYTYuNSA2LjUgMCAxIDEtOC45MjQtOC45MjRDMTIuNTQgMi42OTMgMTIuNDYzIDIgMTIgMkM2LjQ3NyAyIDIgNi40NzcgMiAxMnM0LjQ3NyAxMCAxMCAxMCIvPjwvc3ZnPg==" alt=""></li>
            </ul>
        </section>
    </header>
</template>

<style scoped>
*{}

.header-desktop{
    display: none;
}

.header-mobile {
    background: #FFFAF8;
    padding: 30px;
    align-items: center;
    justify-content: space-between;
    display: flex;
    width: 100vw;
    height: 100px;
}

#menu-icon {
    width: 50px;
    height: auto; /* Ajusta a altura para que seja proporcional */
    cursor: pointer;
    border: none; /* Remove qualquer borda */
    background: none; /* Remove qualquer fundo */
    padding: 0; /* Remove qualquer padding */
    transition: transform 0.3s ease-in-out;
}

#menu-icon.open {
    animation: rotate-to-x 0.3s forwards;
}

#menu-icon.close {
    animation: rotate-to-menu 0.3s forwards;
}

@keyframes rotate-to-x {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(45deg);
    }
}

@keyframes rotate-to-menu {
    0% {
        transform: rotate(45deg);
    }
    100% {
        transform: rotate(0deg);
    }
}

#p-text1 {
    font-weight: 300;
    font-size: 15px;
}

#p-text2 {
    font-weight: 300;
    font-size: 10px;
}

.menu-ul {
    display: none;
    background-color: #3D0094;
    height: 300px;
    width: 100vw;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    position: absolute; /* Posiciona o menu abaixo do cabeçalho */
    top: 100px; /* Ajuste esta altura de acordo com a altura do seu cabeçalho */
    transform: translateX(100%);
    transition: transform 0.3s ease-in-out;
}

.menu-ul.slide-in-right {
    transform: translateX(0);
}

.menu-ul.slide-out-left {
    transform: translateX(100%);
}

.menu-ul li {
    padding: 1px;
    display: none;
    font-weight: 600;
    font-size: 22px;
    list-style: none;
}

.menu-ul a {
    display: none;
    background-color: transparent;
    color: #FFFAF8;
    text-decoration: none;
}

.moon {
    margin-top: 20px;
}

@media (min-width: 1000px) {
    .header-mobile{
        display: none;
    }
    .header-desktop{
        padding: 30px;
        align-items: center;
        justify-content: space-between;
        background-color: #FFFAF8;
        height: 100px;
        width: 100vw;
        display: flex;
    }

    .nav-container ul{
        color: black;
        list-style-type: none;
        display: flex;
    }

    .nav-container ul a{
        font-weight: 300;
        padding: 10px;
        color: black;
        text-decoration: none;
    }
    #p-text1{
        font-size: 22px;
    }
    #p-text2{
        font-size: 15px;
    }
    .nav-container a:hover{
    color: #3D0094;
    transition: 0.3s ease;
}
}  
</style>




<script lang="ts">
document.addEventListener('DOMContentLoaded', () => {
    const menuul = document.querySelector<HTMLUListElement>('.menu-ul');
    const menuli = document.querySelectorAll<HTMLLIElement>('.menu-ul li');
    const menua = document.querySelectorAll<HTMLAnchorElement>('.menu-ul a');
    const menuicon = document.getElementById('menu-icon');

    const showMenu = () => {
        if (menuul && menuicon) {
            menuul.style.display = 'flex';
            menuicon.classList.add('open');
            menuicon.classList.remove('close');
            setTimeout(() => {
                menuul.classList.remove('slide-out-left');
                menuul.classList.add('slide-in-right');
                menuli.forEach(item => item.style.display = 'block');
                menua.forEach(item => item.style.display = 'block');
            }, 10);
        }
    };

    const hideMenu = () => {
        if (menuul && menuicon) {
            menuul.classList.remove('slide-in-right');
            menuul.classList.add('slide-out-left');
            menuicon.classList.remove('open');
            menuicon.classList.add('close');
            setTimeout(() => {
                menuul.style.display = 'none';
                menuli.forEach(item => item.style.display = 'none');
                menua.forEach(item => item.style.display = 'none');
            }, 300);
        }
    };

    menuicon?.addEventListener('click', (event) => {
        event.stopPropagation();
        if (menuul?.style.display === 'none' || !menuul?.style.display) {
            showMenu();
        } else {
            hideMenu();
        }
    });

    window.addEventListener('click', hideMenu);
    menuul?.addEventListener('click', (event) => {
        event.stopPropagation();
    });
});
</script>






