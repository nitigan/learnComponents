<template>
    <div class="bg-cl-danger cl-white dp-flex pd=40px f-s-24px f-w-bold">
        <div class="cs-pointer mg-hrzt-20px">
            <router-link :to="{name:'home'}">
            Home
            </router-link>
        </div>
        <div class="cs-pointer">
            <router-link :to="{name:'about'}">
            About
            </router-link>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>

<style scoped>

</style>
