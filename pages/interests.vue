<template>
  <div>
    <Header />
    <div class="container">
      <div v-for="game in games" :key="game.match_id">
        <GameCard
          :game="game"
          :heroes="heroes"
        />
      </div>
    </div>
  </div>
</template>

<script>
import GameCard from '../components/GameCard'
export default {
  name: 'Interests',
  components: {
    GameCard
  },
  data () {
    return {
      games: [],
      heroes: [],
      url: 'https://api.opendota.com/api/players/103266538/matches?limit=5&offset=0'
    }
  },
  async fetch () {
    this.games = await fetch(this.url).then(res => res.json())
  }
}

</script>

<style scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: block;
  width: 60%;
  padding: 30px;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
