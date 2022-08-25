<template>
  <button @click="onClick" class="btn">Click Me!</button>
</template>

<script>
// import { get } from "http";

export default {
  name: "Button",
  methods: {
    async onClick() {
      let a = await fetch("https://icanhazdadjoke.com/", {
        headers: {
          Accept: "application/json",
        },
      });
      let b = await a.json();
      document.getElementById("joke").innerHTML = b.joke;
      confirm
    },
  },
};
</script>
