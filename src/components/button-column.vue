<template>
    <div class="wrapper" @click="$emit('click')">
        <slot />
    </div>
</template>

<style lang="less" scoped>
.wrapper {
    min-width: 33vh;
    height: 100vh;
    padding: 7vh 12vh 0 5vh;
    flex-direction: column;
    justify-content: space-between;
}
</style>

<script>
export default {
    name: 'ButtonColumn',
}
</script>