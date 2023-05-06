<template>
    <div class="container ">
        <div class="text-center"><h2>this is vue template</h2></div>
    </div>
    <div class="container text-center">
      <h1>{{ user_prop_name }} Counter: {{ counter }}</h1>
      <button @click="incrementCounter">Increment</button>
      <button @click="decrementCounter">Decrement</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ['initialCounter','user_name'],
    data() {
      return {
        counter: 0,
        // counter: this.initialCounter || 0,
        // user_prop_name: 'this',
        user_prop_name : this.user_name
      };
    },
    methods: {
      incrementCounter() {
        this.counter++;
        console.log(this.kuch_b);
      },
      decrementCounter() {
        this.counter--;
      },
    },
    computed: {
      kuch_b() {
        // console.log('this is compted');
      return 'kuch b';
      }
    }
  };
  </script>
  