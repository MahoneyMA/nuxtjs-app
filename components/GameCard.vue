<template>
  <section>
    <button class="accordion" @click="isOpen = !isOpen">
      <a class="bold">
        <p
          v-if="game.player_slot < 128 && game.radiant_win ||
            game.player_slot >=128 && !game.radiant_win"
        > WIN
        </p>
        <p v-else>LOSE</p>
      </a>
      Hero: {{ heroes.localized_name }}
      KDA: {{ game.kills }}/{{ game.deaths }}/{{ game.assists }}
    </button>
    <transition name="ease-out">
      <div v-show="isOpen" id="game.match_id" class="panel">
        <div> {{ new Date(game.start_time * 1000).toString() }}</div>
        <div>
          Match Length: {{ parseInt(game.duration/60,10) }}:
          <span v-if="game.duration%60 < 10">
            0{{ game.duration%60 }}
          </span>
          <span v-else>{{ game.duration%60 }}</span>
        </div>
      </div>
    </transition>
  </section>
</template>

<script>
export default {
  name: 'GameCard',
  props: {
    game: {
      type: Object,
      required: true
    },
    heroes: {
      type: Array,
      required: true
    }
  },
  data: () => {
    return {
      isOpen: false
    }
  }
}
</script>

<style scoped>
.accordion {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
  transition: 0.4s;
}

.active, .accordion:hover {
  background-color: #ccc;
}

.accordion:after {
  content: '\002B';
  color: #777;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}
.panel {
  float:left;
  width:100%;
  text-align:left;
  padding: 0 18px;
  color: white;
  background-color: black;
  overflow: hidden;
}
.ease-out{
  transition:all .3s ease;
}
</style>
