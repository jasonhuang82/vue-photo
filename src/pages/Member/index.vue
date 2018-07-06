<template lang="pug">
  h3 Member
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="./style.scss"></style>

<script>
  export default {
    data() {
      return{
        msg: 'hihi'
      }
    },
    created(){
      console.log('this.$route',this.$route);
    }
  }
</script>
