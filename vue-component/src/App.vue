<template>
  <div id="app">
    <div class="text-center">
      <v-btn
        v-if="!chip1 && !chip2 && !chip3 && !chip4"
        close
        color="primary"
        dark
        @click="chip1 = true, chip2 = true, chip3 = true, chip4= true"
      >Reset Chips</v-btn>

      <v-chip
        v-if="chip1"
        class="ma-2"
        close
        color="deeppurple"
        text-color="white"
        @click:close="chip1 = false"
      >Purple</v-chip>

      <v-chip
        v-if="chip2"
        class="ma-2"
        close
        color="red"
        text-color="white"
        @click:close="chip2 = false"
      >Remove</v-chip>

      <v-chip
        v-if="chip3"
        class="ma-2"
        close
        color="green"
        outlined
        @click:close="chip3 = false"
      >Success</v-chip>

      <v-chip
        v-if="chip4"
        class="ma-2"
        close
        color="orange"
        label
        outlined
        @click:close="chip4 = false"
      >Complete</v-chip>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      chip1: true,
      chip2: true,
      chip3: true,
      chip4: true,
    };
  },
};
</script>