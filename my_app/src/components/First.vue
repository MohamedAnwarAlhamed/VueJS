<template>
    <div v-bind:class="classNname">
        <h1>{{ number }}</h1>
        <input type="text" value="" v-model="number">
        <button @click="inc()">+</button>

        <input type="checkbox" checked="available" v-model="available">
        <p>{{ available }}</p>

        <select name="" id="" v-model="selected">
            <option value="A">A</option>
            <option value="B">B</option>
            <option value="C">C</option>
        </select>
        <span>{{ selected }}</span>


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
            selected: ' ',

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


