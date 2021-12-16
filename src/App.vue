<template>
    String: {{ someString }} <br />
    Object: {{ someObject }} <br />

    <Child
        :someObject="someObject"
        :someString="someString"
    />
</template>

<script setup>
import Child from './components/Child.vue';
import {ref} from 'vue';

const someString = ref('test');

const someObject = ref({s: 'test'});
</script>
