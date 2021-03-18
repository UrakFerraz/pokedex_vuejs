<template>
    <Header msg="Pokedex"/>
<div class="wrapper">
    <PokeCards :cards="lista"/>
</div>

</template>

<script>
import './assets/global.css'
import Header from './components/Header'
import PokeCards from './components/PokeCards'

export default {
  name: 'App',
  components: {
    Header,
    PokeCards
  },
  data() {
    return {
      apiUrl: 'https://pokeapi.co/api/v2/pokemon/',
      lista: []
    }
  },
  methods: {
    async fetchData(num) {
      try {
        const resposta = await fetch(`${this.apiUrl}${num}`)
        .then(res => {
          if(!res.ok) {
            return console.log('falho na resposta - index:', num, res);
          }
          return res.json()
        })
        return resposta
      } catch (e) {
        console.log('erro', e);
      }
    },
    async fetchRange(inicial, quant) {
      const arr = [];
      for(let i = inicial; i <= (inicial + quant); i++) {
        arr.push(this.fetchData(i));
      }
      const resp = await Promise.all(arr)
      .then(res => {
        console.log();
        return res;
      })
      .then(res => {
        return res;
      })
      return resp.filter(el => {
        return el != undefined
      })
    }
  },
  async created() {
    this.lista = await this.fetchRange(1,99)
    // console.log(this.lista);
  }
}
</script>

<style scoped>
.wrapper {
  background-image: url('./assets/img/bg2.jpg');
  background-size: cover;
  background-attachment: fixed;
  padding-bottom: 300px;
}
</style>
