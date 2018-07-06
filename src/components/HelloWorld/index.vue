<template>
  <div class="hello">
    <h1>Hello {{msg}}</h1>
  </div>
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="./style.scss" scoped></style>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: ''
    }
  },
  created() {
    this.msg = this.$route.params.text? this.$route.params.text : 'index';
  },
  props: ['testComp']
}
</script>


