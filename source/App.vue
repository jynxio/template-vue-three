<script setup>
import { ref, onMounted } from "vue";
import initThree from "./threejs/index";

const canvas_ref = ref();

onMounted( _ => initThree( canvas_ref.value ) );
</script>

<template>
    <canvas id="three" ref="canvas_ref"></canvas>
</template>

<style scoped>
canvas#three {
    inline-size: 100vw;
    block-size: 100vh;
    vertical-align: bottom;
}
</style>
