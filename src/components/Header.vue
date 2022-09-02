<template>
  <header>
    <h1>{{ title }}</h1>
    <Button />
  </header>
  <p id="joke">What did the piece of bread say to the knife? Butter me up.</p>

  <div class="share">
    <a href=""
      ><i class="fa-brands fa-whatsapp share_icon" id="whatsapp"></i
    ></a>
    <i class="fa-brands fa-instagram share_icon" id="instagram"></i>
    <i class="fa-brands fa-facebook share_icon" id="facebook"></i>

    <img
      width="20px"
      style="padding: 10px"
      height="20px"
      src="./images.png"
      id="snapchat"
    />
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
  grid-template-columns: repeat(4, 100px);
  justify-content: center;
  margin-top: 90px;
}
.share_icon {
  text-align: center;
  padding-bottom: 10px;
  padding-top: 10px;
  width: 50px;
}
#whatsapp:hover {
  color: #fff;
  background-color: #44c052;
  border-radius: 60%;
}
#instagram:hover {
  color: #fff;
  background: linear-gradient(
    148deg,
    rgba(168, 7, 233, 1) 0%,
    rgba(246, 1, 206, 1) 42%,
    rgba(247, 237, 12, 1) 100%
  );
  border-radius: 60%;
}
#facebook:hover {
  color: #fff;
  background-color: #2b71f3;
  border-radius: 60%;
}
#snapchat:hover {
  color: #fff;
  background-color: #fffb00;
  border-radius: 60%;
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
