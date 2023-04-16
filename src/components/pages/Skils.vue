<script setup>
import { ref } from 'vue'
const activeTab = ref('web')
/*
    const buton = document.getElementById('v-pills-settings-tab')
    const veri = document.getElementById('v-pills-langs')
    const veri2 = document.getElementById('v-pills-web')
    const veri4 = document.getElementById('v-pills-settings')
    function show() {
        console.log(buton?.getAttribute('data-bs-target'));
        veri?.setAttribute('class', 'tab-pane fade')
        veri2?.setAttribute('class', 'tab-pane fade')
        veri4?.setAttribute('class', 'tab-pane fade show active')
    }*/

</script>

<template>
    <div class="skills">
        <ul class="nav nav-tabs" id="myTab" role="tablist">
            <li class="nav-item  " role="presentation">
                <button class="nav-link" :class="{ active: activeTab === 'web' }" @click="activeTab = 'web'" id="web-tab" data-bs-toggle="tab" data-bs-target="#web-tab-pane" type="button" role="tab" aria-controls="web-tab-pane" aria-selected="true">web</button>
            </li>
            <li class="nav-item " role="presentation">
                <button class="nav-link" :class="{ active: activeTab === 'langs' }" @click="activeTab = 'langs'" id="langs-tab" data-bs-toggle="tab" data-bs-target="#langs-tab-pane" type="button" role="tab" aria-controls="langs-tab-pane" aria-selected="false">langs</button>
            </li>
            <li class="nav-item " role="presentation">
                <button class="nav-link" :class="{ active: activeTab === 'others' }" @click="activeTab = 'others'" id="others-tab" data-bs-toggle="tab" data-bs-target="#others-tab-pane" type="button" role="tab" aria-controls="others-tab-pane" aria-selected="false">others</button>
            </li>
        </ul>
        <div class="tab-content">
        <div class="tab-pane fade" :class="{ show: activeTab === 'web', active: activeTab === 'web' }" id="web-tab-pane" role="tabpanel" aria-labelledby="web-tab">
            <div class="mevn">
                <a href="https://www.mongodb.com/" target="_blank">
                    <i class="devicon-mongodb-plain colored"></i>
                </a>
                <a href="https://expressjs.com/" target="_blank">
                    <i class="devicon-express-original"></i>
                </a>
                <a href="https://vuejs.org/" target="_blank">
                    <i class="devicon-vuejs-plain colored"></i>
                </a>
                <a href="https://nodejs.org" target="_blank">
                    <i class="devicon-nodejs-plain colored"></i>
                </a>
                <a href="https://sass-lang.com/" target="_blank">
                    <i class="devicon-sass-original colored"></i>
                </a>
            </div>
      </div>
      <div class="tab-pane fade" :class="{ show: activeTab === 'langs', active: activeTab === 'langs' }" id="langs-tab-pane" role="tabpanel" aria-labelledby="langs-tab">
        <div class="languages">
            <a href="https://www.typescriptlang.org/" target="_blank">
                <i class="devicon-typescript-plain colored"></i>
            </a>
            <a href="https://javascript.info/" target="_blank">
                <i class="devicon-javascript-plain colored"></i>
            </a>
            <a href="https://www.python.org/" target="_blank">
                <i class="devicon-python-plain"></i>
            </a>
        </div>
      </div>
      <div class="tab-pane fade" :class="{ show: activeTab === 'others', active: activeTab === 'others' }" id="others-tab-pane" role="tabpanel" aria-labelledby="others-tab">
        <div class="others">
            <a href="https://git-scm.com/">
                <i class="devicon-git-plain colored" target="_blank"></i>
            </a>
            <a href="https://github.com/" target="_blank">
                <i class="devicon-github-original"></i>
            </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
    @import '../../../public/Skils.scss';
</style>