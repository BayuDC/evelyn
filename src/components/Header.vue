<script>
import HeaderDefault from './HeaderDefault.vue';
import HeaderOverlay from './HeaderOverlay.vue';

export default {
    name: 'Header',
    data() {
        return {
            overlay: false,
        };
    },
    components: {
        HeaderDefault,
        HeaderOverlay,
    },
};
</script>

<template>
    <HeaderDefault @toggle="() => (overlay = true)" />
    <HeaderOverlay @toggle="() => (overlay = false)" :render="overlay" />
</template>
