<template>
  <div class="card">
    <label class="block">
      <span class="form-label mb-2">Select a date</span>
      <input ref="input" class="form-input" type="text" :value="value" />
    </label>
  </div>
</template>

<script>
import Pikaday from "pikaday";
import "pikaday/css/pikaday.css";

export default {
  props: {
    value: {
      required: true,
    },
    options: {
      default: () => {},
    },
  },
  mounted() {
    const picker = new Pikaday({
      field: this.$refs.input,
      onSelect: () => {
        this.$emit("input", picker.toString());
      },
      ...this.options,
    });
  },
};
</script>
