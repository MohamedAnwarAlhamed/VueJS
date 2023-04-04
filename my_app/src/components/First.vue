<template>
    <div class="first">
        <h1>{{ msgp }}</h1>
        <h1>{{ number }}</h1>
        <h1>{{ skills[2] }}</h1>
        <h1>{{ person.name }}</h1>
        <h1>{{ available }}</h1>
        <h1>{{ msgf }}</h1> 
        <h1>{{ changeMsg() }}</h1>
        <h1>{{ changeNumber() }}</h1>
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
            number: 123,
            skills: ['html', 'css', 'js'],
            person: {
                name: 'mohamed',
                age: 25,
            },
            available: true,

        };
    },
    methods: {
        changeMsg() {
            return  this.msgf = "Hi mohamed anwar first changed";
        },
        changeNumber() {
            return this.number = 456;
        },
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


