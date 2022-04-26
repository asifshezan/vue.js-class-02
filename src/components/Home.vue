<template>
    <div>
        <h1>Home Component</h1>
        <Users />
        <products />
    </div>
</template>
<script>
import Products from './Products.vue';
import Users from './Users.vue'


export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name:'Home',
    components:{
    Users,
        Products,
    }
};
</script>

<style scoped>
    div{
        background-color:rgb(218, 137, 232);
        height: 500px;
    }
</style>