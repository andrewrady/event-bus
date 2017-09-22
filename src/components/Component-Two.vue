<template>
  <div id="two" class="ui styled accordion">
    <p>Component Two</p>
    <p>Age: {{ recievedAge }}</p>
    <button @click="clear">clear</button>
  </div>  
</template>

<script>
import { EventBus } from '../event-bus.js';

export default {
  data() {
    return {
      recievedAge: ''
    }
  },
  mounted() {
    this.moveData();
  },
  methods: {
    moveData() {
      EventBus.$on('move-age', moveAge => {
        alert('Age Sent')
        this.recievedAge = moveAge;
      })
    },
    clear() {
      this.recievedAge = '';
    }
  }
}
</script>
<style>
#two {
  height: 88px;
}
</style>
