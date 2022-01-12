<template>
  <q-page padding>
    <div class="q-ma-md">
 <template v-for="(novel, i) in novelList" :key="i">
       <q-btn class="novelistBtn">  <router-link :to="this.novel.nome">{{ novel.nome }}</router-link></q-btn>

 </template>
      </div>
     </q-page>
</template>

<script>
export default {
  // name: 'PageName',
  data() {
    return {
      novelList: [],
    };
  },
  created() {
    // Simple GET request using fetch
    this.ler = false;
    fetch("https://api.npoint.io/b44f929370822909de6b")
      .then((response) => response.json())
      .then((data) => (this.novelList = data));
  },
};
</script>

<style>
.novelistBtn {
  background-color: #ff9800 !important;
  color: black;
  margin-top: 15px;
  margin-left: 15px;
}

</style>
