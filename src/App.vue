

<template>
  <div class="container mt-5">
    <h1 class="text-center mb-4">Chuck Norris Jokes</h1>
    <div class="row">
      <div class="col-sm-12 col-md-4 mb-4" v-for="(joke, index) in chuckJokes" :key="index">
        <chuck-card :icon-url="joke.icon_url" :value="joke.value"></chuck-card>
      </div>
    </div>
  </div>
</template>


<script>
import ChuckCard from './components/ChuckCard.vue'

export default {
  name: 'App',
  components: {
    ChuckCard
  },
  data() {
    return {
      chuckJokes: [
        {
          icon_url: "https://api.lorem.space/image/game?w=150&h=220",
          value: "Chuck Norris can skydive into outer space."
        },
        {
          icon_url: "https://api.lorem.space/image/album?w=150&h=150",
          value: "The chief export of Chuck Norris is pain."
        },
        {
          icon_url: "https://api.lorem.space/image/game?w=150&h=220",
          value: "Chuck Norris doesn’t read books. He stares them down until he gets the information he wants."
        },
        {
          icon_url: "https://api.lorem.space/image/album?w=150&h=150",
          value: "Time waits for no man. Unless that man is Chuck Norris."
        },
        {
          icon_url: "https://api.lorem.space/image/game?w=150&h=220",
          value: "If you spell Chuck Norris in Scrabble, you win. Forever."
        }
      ]
    }
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 50px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  background: #f0f0f0;
  margin: 10px 0;
  padding: 10px;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

h1 {
  color: #2c3e50;
}
</style>
