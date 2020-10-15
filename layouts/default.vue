<template>
    <section style="display:flex;height:100vh;">
        <b-sidebar
            open
            :fullheight="true"
            position="static"
            mobile="hide"
        >
            <div class="pl-4 pt-4 pr-4 pb-4">
                <b-menu class="is-custom-mobile">
                    <b-menu-list label="Navigation">
                        <b-menu-item active icon="home" label="Home" @click="$router.push('/')"></b-menu-item>
                        <b-menu-item icon="gamepad-variant" label="Play" @click="$router.push('/play')"></b-menu-item>
                        <b-menu-item icon="trophy" label="Leaderboard"></b-menu-item>
                    </b-menu-list>
                    <b-menu-list label="Actions">
                        <b-menu-item icon="login" label="Login"></b-menu-item>
                    </b-menu-list>
                </b-menu>
            </div>
            <!-- <nuxt-link :to="item.to" exact-active-class="is-active">
                <b-icon :icon="item.icon" />
                <span style="margin-left:8px;">{{ item.title }}</span>
            </nuxt-link> -->
        </b-sidebar>
        <nuxt />
    </section>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
            title: 'Home',
            icon: 'home',
            to: { name: 'index' }
        },
        {
            title: 'Inspire',
            icon: 'lightbulb',
            to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>

<style>
    html {
        overflow: auto; 
    }
</style>
