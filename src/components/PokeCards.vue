<template>
    <div class="container grid self-center">
        <div class="block flex shadow-6 block-cards" :key="card.name" v-for="card in cards">
            <PokeCard :card="card"/>
        </div>
    </div>
</template>

<script>
import PokeCard from './PokeCard'

    export default {
        name: 'PokeCards',
        props: {
            cards: Array
        },
        components: {
            PokeCard
        }
    }
</script>

<style scoped>
.block {
    background: rgba(255,255,255,.10);
    border-radius: 16px 30px 16px 16px;
    padding: 20px;
    backdrop-filter: blur(20px);
    overflow: hidden;
    min-height: 300px;
    align-self: center;
}

.block-cards::before {
    content: "";
    position: absolute;
    width: 1500px;
    height: 500px;
    left: 50%;
    transform: translateX(-50%);
    top: 200px;
    background-color: rgba(22, 43, 13, 0.3);
    border-radius: 50%;
    filter: blur(30px);
    z-index: -1;
}
.container {
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    grid-gap: 30px;
    width: 90vw;
    max-width: 1150px;
    margin-top: 350px;
}
</style>