<template>
    <div>
<section > 
    <p v-for="(user , i) in users" :key="i" :user_name="user" @click="highlight_username"> {{user}} </p>

</section>
    </div>
</template>

<script>
    export default {
        methods:{
            highlight_username( details ) {
                let username_value = details[`target`].getAttribute(`user_name`)
               this.$root.$emit(`user_clicked` , username_value) 
            }
        },
        data(){
            return{
                users: [`greg` , `paul` , `jack` , `jill`]
            }
        }
    }
</script>

<style scoped>

</style>