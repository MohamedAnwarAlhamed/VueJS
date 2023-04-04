<template>
    <div class="first">
        <h1>{{ msgp }}</h1>
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
    props: {
        msgp: String,
    },
};
</script>
        
<style scoped></style>


