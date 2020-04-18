<template>
  <div class="navigation">
    <nuxt-link to="/" class="big">home</nuxt-link>
    <nuxt-link to="/about" class="big">about</nuxt-link>
    <nuxt-link to="/media" class="big">media</nuxt-link>
  </div>
</template>

<script>
export default {
  name: "Navigation",
  components: {},
  data() {
    return {};
  },
  props: ["linkColor", "navBackgroundColor"]
};
</script>

<style scoped>
.navigation {
  height: 60px;
  position: absolute;
  left: 100px;
  top: 20px;
  transition: all 300ms;
  z-index: 2;
}

.navigation a {
  margin-right: 20px;
  font-size: 18px;
}

/*@media only screen and (max-width: 599px) {*/
/*.navigation {*/
/*padding-left: 10px;*/
/*!*background-color: ;*!*/
/*height: 50px;*/
/*!*border-bottom: 1px solid grey;*!*/
/*!*box-shadow: 0px 1px 5px rgba(128, 128, 128, 0.2);*!*/
/*width: 100%;*/
/*!*position: fixed;*!*/
/*!*z-index: 2;*!*/
/*!*background-color: white;*!*/
/*}*/

/*.navigation a {*/
/*padding-top: 18px;*/
/*}*/

/*}*/
</style>
