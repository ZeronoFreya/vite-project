<template lang="pug">
.container {{msg}}
</template>

<script setup name="HelloWorld">
import { defineProps, useContext } from "vue";

const props = defineProps({
    msg: {
        type: String,
        default: "",
    },
});

const { expose, emit } = useContext();

const demo = () => {
    console.log("demo");
};
expose({
    demo,
});
</script>

<style lang="scss" scoped>
.container {
    width: 100%;
    height: 100%;
}
</style>
