<template lang="pug">
  div
    h2.Products hello {{ msg }}
    ul
      li
        router-link(to="/products/member") member
      li
        router-link(to="/products/company") company 
    router-view
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="./style.scss"></style>

<script>
export default {
  name: 'Products',
  data () {
    return {
      msg: 'Products'
    }
  },
  created() {
    // console.log('this.$route',this.$route);
    
    // this.msg = this.$route.params.text? this.$route.params.text:'Products';
  }
}
</script>


