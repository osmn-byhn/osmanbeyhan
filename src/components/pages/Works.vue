<script setup>
  import { ref } from 'vue'
  import axios from 'axios'
  const dataGithub = ref([])
  const dataLanguage = ref([])
  const config = {
    headers: {
      "Accept": "application/vnd.github.v3+json"
    }
  }
  axios.get('https://api.github.com/users/osmn-byhn/repos', config)
  .then(function (res) {
    for (let i = 0; i < res.data.length; i++) {
      const element = res.data[i];
      for (let j = 0; j < element.topics.length; j++) {
        const found = element.topics[j];
        if (found.includes('project-completed')) {
          dataGithub.value.push(element)
          axios.get(element.languages_url)
            .then(response => {
              dataLanguage.value.push(response.data)
              console.log(response);
            })
            .catch(error => {
              console.log(`Hata oluştu: ${error.message}`);
            });
          }
        }
      }
    })
  .catch(err=> console.log(err))

  
</script>

<template>
  <div class="content">
    <div class="second">
      <div class="repos" v-for="(item, i) in dataGithub">
        <ul>
          <li id="name">
            <a :href="dataGithub[i].html_url" target="_blank">{{ dataGithub[i].name }}</a>
          </li>
          <li>
            <a :href="dataGithub[i].homepage" target="_blank">
              <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </li>
        </ul>
        <div class="langs">
          <ul v-if="dataLanguage[i]">
            <li v-for="(lang, j) in dataLanguage[i]">{{ j }}</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="img">
      <img src="../../../public/angry_programmer.gif" alt="">
    </div>
  </div>
</template>


<style scoped lang="scss">
    @import '../../../public/Works.scss'
</style>