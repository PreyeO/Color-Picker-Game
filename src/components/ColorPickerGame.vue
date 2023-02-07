<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { ref, reactive } from "@vue/reactivity";
import ColorPicker from "../composables/color-picker";

export default {
  setup() {
    const { colors, message, matchColor } = ColorPicker();
    return { colors, message, matchColor };
  },
};
</script>

<style></style>