<template>
    <div class="card flex" data-state="column">
        <div class="card-poke-svg-wrapper flex align-center">
            <img class="poke-svg" :src="card.sprites.other.dream_world.front_default" alt="">
        </div>
        <p class="title">{{ card.name }}</p>
        <button class="poke-plus-btn" @click="show = !show">
            <img src="../assets/img/plus.svg" alt="">
        </button>
        <PokeCardInfos :showInfo="show" :infos="card"/>
    </div>
</template>

<script>
import PokeCardInfos from './PokeCardInfos'
    export default {
        data() {
            return {
                show: false,
            }
        },
        props: {
            card: Object,
        },
        methods: {
            maisInfo() {
                this.show = !this.show
                this.$emit('mais-info', this.show);
                console.log(this.show);
            }
        },
        components: {
            PokeCardInfos
        }
    }
</script>

<style scoped>
.card {
    flex: 1;

}

.card-poke-svg-wrapper {
    width: 200px;
    height: 180px;
    place-self: center;
    flex: 1;
}

.poke-svg {
    width: 100%;
    height: 100%;
    object-fit: contain;
    filter: drop-shadow(0 10px 20px rgba(9, 9, 19, 0.7));
}
.poke-plus-btn {
    position: absolute;
    top: 0;
    right: 0;
}

.poke-plus-btn img {
    width: 30px;
    height: 30px;
    filter: drop-shadow(0 5px 6px rgba(0,0,0,.4));
}

.title {
    font-family: var(--fontBlack);
    font-size: 2em;
    text-transform: capitalize;
    text-align: center;
    margin: 20px 0;
}
</style>