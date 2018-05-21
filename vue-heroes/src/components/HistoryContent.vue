<template>
  <div class="mainVue">
    <h1>{{ histoire }}</h1>
  </div>
</template>

<script>
//import HistoryContent from './components/HistoryContent.vue'

export default {
  name: 'HistoryContent',
  /*components: {
    
  },*/
  props: {
    histoire: String
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
