<template>
    <div id="app">
        <ch-header></ch-header>
        <main id="main-content">
            <transition
                mode="out-in"
                name="fade"
            >
                <router-view></router-view>
            </transition>
        </main>
        <ch-footer></ch-footer>
    </div>
</template>

<script>

import ChHeader from './partials/Header.vue'
import ChFooter from './partials/Footer.vue'

export default {
    components: {
        ChHeader,
        ChFooter
    }
}

</script>

<style lang="scss">

// https://bulma.io/documentation/overview/customize/
@import "../node_modules/bulma/sass/utilities/initial-variables.sass";
@import "../node_modules/bulma/sass/utilities/functions.sass";

// Theme Variables
@import "./scss/theme";

// Transitions
@import "./scss/transitions";

// Import the rest of Bulma
@import "../node_modules/bulma/bulma.sass";

// Font Awesome
@import "../node_modules/font-awesome/css/font-awesome.css";

// Page styling
html,
body,
#app {
    height: 100%;
}

#app {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

</style>
