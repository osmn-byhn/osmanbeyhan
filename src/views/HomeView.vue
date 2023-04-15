<script setup>
import { ref, onMounted } from 'vue'
    import ShortAbout from '../components/pages/ShortAbout.vue';
    import AboutMe from '../components/pages/AboutMe.vue';
    import Skils from '../components/pages/Skils.vue';
    import Works from '../components/pages/Works.vue'
    const isMobile = ref(false)
    function checkWindowSize() {
      isMobile.value = window.innerWidth <= 1031
    }
    onMounted(() => {
        window.addEventListener('resize', checkWindowSize)
        checkWindowSize()
    })
</script>

<template>
    <div class="mobile">
        <div class="links-container">
            <ShortAbout class="component"/>
            <AboutMe class="component" id="about" />
            <Skils class="component" id="skils" />
            <Works class="component" id="works" />
        </div>
    </div>
    
    <div class="desktop" :class="{ 'd-none': isMobile }">
        <div id="carouselExampleIndicators" class="carousel slide">
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <div>
                        <ShortAbout />
                    </div>
                </div>
                <div class="carousel-item">
                    <div>
                        <AboutMe />
                    </div>
                </div>
                <div class="carousel-item">
                    <div>
                        <Skils />
                    </div>
                </div>
                <div class="carousel-item">
                    <div>
                        <Works />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @import '../../public/HomeView.scss'
</style>