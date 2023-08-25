
<template>
    <AppProducts/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
    
    <pre>
      {{ $store.state.cart }}
    </pre>
    <button @click="updateUser()">atualizar perfil</button>
</template>

<script >
import HelloWorld from './components/HelloWorld.vue'
import AppProducts from './components/Products/AppProducts.vue'

export default {
  name: 'App',
  components: {
    AppProducts
  },

  data() {
    return {

    }
  },

  methods: {
    updateUser() {
      const newUser = {
        first_name: 'Herert',
        last_name: 'Carlos',
        email: 'herbert@herbert.com'
      }
      this.$store.commit('storeUser', newUser)
    }
  },

}
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
