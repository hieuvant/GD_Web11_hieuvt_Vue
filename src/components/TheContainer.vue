<template>
    <div class="container">
        <TheSidebar></TheSidebar>
        <div class="content">
        <TheHeader></TheHeader>
        <TheMain></TheMain>
    </div>
    </div>
</template>
<script>
import TheSidebar from './TheSidebar.vue';
import TheHeader from './TheHeader.vue';
import TheMain from './TheMain.vue';
export default {
    name:"TheContainer",
    components:{
        TheSidebar, TheHeader, TheMain
    }
}
</script>
<style scoped>

</style>