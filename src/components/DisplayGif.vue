<template>
    <div>
        <div v-for="(gif, index) in gifData.data" :key="index">
            <img :src="gif.images.original.url" alt="" class="w-30pct"><br>
            {{gif.title}} <br>
        </div>
    </div>
</template>

<script>
export default {
    props: ['gifData']
}
</script>

<style scoped>

</style>
