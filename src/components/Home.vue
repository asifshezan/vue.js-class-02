<template>
    <div>
        <p v-html="rowHtml"></p>
        <h2 v-once>{{ name }}</h2>
        <h2 v-if="show">{{ name }}</h2>
        <h2>{{ a+b }}</h2>
        <h2>{{ ok?"Yes":"No" }}</h2>

        <button v-on:click="updatetext">Click Here</button>
        <button v-bind:disabled="disableBtn" v-on:click="updatetext">Click Here</button>
        <!-- <Users />
        <products /> -->
    </div>
</template>
<script>
// import Products from './Products.vue';
// import Users from './Users.vue'


export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name:'Home',
    data(){
        return {
            name:'Asif',
            a:39,
            b:11,
            // eslint-disable-next-line no-undef
            ok:false,
            show:true,
            rowHtml:"<h1>Home Component</h1>",
            disableBtn:true
        }
    },methods: {
        updatetext(){
            this.name="Shezan",
            this.ok=!this.ok,
            this.show=!this.show
        }
    },
//     components:{
//     Users,
//         Products,
//     }
};
</script>

<style scoped>
    div{
        background-color:rgb(218, 137, 232);
        height: 500px;
    }
</style>