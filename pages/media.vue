<template>
  <div>


    <div class="text-container">

    <div v-for="item in media" :key="item.id">
      <p class="format">{{item.format}}</p>
      <a class="title" :href="item.href" target="_blank">{{item.title}}</a>
      <p class="medium">{{item.medium}}</p>
      <p class="year">{{item.year}}</p>
    </div>



    </div>


  </div>
</template>


<script>
  import axios from 'axios';


    export default {
        data() {
            return {
                color: 'blue',
            }
        },

        async asyncData() {
            const res = await axios.get('https://sunilsandhu-47c54.firebaseio.com/media.json');
            const media = res.data;
            return {media};

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

.year {
  color: #553b3b;
  font-size: 0.9em;
}

</style>
