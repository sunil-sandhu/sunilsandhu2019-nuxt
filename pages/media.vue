<template>
  <div>


    <div class="text-container">

    <div v-for="item in media">
      <p class="format">{{item.format}}</p>
      <a class="title" :href="item.link" target="_blank">{{item.title}}</a>
      <p class="medium">{{item.medium}}</p>
      <p class="year">{{item.year}}</p>
    </div>



    </div>


  </div>
</template>


<script>
    export default {
        data() {
            return {
                color: 'blue',
                media: [
                    {
                        format: 'article',
                        title: 'the 2019 web developer roadmap',
                        medium: 'medium',
                        link: 'https://medium.com/@sunilsandhu/the-web-developer-roadmap-for-2019-692cb02d36a4'
                    },
                ]
            }
        },

        components: {

        },

        methods: {
        }

    }


</script>

<style scoped>

.title {
  font-size: 1.5em;
  color: #646464;
  word-spacing: -0.04em;
}

.format {
  margin-top: 30px;
  font-size: 1em;
  color: #C3BFBF;
}

.medium {
  font-size: 1.25em;
  color: #9D9D9D;

}

</style>
