<script>
  export default {
    name: 'App',
    data() {
      return{
        message: 'Cuso',
        content: 'lorem ipsum dolor',

        name:'',
        lastname:'',

        count: 0,

        image: 'https://picsum.photos/300/300'
      }
    },
    methods: {
      firstFunct(){
        console.log('Cliccato');
        this.secondFunct()
      },
      secondFunct(){
        console.log('secondFunct');
      }
    }
  }
</script>

<template>
  <div>
    <h1>Hello {{ message }}</h1>
    <p>{{ content }}</p> 
    
    <label for="name">first name</label>
    <input type="text" v-model="name">

    <label for="name"> lastname</label>
    <input type="text" v-model="lastname">

    <p>Buongiorno {{ name + ' ' + lastname }}</p>
    <p>Buongiorno {{ name }} {{ lastname }}</p>
    <p>{{'Buongiorno ' + name }} {{ lastname }}</p>

    <button @click="count++">Click</button>
    {{ count }}

    <div>
      <img :src="image" alt="Lorem Picture">
    </div>

    <div>
      <img src="/vite.svg" alt="Lorem Picture" style="margin-right: 2rem;">
      <img src="./assets/vue.svg" alt="Lorem Picture">
    </div>

  </div>  
</template>

<style>
</style>
