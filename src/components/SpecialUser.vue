<template>
  <div>
    <p>Special Uer :</p>
    <p>{{ special }}</p>
    <p>has Logged In</p>
  </div>
</template>

<script>
export default {
    data (){
        return{
            special: undefined
        }
    },
  methods: {
    show_user(post) {
      this.special = post
    },
  },
  mounted ( ) {
    this.$root.$on(`user_clicked` , this.show_user)
  }
};
</script>

<style scoped>
</style>