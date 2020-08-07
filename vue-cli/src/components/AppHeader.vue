<template>
  <header>
    <h1>{{ propsdata }}</h1>
    <button v-on:click="sendEvent">Send</button>
  </header>
</template>

<script>
export default {
  props: ["propsdata"],
  sendEvent: function () {
    this.$emit("renew");
  },
};
</script>

<style>
</style>