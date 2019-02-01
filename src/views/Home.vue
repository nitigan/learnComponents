<template>
  <div class="home t-al-center">
    <h1 class="f-s-36px f-w-bold">Home Page</h1>
    <DisplayGif :gifData="result.data" />
  </div>
</template>

<script>
import axios from 'axios'
import DisplayGif from '@/components/DisplayGif.vue'

export default {
  name: 'home',
  components:{
    DisplayGif
  },
  data (){
    return{
      result: {
        data:{
          data:[]
        }
      },
      apiKey: 'kr1gdiV4ylqXRl14v4HuuyLpyMHtUx2f',
      search: 'lisa blackpink'
    }
  },
  async mounted(){
    this.result = await axios.get('https://api.giphy.com/v1/gifs/search?api_key='+ this.apiKey +'&q='+ this.search+'&limit=100&offset=0&rating=G&lang=en')
      console.log('result',this.result)
  }
}
</script>
