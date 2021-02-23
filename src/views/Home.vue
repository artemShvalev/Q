<template>
  <div class="home">
    <q-card dark bordered class="bg-grey-7 my-card">
      <q-card-section v-model="lorem">
        <div class="text-h6">В чем разница между null и undefined?</div>
      </q-card-section>
      </q-card>
    <div class="q-pa-md">
      <div class="q-gutter-sm">
        <q-checkbox
          label="Привет"
          :disable="false"
          v-model="val"
          :dark="false" />
      </div>
  </div>
    <div class="q-px-sm">
    </div>
</div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue';

export default {
  name: 'Home',
  data() {
    return {
      lorem: 'lorem ipsum bkla bkjgfd asd',
      val: ref(true),
    };
  },
};
</script>

<style scoped lang="scss">
  .home {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    top: 200px;
    left: 0;
    right: 0;
    .my-card {
      width: 100%;
      height: 100%;
      max-width: 600px;
      max-height: 500px;
    }
  }
</style>
