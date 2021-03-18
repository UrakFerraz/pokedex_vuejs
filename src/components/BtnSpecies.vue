<template>
    <div class="btn-species">
        <div class="icon bug">
            <img src="../assets/img/icons/bug.svg"/>
        </div>
        <div class="icon dark">
            <img src="../assets/img/icons/dark.svg"/>
        </div>
        <div class="icon dragon">
            <img src="../assets/img/icons/dragon.svg"/>
        </div>

        <div class="icon electric">
            <img src="../assets/img/icons/electric.svg"/>
        </div>
        <div class="icon fairy">
            <img src="../assets/img/icons/fairy.svg"/>
        </div>
        <div class="icon fighting">
            <img src="../assets/img/icons/fighting.svg"/>
        </div>
        <div class="icon fire">
            <img src="../assets/img/icons/fire.svg"/>
        </div>
        <div class="icon flying">
            <img src="../assets/img/icons/flying.svg"/>
        </div>
        <div class="icon ghost">
            <img src="../assets/img/icons/ghost.svg"/>
        </div>
        <div class="icon grass">
            <img src="../assets/img/icons/grass.svg"/>
        </div>
        <div class="icon ground">
            <img src="../assets/img/icons/ground.svg"/>
        </div>
        <div class="icon ice">
            <img src="../assets/img/icons/ice.svg"/>
        </div>
        <div class="icon normal">
            <img src="../assets/img/icons/normal.svg"/>
        </div>
        <div class="icon poison">
            <img src="../assets/img/icons/poison.svg"/>
        </div>
        <div class="icon psychic">
            <img src="../assets/img/icons/psychic.svg"/>
        </div>
        <div class="icon rock">
            <img src="../assets/img/icons/rock.svg"/>
        </div>
        <div class="icon steel">
            <img src="../assets/img/icons/steel.svg"/>
        </div>
        <div class="icon water">
            <img src="../assets/img/icons/water.svg"/>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

.icon {
    border-radius: 100%;
    height: 100px;
    width: 100px;
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