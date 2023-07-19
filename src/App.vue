<template>
  <h1> {{ title }} </h1>
  <Modal v-if="showModal" :theme="theme" @triggerclose="toggleModal" >
    <template v-slot:links>
      <a href="#" @click="toggleModal">Close The Modal</a>
      <br><br><br>
      <a href="#">Sign Up</a>
      <a href="#">More Info</a>
    </template>

    <h1 class=""> Judulnya</h1>
    <p>Content nya adalah sebagai berikut Loream ipsum dolor ismet</p>
    <br>
  </Modal>
  <br>
  <input type="text" ref="tulisan" v-model="theme">
  <button @click="toggleModal">Submit</button>
  <p>Tema hanya ada (normal,dark) dan Anda telah memilih tema : {{ theme }} </p>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components:{ Modal },
  data(){
    return {
      title:"My First Vue Application :)",
      theme:"normal",
      showModal:false
    }
  },
  methods:{
    toggleModal(){
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
#app , .modals{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  border-bottom: 1px solid #534949;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
