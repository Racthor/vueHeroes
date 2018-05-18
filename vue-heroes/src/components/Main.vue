<template>
  <div class="mainVue">
    <h1>{{ titre }}</h1>
    <p>
      En fait on va avoir plein de vue les unes dans les autres wesh !
    </p>
    <ul>
      <li v-for="histoire in findDatas()">
        <button @click="findHistory(histoire)">{{histoire}}</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Main',
  props: {
    titre: String,
    version: String
  },
  computed : {
  },
  methods : {
    findDatas : function () {
      //TODO : lire un fichier genre datas.json qui contient toutes les donnée nécessaire pour jouer.
      return ["histoire 1", "histoire 2", "histoire 3"];
    },
    findHistory : function (histoire) {
      alert(this.findDatas().histoire);
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
