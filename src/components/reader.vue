<template>
  <div>



    <div class="post">
<q-btn color="primary" text-color="black" @click="configOpen = !configOpen">Configurações</q-btn>
<div class="control bg-primary" v-show="configOpen" >
  <div style="padding:20px 10px 10px 10px">
    <q-btn @click="darkMode = !darkMode">Dark Mode</q-btn>
     <q-btn @click="darkMode = !darkMode">Aumentar Fonte </q-btn>
       <q-btn @click="darkMode = !darkMode">Diminuir Fonte</q-btn>
  </div>
</div>
  <div class="closeArticle">Close Article</div>
  <span class="company">{{obraNome}}</span>
  <h3>{{capTit}}</h3>

  <div class="author">{{tradutor}} </div>


  <article>
    <p>Etiam eu feugiat purus. Sed eget tortor eget massa maximus blandit sit amet nec libero. Quisque vel arcu vitae nisi luctus tincidunt a ut sem. Etiam ultricies mollis elit nec sollicitudin. Pellentesque sit amet ex quis elit dictum fermentum. Praesent
      a nibh nec mi faucibus porttitor ac id mi. Duis faucibus ligula ac diam tempus, vel vulputate velit eleifend. In facilisis nisi mauris, sit amet vehicula dui euismod non. Fusce venenatis ultricies faucibus. Proin lacinia vel orci gravida dictum.
      Aliquam pretium aliquet rhoncus. Donec at erat tincidunt magna fermentum pharetra sit amet ut risus.</p>

    <p>Donec tincidunt, metus eu ullamcorper mollis, justo ipsum placerat dui, ac vestibulum nibh libero vitae enim. Ut viverra dui eget nisi consectetur tincidunt. Vestibulum ut tincidunt nulla, vitae bibendum tellus. Nulla facilisi. Integer molestie tortor
      et nisi posuere, non lacinia lacus luctus. Proin eu sollicitudin mi. Etiam at odio augue. Aliquam erat volutpat. Duis malesuada sit amet justo vel pulvinar. Sed elementum et eros eget imperdiet. Duis ut ante ipsum.</p>

    <p>Nulla facilisi. Curabitur purus nisi, interdum vitae turpis vel, commodo volutpat lorem. Phasellus ultricies pharetra nisl ullamcorper ultrices. Etiam suscipit cursus urna, sed ultrices metus finibus quis. Aenean turpis libero, aliquam eget elit eget,
      porta hendrerit turpis. Sed vel ante quis sem faucibus faucibus. Sed nibh libero, vulputate eget ligula tempus, pharetra aliquam turpis. Maecenas arcu leo, volutpat sit amet ipsum a, posuere tristique ipsum. Nam viverra ex sed justo consectetur
      pulvinar. In non nunc id mauris vehicula tincidunt nec eu nunc. Vivamus vestibulum augue orci, non venenatis enim pellentesque vitae.</p>

    <p>Fusce ut suscipit nisi, et suscipit ipsum. Mauris vel augue at libero pellentesque lobortis. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum suscipit lacus non ex hendrerit tristique. Maecenas
      gravida felis in elit rhoncus, tincidunt bibendum felis ornare. Sed eu metus sed neque posuere fringilla eu a urna. In ac nulla iaculis, ornare orci sit amet, suscipit dui. Mauris sed est tortor. Quisque tincidunt, velit fermentum sagittis scelerisque,
      risus libero consequat mi, vel viverra ante velit ut ipsum. Sed nunc velit, convallis vel volutpat nec, viverra et dolor. Nunc sit amet purus vitae est sollicitudin semper nec non dolor. Nunc mattis nibh sem, eu pretium elit consectetur a. Quisque
      ante ante, congue ac consequat at, commodo et urna. Nam ullamcorper blandit iaculis. Donec bibendum hendrerit nisi eu aliquet. Suspendisse tellus urna, vestibulum vel ex at, posuere condimentum metus.</p>
  </article>

  <div class="keepReading">Próximo</div>
   <div class="keepReading">Indíce</div>
   <div class="keepReading">Anterior</div>
</div></div>
</template>

<script>
export default {
  // name: 'ComponentName',
  setup () {
    return {}
  },
  data() {
    return {
      obraNome:'Supreme Magus',
      capTit:'Cap-01',
      tradutor:'Edu',
      configOpen:false,
      darkMode: false
    }
  },
  methods: {
    configs(){

    }
  },
}
</script>


<style>

.post {
  background: white;
  max-width: 900px;
  padding: 50px;
  margin: 50px auto;
}

#pressCoverage .post h3 {
  font-size: 24px;
  padding: 0;
  margin: 0;
}

.post h1 {
  padding: 5px 0px;
}

#pressReleases .post h3 {
  font-size: 24px;
  padding-bottom: 15px;
  margin: 0;
}

.post .company {
  font-weight: 700;
  text-transform: uppercase;
}

.post:nth-of-type(1) .company {
  border-bottom: #F57C00 solid 3px;
}

.post:nth-of-type(2) .company {
  border-bottom: yellow solid 3px;
}

.post .author {
  color: grey;
  padding: 15px 0px;
}

.post .keepReading,
.post .closeArticle {
  float: right;
  font-weight: 700;
  text-transform: uppercase;
  cursor: pointer;
  text-decoration: none;
  color: black;
}

.post .closeArticle {
  opacity: 0;
}

.post article {
  display: initial;
}

@media screen and (max-width: 980px) {
  .post h3 {
    font-size: 20px;
    line-height: 28px;
  }
  .post h2 {
    font-size: 32px;
    line-height: 40px;
  }
  .post .keepReading,
  .post .closeArticle {
    width: 100%;
    text-align: center;
    float: none;
    margin: 20px auto 0px;
  }
  .post .closeArticle {
    margin: 0px auto 20px;
  }
}
</style>
