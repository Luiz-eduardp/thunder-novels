<template>
  <q-page padding>
      <q-carousel
        v-model="slide"
        transition-prev="jump-right"
        transition-next="jump-left"
        swipeable
        animated
        control-color="black"
        prev-icon="arrow_left"
        next-icon="arrow_right"
        navigation-icon="radio_button_checked"
        navigation
        padding
        arrows
        height="300px"
        class="bg-secondary text-black shadow-1 rounded-borders"
      >
        <q-carousel-slide name="style" class="column no-wrap flex-center">
          <q-icon name="trending_up" size="56px" />
          <div class="q-mt-md text-center">
            Traduções de Qualidade na Velocidade da Luz!
          </div>
        </q-carousel-slide>



      </q-carousel>

  </q-page>
</template>
<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref('style'),
    }
  },

}
</script>
