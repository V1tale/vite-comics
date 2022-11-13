<script>
import AppHeader from "./components/AppHeader.vue"
import AppFooter from "./components/AppFooter.vue"
import AppMain from "./components/AppMain.vue"

export default {
    data() {
        return {

        }
    },
    components: {
        AppHeader,
        AppMain,
        AppFooter,
    }
}
</script>

<template>
<AppHeader />
<AppMain />
<AppFooter />
</template>

<style lang="scss">
</style>