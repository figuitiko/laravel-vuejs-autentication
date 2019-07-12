<template>
    <div id="main">
        <header id="header">
            <h1>
                <router-link :to="{name: 'home'}">
                    Laravel Vue SPA
                </router-link>
            </h1>
            <navigationMenu></navigationMenu>
        </header>
        <transition name="fade">
        <div id="content">

                <router-view></router-view>

        </div>
        </transition>
    </div>
</template>
<script>
    import navigationMenu from './components/Menu.vue'
    export default {
        mounted(){
            console.log(this.$auth.user().email );
        },
        data() {
            return {

//

            }
        },
        components: {
            navigationMenu
        }
    }
</script>