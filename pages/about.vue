<template>
  <div class="content">
    <h1 class="name">About</h1>

    <p>
      I am a
      <strong>digital creator</strong>, located at the intersection between Software Development, User Experience, and Interface Design. I am the
      <strong>Founder and Editor</strong> of
      <strong>
        <a href="https://plainenglish.io">Plain English</a>
      </strong>. I work on
      <strong>open-source</strong> projects,
      <strong>teach</strong> people how to code, and
      <strong>speak</strong> about the things that I know.
    </p>

    <nuxt-link to="/media" class="button">Media</nuxt-link>
  </div>
</template>

<script>
export default {
  components: {}
};
</script>

<style scoped>
h2,
h3,
h4,
h5,
p {
  font-size: 1.3em;
  margin: 5px 0;
  text-align: left;
  color: #646464;
  word-spacing: -0.04em;
  line-height: 1.3em;
}

@media only screen and (max-width: 599px) {
  h2,
  h3,
  h4,
  h5,
  p {
    font-size: 1.2em;
    margin: 5px 0;
    text-align: left;
    color: #646464;
    word-spacing: -0.04em;
    line-height: 1.4em;
  }
}
</style>
