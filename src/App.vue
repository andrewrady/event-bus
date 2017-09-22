<template>
  <div id="app" class="ui container">
    <h1>Event Bus Demo</h1>
    <div class="ui grid">
      <div class="eight wide column">
        <component-one></component-one>
      </div>
      <div class="eight wide column">
        <component-two></component-two>
      </div>
    </div>
  </div>
</template>

<script>
import componentOne from './components/Component-One.vue';
import componentTwo from './components/Component-Two.vue';

export default {
  components: {
    componentOne,
    componentTwo
  }  
}
</script>
