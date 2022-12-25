<template>
  <div>
    <button @click="onStartGame(16)">
      <p>4x4</p>
      <p>easy</p>
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    onStartGame(type) {
      this.$emit("onStartGame", { type });
    },
  },
};
</script>
