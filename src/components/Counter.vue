<template>
<div>Привет я счетчик: {{counter}} секунд</div>
</template>

<script>
import {
  onBeforeMount, onBeforeUnmount, onBeforeUpdate,
  onMounted, onUpdated,
// eslint-disable-next-line import/no-extraneous-dependencies
} from '@vue/runtime-core';

export default {
  name: 'Counter',
  data() {
    return {
      counter: 60,
      timer: null,
    };
  },
  setup() {
    onBeforeMount(() => {
    });
    onMounted(() => {
      this.startCount();
    });
    onBeforeUpdate(() => {
      // eslint-disable-next-line no-console
      console.log('Before Update!');
    });
    onUpdated(() => {
      // eslint-disable-next-line no-console
      console.log('Updated!');
    });
    onBeforeUnmount(() => {
      this.stopCount();
    });
  },
  methods: {
    startCount() {
      this.counter = setInterval(() => {
        // eslint-disable-next-line no-plusplus
        this.timer--;
      }, 1000);
    },
    stopCount() {
      clearTimeout(this.counter);
    },
  },
  watch: {
    counter(time) {
      if (time === 0) {
        this.stopCount();
      }
    },
  },
};
</script>

<style scoped lang=scss>

</style>
