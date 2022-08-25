<template>
  <header>
    <h1>{{ title }}</h1>
    <Button />
  </header>
  <p id="joke">
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Corporis quis
    incidunt aperiam
  </p>

  <div class="share">
    <i class="fa-brands fa-whatsapp"></i>
    <i class="fa-brands fa-instagram"></i>
    <i class="fa-brands fa-facebook"></i>
    <i class="fa-brands fa-snapchat"></i>
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: String,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
.share {
  display: grid;
  grid-template-columns: repeat(4, 10vw);
  justify-content: center;
  padding-left: 100px;
  margin-top: 90px;
}
@media (max-width: 420px) {
  .share {
    padding-left: 32px;
  }
  header {
    display: block;
  }
}
</style>
