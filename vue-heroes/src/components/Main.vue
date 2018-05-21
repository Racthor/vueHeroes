<template>
  <div class="mainVue">
    <component:Header></component:Header>
    <h1>{{ titre }}</h1>
    <p>
      Version de vueHeroes : {{ version }}
    </p>
    <div v-if="quelleHistoire">
      <ul>
        <li v-for="(histoire, index) in findDatas()">
          <button @click="findHistory(index)">{{histoire}}</button>
        </li>
      </ul>
    </div>
    <div v-else>
      <HistoryContent />
    </div>
    <component:Footer></component:Footer>
  </div>
</template>

<script>
import HistoryContent from './HistoryContent.vue'

export default {
  name: 'Main',
  components: {
    HistoryContent
  },
  props: {
    quelleHistoire: true,
    titre: String,
    version: String
  },
  data: {
    cetteHistoire: String
  },
  methods : {
    findDatas : function () {
      //TODO : lire un fichier genre datas.json qui contient toutes les donnée nécessaire pour jouer.
      return ["histoire 1", "histoire 2", "histoire 3"];
    },
    findHistory : function (indHistoire) {
      this.quelleHistoire = false;
      this.cetteHistoire = this.findDatas()[indHistoire];
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
