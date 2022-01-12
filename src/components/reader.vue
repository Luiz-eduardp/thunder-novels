<template>
  <q-page padding>
    <div class="q-ma-md">
      <template v-for="(novel, i) in novelList" :key="i">
        <q-btn class="novelistBtn" @click="ler = !ler">{{ novel.nome }}</q-btn>
        <div class="q-ma-md reader" v-show="ler">
          <q-select
            v-model="capAtual"
            :options="novel.caps[i]"
            label="Capítulos"
          />
          <div v-html="novel.caps[this.capAtual].content"></div>
        </div>
      </template>
    </div>
  </q-page>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      model: ref(null),
    };
  },
  // name: 'PageName',
  data() {
    return {
      novelList: [],
      novelSelect: [],
      capAtual: 0,
      ler: false,
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

.reader {
  border: 2px solid white;
  text-align: left;
  padding: 30px 30px;
}
</style>
