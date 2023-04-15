<script setup>
    import Offcanvas from "../components/Offcanvas.vue";
    const toggle = () => {
        var icon = document.getElementById('icon')
        if(document.body.classList.contains("light")){
            document.body.classList.remove("light")
            document.body.classList.add("dark")
            icon.setAttribute('class', 'bi bi-sun-fill')
        } else {
            document.body.classList.add("light")
            icon.setAttribute('class', 'bi bi-moon-fill')
        }
    }

</script>

<template>
    <nav>
        <ul>
            <li id="head"  data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1">
                <a  id="osmanbeyhan">
                    <h3>
                        osman<span>beyhan</span> 
                    </h3>
                </a>
                <a href="" id="icon-power">
                    <i class="fa-solid fa-power-off"></i>
                </a>
            </li>
            <li id="links">
                <ul>
                    <li data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2">
                        <a href="/#about">about-me()</a>
                    </li>
                    <li data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3">
                        <a href="/#skils">skils()</a>
                    </li>
                    <li data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3" aria-label="Slide 4">
                        <a href="/#works">works()</a>
                    </li>
                </ul>
            </li>
            <li id="social-medias">
                <ul id="account-icon">
                    <li>
                        <a href="https://www.instagram.com/osmn_byhn/" target="_blank">
                            <i class="bi bi-instagram"></i>
                        </a>
                    </li>
                    <li>
                        <a href="https://www.linkedin.com/in/osman-beyhan-12304b23a/" target="_blank">
                            <i class="bi bi-linkedin"></i>
                        </a>
                    </li>
                    <li>
                        <a href="https://github.com/osmn-byhn" target="_blank">
                            <i class="bi bi-github"></i>
                        </a>
                    </li>
                    <li>
                        <a href="mailto:osmanbeyhan12@gmail.com" target="_blank">
                            <i class="bi bi-envelope-at-fill"></i>
                        </a>
                    </li>
                    <li>
                        <a href="https://wa.me/+905350217844">
                            <i class="bi bi-whatsapp"></i>
                        </a>
                    </li>
                </ul>
                <ul id="icons">
                    <li id="sun">
                        <i class="bi bi-brightness-high-fill" id="icon" @click="toggle()"></i>
                    </li>
                    <li id="burger">
                        <a type="button" class="btn" data-bs-toggle="modal" data-bs-target="#exampleModal">
                            <i class="fa-solid fa-burger"></i>
                        </a>
                    </li>
                </ul>
            </li>
        </ul>
    </nav>
    <Offcanvas />
</template>

<style scoped lang="scss">
    @import "../../public/Navbar.scss"
</style>