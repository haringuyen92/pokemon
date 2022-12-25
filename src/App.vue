<template>
  <MainScreen
    v-if="screen === 'default'"
    @onStartGame="onStartGame($event)"
  ></MainScreen>
  <InteractScreen v-if="screen === 'play'">></InteractScreen>
</template>

<script>
import MainScreen from "@/components/MainScreen.vue";
import InteractScreen from "@/components/InteractScreen.vue";

export default {
  name: "App",
  components: { InteractScreen, MainScreen },
  data() {
    return {
      screen: "default",
    };
  },
  methods: {
    onStartGame(config) {
      this.screen = "play";
      console.log(config);
    },
  },
};
</script>
