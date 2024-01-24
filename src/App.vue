<script>
  export default {
    name: 'App',
    data() {
      return{
        message: 'CusoMat',
        content: 'lorem ipsum dolor',

        name:'',
        lastname:'',

        count: 0,
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
  </div>  
</template>

<style>
</style>
