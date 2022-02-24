<template>
    <div class="container MyMain">
        <div class="row">
            <div class="col" v-for="(disco, index) in listaDischi" :key="index">
                <img :src="disco.poster">
                <h2>{{disco.title}}</h2>
                <div>{{disco.author}}</div>
                <div>{{disco.year}}</div>
            
            </div>
        </div>
    </div>
</template>

<script>

const axios = require('axios');

export default {
    name: 'MyMain',
    data() {
        return {
            listaDischi: [],
        }
    },
    methods: {
        getDischi() {
                // Make a request for a user with a given ID
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.listaDischi = response.data.response;
                console.log(this.listaDischi);
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
            .then(function () {
                // always executed
            });
        }
    },

    mounted() {
        this.getDischi();
    }


}
</script>

<style scoped>
    .MyMain {
        background-color: blue;
    }
</style>