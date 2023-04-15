<script setup lang="ts">
</script>

<template>
    <div class="modal" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-fullscreen">
            <div class="modal-content">
                <div class="modal-head">
                    <h1 class="modal-title fs-5" id="exampleModalLabel">
                        <a href="/">
                            <i class="fa-solid fa-power-off"></i>
                        </a>
                    </h1>
                    <button type="button" data-bs-dismiss="modal" aria-label="Close">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>
                <div class="modal-links">
                    <ul>
                        <li data-bs-dismiss="modal" aria-label="Close">
                            <a href="#about">about-me()</a>
                        </li>
                        <li data-bs-dismiss="modal" aria-label="Close">
                            <a id="link" href="/#skils">skils()</a>
                        </li>
                        <li data-bs-dismiss="modal" aria-label="Close">
                            <a id="link" href="/#works">works()</a>
                        </li>
                    </ul>                
                </div>
                <div class="modal-foot">
                    <hr>
                    <ul>
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
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @import "../../public/Offcanvas.scss"
</style>