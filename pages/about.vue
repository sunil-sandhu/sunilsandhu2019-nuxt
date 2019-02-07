<template>
    <div class="content">

        <h1 class="name">about</h1>

        <p>i am a <strong>digital creator</strong>, located at the intersection between full-stack development, user experience, and interface design. i am the <strong>editor of javascript in plain english</strong>. i am currently working as <strong>a full-stack developer</strong> for a behavioural psychology-led research and design agency in the uk.</p>

        <nuxt-link to="/media" class="button">media</nuxt-link>

    </div>
</template>

<script>


    export default {
        components: {
        }
    }
</script>

<style scoped>

  h2, h3, h4, h5, p {
    font-size: 1.3em;
    margin: 5px 0;
    text-align: left;
    color: #646464;
    word-spacing: -0.04em;
    line-height: 1.3em;
  }


  @media only screen and (max-width: 599px) {
      h2, h3, h4, h5, p {
          font-size: 1.2em;
          margin: 5px 0;
          text-align: left;
          color: #646464;
          word-spacing: -0.04em;
          line-height: 1.4em;
      }

  }

</style>
