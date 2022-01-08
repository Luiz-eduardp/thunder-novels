<template>
<q-page padding>
    <div class="q-ma-md" >
        <template v-for="(novel, i) in novelList" :key="i">
            <q-btn class="novelistBtn" @click="ler = !ler">{{novel.nome}}</q-btn>
 <div class="q-ma-md reader" v-show="ler">
   <q-select v-model="novel.caps.index" :options="capAtual" label="Standard" />
   {{novel.caps[this.capAtual].content}}
     </div>
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
            novelSelect:[],
            capAtual:0,
            ler:false
        }
    },
     created() {
  // Simple GET request using fetch
  this.ler = false
  fetch("https://api.npoint.io/b44f929370822909de6b")
    .then(response => response.json())
    .then(data => (this.novelList = data));
}
}
</script>

<style>

.novelistBtn{
  background-color:#FF9800 !important;
  color:black;
  margin-top: 15px;
  margin-left: 15px;
}

.reader{
border: 2px solid white;
}
</style>
