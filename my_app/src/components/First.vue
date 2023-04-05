<template>
    <div v-bind:class="classNname">
        <h1 :class="getStyle()">{{ msgp }}</h1>
        <h1>{{ number }}</h1>
        <h1>{{ skills[2] }}</h1>
        <h1>{{ person.name }}</h1>
        <h1>{{ available }}</h1>
        <h1>{{ msgf }}</h1> 
        <h1>{{ changeMsg() }}</h1>
        <h1>{{ changeNumber() }}</h1>
        <a :href="link">Google</a>
        <Third />
        <button v-on:click="getName()">click</button>
        <!-- <button v-on:click="number++">click2</button> -->
        <button v-on:click="inc()">click2</button>


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
            classNname: 'first',
            link: 'https://www.google.com',

        };
    },
    methods: {
        changeMsg() {
            return  this.msgf = "Hi mohamed anwar first changed";
        },
        changeNumber() {
            // return this.number = 456;
        },
        getStyle(){
            return 'c1';
        },
        getName(){
            console.log("Hi mohamed anwar");
        },
        inc(){
            this.number++;
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
        
<style scoped>
.first {
    background-color: #f00;
}
.c1 {
    color: green;
}
</style>


