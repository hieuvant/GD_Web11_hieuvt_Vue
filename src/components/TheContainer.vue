<template>
    <div class="container">
        <TheSidebar></TheSidebar>
        <div class="content">
        <TheHeader></TheHeader>
        <TheMain></TheMain>
        <TheDialog></TheDialog>
    </div>
    </div>
</template>
<script>
import TheSidebar from './TheSidebar.vue';
import TheHeader from './TheHeader.vue';
import TheMain from './TheMain.vue';
import TheDialog from './TheDialog.vue';
export default {
    name:"TheContainer",
    components:{
        TheSidebar, TheHeader, TheMain, TheDialog
    }
}
</script>
<style scoped>

</style>