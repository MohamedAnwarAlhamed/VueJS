<template>
    <div class="first">
        <h1>{{ msgf }}</h1> 
        <Third />
    </div>
</template>
        
<script>
import Third from './Third.vue';
export default {
    name: 'First',
    data() {
        return {
            msgf: "Hi mohamed anwar first",
        };
    },
    components: {
        Third,
    },
};
</script>
        
<style scoped></style>


