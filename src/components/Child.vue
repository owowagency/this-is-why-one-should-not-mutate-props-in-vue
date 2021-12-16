<template>
    String: <input v-model="s" />
    Object: <input v-model="o.s" />
</template>

<script setup>
import {defineProps, toRef, watchEffect} from 'vue';

const props = defineProps({
    someString: {
        type: String,
        required: true,
    },
    someObject: {
        type: Object,
        required: true,
    },
});

const s = toRef(props, 'someString');

const o = toRef(props, 'someObject');

watchEffect(() => console.log(s.value));
watchEffect(() => console.log(o.value));
</script>
