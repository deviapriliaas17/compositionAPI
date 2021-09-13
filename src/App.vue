<template>
  <section class="container">
    <h2>{{ user.name }}</h2>
    <h3>{{ user.age }}</h3>
  </section>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup(){
    // const uName = ref('Devi')
    // const uAge  = ref(22)

    const user = reactive({
      name:'Devi',
      age:22
    })

    setTimeout(() =>{
      // uName.value = 'Devi Aprilia Ayu Santoso';
      // uAge.value  = '23'
      user.name = 'Devi Aprilia Ayu Santoso',
      user.age  = 23
    },2000)

    return{
      user    :user
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>