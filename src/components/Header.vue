<template>
<transition name="scrollNavBar">
    <div v-if="showNavbar" class="header flex align-center" data-state="column" ref="header">
        <img src="../assets/img/logo.svg" alt="">
        <!-- <h1>{{ msg }}</h1> -->
        <!-- <SearchBar /> -->
    </div>
</transition>
</template>

<script>
// import SearchBar from './SearchBar'
    export default {
        name: 'Header',
        data() {
            return {
                screenScroll: false,
                title: '',
                showNavbar: true,
                lastScrollPosition: 0
            }
        },
        props: {
            msg: String
        },
        mounted () {
        window.addEventListener('scroll', this.onScroll)
        },
        beforeUnmount () {
        window.removeEventListener('scroll', this.onScroll)
        },
        components: {
            // SearchBar
        },
        methods: {
            onScroll () {
                // Get the current scroll position
                const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop
                // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
                if (currentScrollPosition < 0) {
                return
                }
                // Here we determine whether we need to show or hide the navbar
                this.showNavbar = currentScrollPosition < this.lastScrollPosition
                // Set the current scroll position as the last scroll position
                this.lastScrollPosition = currentScrollPosition
            },
            handleScroll: function() {
                console.log('el');
            }
        }
    }
</script>

<style scoped>
    .header {
        margin-top: 30px;
        width: 90vw;
        flex-grow: 1;
        max-width: 1150px;
        position: fixed;
        z-index: 3;
        left: 50%;
        top: 0;
        transform: translateX(-50%);
        transition: 0.5 ease-in-out all;
    }

    /* .navbar-hidden {
        top: -350px;
        transition: 0.5 ease-in-out all;
    } */
    .scrollNavBar-enter-active, .scrollNavBar-leave-active {
    transition: opacity .5s ease;
    }

    .scrollNavBar-enter-from, .scrollNavBar-leave-to {
    opacity: 0;
    }
    h1 {
        font-size: 30px;
        color: white;
        text-align: center;
        font-weight: var(--fw-500);
    }

    img {
        width: 70vw;
        height: auto;
        max-width: 400px;
        align-self: center;
        filter: drop-shadow(0 10px 20px white);
    }
</style>