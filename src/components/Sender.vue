<template>
  <b-card>
    <input v-model="number" type="number" />
    <button @click="changeNumber">
     Change number
    </button>
  </b-card>
</template>

<script>
import { EventBus } from "../event-bus.js";
export default {
  name: "NumberSubmit",
  data() {
    return {
      number: 0
    };
  },
  methods: {
    changeNumber(newNumber) {
      EventBus.$emit("number-changed", Number(this.number));
    }
  }
};
</script>