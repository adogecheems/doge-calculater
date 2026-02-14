<template>
    <div class="wrapper">
        <div class="button" :style="{ backgroundColor: color[0] }" @click="$emit('click', expr)">
            <text class="text" :style="{ color: color[1] }">{{ text }}</text>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: { type: String, required: true },
        expr: { type: Object, required: true },
        color: { type: Array, required: true }
    },
}
</script>

<style lang="less" scoped>
.wrapper {
    flex: 1;
}

.button {
    flex: 1;
    margin: 1.5vh;
    border-radius: 5vh;
    justify-content: center;
    align-items: center;
}

.button:active {
    opacity: 0.6;
}

.text {
    font-size: 9vh;
}
</style>