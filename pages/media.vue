<template>
  <div class="content">

    <nuxt-link to="/">back</nuxt-link>

    <div class="text-container">
    <h2>i am a digital creator, working at the intersection between front and back-end development, ux, and human-centred design.
    </h2>
    <h3>
      i am the editor of javascript in plain english, a publication that focuses on making javascript more accessible.
    </h3>
    <h4>
      i currently work as a full-stack developer for instinct laboratory, a behavioural psychology-led design agency in the uk.
    </h4>
    </div>


  </div>
</template>


<script>
    export default {
        data() {
            return {
                color: 'blue',
            }
        },

        components: {

        },

        methods: {
        }

    }


</script>

<style scoped>


h2, h3, h4 {
  font-size: 1.3em;
  margin: 15px 0;
  font-weight: 300;
  text-align: left;
}

</style>
