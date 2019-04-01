<template>
  <b-card>
    <h2>{{ currentNumber }}</h2>
  </b-card>
</template>

<script>
import { EventBus } from "../event-bus.js";
export default {
  name: "NumberDisplay",
  data() {
    return {
      currentNumber: 0
    };
  },
  created() {
    EventBus.$on("number-changed", number => {
      this.currentNumber = number;
    });
  }
};
</script>