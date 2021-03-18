<template>
    <div class="search-bar flex align-center row-items-align-center">
        <input type="text" v-model="searchString" placeholder="Busca" class="flex row-items-align-center search-bar-input-field">
        <button class="searchBtnSubmitIcon"></button>
    </div>
</template>

<script>
    export default {
        name: 'SearchBar',
        data() {
            return {
                searchString: ''
            }
        }
    }
</script>

<style scoped>
.search-bar {
    gap: 10px;
    margin: 40px 0;
}
.search-bar-input-field {
    flex: 1;
    border: 2px solid white;
    border-radius: 10px;
    background-color: white;
    font-size: 20px;
    padding: 8px;
    width: 100%;
    max-width: 300px;
    /* height: 37px; */
}

.searchBtnSubmitIcon {
    width: 44px;
    height: 44px;
    border-radius: 10px;
    padding: 6px;
    background-color: #fff;
}
</style>