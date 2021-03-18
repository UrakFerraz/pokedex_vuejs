<template>
    <transition name="fadeInfos">
        <div v-if="showInfo" class="flex" data-state="column">
            <div class="flex row-items-align-center poke-types-wrapper row-wrap">
                <p class="type-text">Tipos:</p>
                <div class="poke-types row-items-align-center flex" :key="info.slot" v-for="info in infos.types">
                    <div :class="`icon ${info.type.name}`">
                        <img :src="`../assets/img/icons/${info.type.name}.svg`">
                    </div>
                    <p class="type-text">{{ info.type.name }}</p>
                </div>
            </div>
            <div class="flex poke-abilities"  data-state="column">
                <div class="poke-ability" :key="stat.stat.name" v-for="stat in infos.stats">
                    <div class="line">
                        <div class="line-porcentage" :style="`width: ${stat.base_stat}%`"></div>
                    </div>
                    <div class="flex stats">
                        <p>{{ stat.stat.name }}</p>
                        <p>{{ stat.base_stat }}</p>
                    </div>
                </div>
            </div>
        </div>
    </transition>
</template>

<script>
    export default {
       props: {
            infos: Object,
            showInfo: {
                    type: Boolean,
                    required: false
                }
       } 
    }
</script>

<style scoped>

.poke-ability {
    margin: 10px 0;
}

.poke-types {
    gap: 5px;
}

.poke-types-wrapper {
    background: rgba(255,255,255,.1);
    padding: 6px;
    margin-bottom: 6px;
    gap: 15px;
    border-radius: 10px;
}

.type-text {
    text-transform: capitalize;
    color: white;
}

.stats p {
    font-weight: var(--fw-500);
    color: white;
}

.stats p:first-child {
    flex:1;
    text-transform: capitalize;
}

.line {
    width: 100%;
    height: 6px;
    background-color: rgba(255,255,255,.1);
    margin-bottom: 3px;
    overflow: hidden;
    border-radius: 6px;
}

.line-porcentage {
    position: absolute;
    left: 0;
    top: 0;
    height: 6px;
    background-color: #fff;
}







.fadeInfos-enter-active, .fadeInfos-leave-active {
    transition: all .5s ease;
}

.fadeInfos-enter-from, .fadeInfos-leave-to {
    opacity: 0;
}









.icon {
    border-radius: 100%;
    height: 30px;
    width: 30px;
    margin:auto;
    transition: 200ms all;
}

.icon:hover{
    filter: saturate(200%);
    transform: scale(1.1);
    cursor: pointer;
}

.icon img {
    height: 60%;
    width: 60%;
    margin: 20%;
}

.bug {
    background: #92BC2C;
    box-shadow: 0 0 20px #92BC2C;
}

.dark {
    background: #595761;
    box-shadow: 0 0 20px #595761;
}

.dragon {
    background: #0C69C8;
    box-shadow: 0 0 20px #0C69C8;
}

.electric {
    background: #F2D94E;
    box-shadow: 0 0 20px #F2D94E;
}

.fire {
    background: #FBA54C;
    box-shadow: 0 0 20px #FBA54C;
}

.fairy {
    background: #EE90E6;
    box-shadow: 0 0 20px #EE90E6;
}

.fighting {
    background: #D3425F;
    box-shadow: 0 0 20px #D3425F;
}

.flying {
    background: #A1BBEC;
    box-shadow: 0 0 20px #A1BBEC;
}

.ghost {
    background: #5F6DBC;
    box-shadow: 0 0 20px #5F6DBC;
}

.grass {
    background: #5FBD58;
    box-shadow: 0 0 20px #5FBD58;
}

.ground {
    background: #DA7C4D;
    box-shadow: 0 0 20px #DA7C4D;
}

.ice {
    background: #75D0C1;
    box-shadow: 0 0 20px #75D0C1;
}

.normal {
    background: #A0A29F;
    box-shadow: 0 0 20px #A0A29F;
}

.poison {
    background: #B763CF;
    box-shadow: 0 0 20px #B763CF;
}

.psychic {
    background: #FA8581;
    box-shadow: 0 0 20px #FA8581;
}

.rock {
    background: #C9BB8A;
    box-shadow: 0 0 20px #C9BB8A;
}

.steel {
    background: #5695A3;
    box-shadow: 0 0 20px #5695A3;
}

.water {
    background: #539DDF;
    box-shadow: 0 0 20px #539DDF;
}
</style>