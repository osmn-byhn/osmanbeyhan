<script setup>
    const date = new Date();
    let year = date.getFullYear();


    // Authorization token that must have been created previously. See : https://developer.spotify.com/documentation/web-api/concepts/authorization
const token = 'BQCILfIMQB6ujvZl4tKF95jEqTNvao1_Y0ocO6A22tKZvSQEBfSDZSO3UT9npkZPQgSunicz8Hul-Bkgz1NKy2Pph7BWFCQ44qUW9159F5gtYan0bYqlhRvf7F9Fmx6XlucPipT3BJJFWI-vosnl0no3jFI_Eo6kk8XGhIMXgj2Ri-bkgOuWVVIxKh2OeKSzpW7PuvQpuy7LNL4sVin_0nviyPMaqaYqM-vrswHrlR2_wg7W-looA-0cNMMg8EGmtF54HH-CGIQ4WyP36Dk_Cp_Wv49J65xD8hl9XjEijU65uCkqXtH5r3MsFrAOvFT3FZRuuiDEOuInvCdr_2NtiZVMqZZtdnKlKSpyQN8kEDqU-VUEM6s';
async function fetchWebApi(endpoint, method, body) {
  const res = await fetch(`https://api.spotify.com/${endpoint}`, {
    headers: {
      Authorization: `Bearer ${token}`,
    },
    method,
    body:JSON.stringify(body)
  });
  return await res.json();
}

async function getTopTracks(){
  // Endpoint reference : https://developer.spotify.com/documentation/web-api/reference/get-users-top-artists-and-tracks
  return (await fetchWebApi(
    'v1/me/top/tracks?time_range=short_term&limit=5', 'GET'
  )).items;
}

const topTracks = await getTopTracks();
console.log(
  topTracks?.map(
    ({name, artists}) =>
      `${name} by ${artists.map(artist => artist.name).join(', ')}`
  )
);
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