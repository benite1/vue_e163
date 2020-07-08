<template>
  <div>
    <h2>Hello {{ name }}</h2>
    <h2>age {{ age }}</h2>
    <input type="text" :value="name">
    <input type="text" :v-model="name">
    <div><button @click="dosave">SAVE</button></div>
    <div><button @click="domenu">MAIN MENU</button></div>
    <div><button @click="dohome">HOME</button></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: 'Orasa Kartsanit',
      age: 20,
    }
  },
  methods: {
    dosave() {
      console.log('DO SAVE')
    },
    domenu() {
      this.$router.push('/activity/menu')  
    },
    dohome() {
      this.$router.push('/')
    },
  }
}
</script>
