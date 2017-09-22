<template>
  <div id="one" class="ui styled accordion">
    <p>Component One</p>
    <p>Age from data: {{age}}</p>
    <button @click="sendData">Send Age</button>
  </div>
</template>

<script>
import { EventBus } from '../event-bus.js';

export default {
  data () {
    return {
     age: 25
    }
  },
  methods: {
    sendData() {
      EventBus.$emit('move-age', this.age);
    }
  }
}
</script>
<style>
#one {
  height: 88px;
}
</style>
