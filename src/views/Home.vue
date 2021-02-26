<template>
  <div class="home">
    <q-card dark bordered class="bg-grey-7 my-card">
      <q-card-section v-model="lorem">
        <div class="text-h6">В чем разница между null и undefined?</div>
      </q-card-section>
      </q-card>
    <Counter />
    <div class="abs">
      <div class="fit">
        <q-checkbox
          checked
          @click.prevent="togleOf"
          label="Привет"
          :disable="disable"
          v-model="val"
          color="green"
          :dark="false" />

           <q-checkbox
          label="Привет"
          :disable="false"
          v-model="val1"
          color="green"
          :dark="false" />

          <q-checkbox
          label="Привет"
          :disable="false"
          v-model="val2"
          color="green"
          :dark="false" />
      </div>
    </div>
  </div>
    <div class="q-px-sm"></div>
</template>

<script>
// @ is an alias to /src
import { ref } from 'vue';
import Counter from '../components/Counter.vue';

export default {
  name: 'Home',
  data() {
    return {
      lorem: 'lorem ipsum bkla bkjgfd asd',
      val: ref(false),
      val1: ref(false),
      val2: ref(false),
      disable: false,
    };
  },
  methods: {
    togleOf() {
      this.disable = true;
    },
  },
  components: {
    Counter,
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
    .abs{
      position: absolute;
      top: 100px;
    }
  }
</style>
