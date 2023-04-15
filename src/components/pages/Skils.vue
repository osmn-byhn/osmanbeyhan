<script setup lang="ts">
/*
    const buton = document.getElementById('v-pills-settings-tab')
    const veri = document.getElementById('v-pills-profile')
    const veri2 = document.getElementById('v-pills-home')
    const veri4 = document.getElementById('v-pills-settings')
    function show() {
        console.log(buton?.getAttribute('data-bs-target'));
        veri?.setAttribute('class', 'tab-pane fade')
        veri2?.setAttribute('class', 'tab-pane fade')
        veri4?.setAttribute('class', 'tab-pane fade show active')
    }*/
</script>

<template>

    <div class="technologies">
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
        <div class="others">
            <a href="https://git-scm.com/">
                <i class="devicon-git-plain colored" target="_blank"></i>
            </a>
            <a href="https://github.com/" target="_blank">
                <i class="devicon-github-original"></i>
            </a>
        </div>
    </div>


    <ul class="nav nav-tabs" id="myTab" role="tablist">
  <li class="nav-item" role="presentation">
    <button class="nav-link active" id="home-tab" data-bs-toggle="tab" data-bs-target="#home-tab-pane" type="button" role="tab" aria-controls="home-tab-pane" aria-selected="true">Home</button>
  </li>
  <li class="nav-item" role="presentation">
    <button class="nav-link" id="profile-tab" data-bs-toggle="tab" data-bs-target="#profile-tab-pane" type="button" role="tab" aria-controls="profile-tab-pane" aria-selected="false">Profile</button>
  </li>
  <li class="nav-item" role="presentation">
    <button class="nav-link" id="contact-tab" data-bs-toggle="tab" data-bs-target="#contact-tab-pane" type="button" role="tab" aria-controls="contact-tab-pane" aria-selected="false">Contact</button>
  </li>
  <li class="nav-item" role="presentation">
    <button class="nav-link" id="disabled-tab" data-bs-toggle="tab" data-bs-target="#disabled-tab-pane" type="button" role="tab" aria-controls="disabled-tab-pane" aria-selected="false" disabled>Disabled</button>
  </li>
</ul>
<div class="tab-content" id="myTabContent">
  <div class="tab-pane fade show active" id="home-tab-pane" role="tabpanel" aria-labelledby="home-tab" tabindex="0">home</div>
  <div class="tab-pane fade" id="profile-tab-pane" role="tabpanel" aria-labelledby="profile-tab" tabindex="0">profile</div>
  <div class="tab-pane fade" id="contact-tab-pane" role="tabpanel" aria-labelledby="contact-tab" tabindex="0">contact</div>
  <div class="tab-pane fade" id="disabled-tab-pane" role="tabpanel" aria-labelledby="disabled-tab" tabindex="0">...</div>
</div>
</template>

<style scoped lang="scss">
    @import '../../../public/Skils.scss';
</style>