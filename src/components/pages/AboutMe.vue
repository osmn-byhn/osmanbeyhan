<script setup lang="ts">
    const date = new Date();
    let year = date.getFullYear();
</script>

<template>
    <div class="content">
        <div class="image">
            <img src="https://pa1.narvii.com/5807/f8b961aa03e6121f3801b16a9f7cefb753f416fb_hq.gif" alt="">
        </div>
        <div class="about">
            <h1 id="title">Hello!👋</h1>
            <p id="description-1">
                My name is Osman. I am a web developer living in Turkey. Let me tell you about myself a little bit; I like to create things and I learning programming and I've been coding for 4 years. Now I am {{ year - 2004 }} years old and I think I'am a young programmer so I have a lot to learn.
            </p>
            <p class="description-2">
                I have insatiable curiosity and I learning fastly so I want to use this feature for my career. My life philosophy; to learn and to teach what I have learned.
            </p>
            <p class="description-3">
                I love to learn because It is the reason for living that I have found for my meaningless life.
            </p>
            <p class="description-4">
                I love to teach because I think "The fastest way to learn is to teach".
            </p>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @import '../../../public/AboutMe.scss';
</style>