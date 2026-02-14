<template>
    <div class="button" :style="{ backgroundColor: color }" @click="$emit('click')">
        <image class="icon" :src="icon" />
    </div>
</template>

<script>
export default {
    name: 'IconButton',
    props: {
        icon: { type: String, required: true },
        color: { type: String, required: false, default: '#1a1b1f' },
    },
}
</script>

<style lang="less" scoped>
@import '../styles/md-color.less';

.button {
    width: 20vh;
    height: 20vh;
    border-radius: 7vh;
    justify-content: center;
    align-items: center;
}

.button:active {
    opacity: 0.6;
}

.icon {
    width: 60%;
    height: 60%;
}
</style>