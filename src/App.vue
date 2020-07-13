<template>
  <div id="app">
    <input type="file" @change="onUploadImg">
    <img width=500 :src="img" />
  </div>
</template>

<script>
import {uploadImg} from './services/imgUpload.service.js'
export default {
  data(){
    return {
      img: ''
    }
  },
  methods:{
  async onUploadImg(ev){
      uploadImg(ev) 
      let img = await res.url
      this.img = res.url

    }
  }

 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
