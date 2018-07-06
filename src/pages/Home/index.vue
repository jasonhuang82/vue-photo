<template>
  <h2 class="Home">{{ msg }}</h2>
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="./style.scss"></style>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Home'
    }
  },
  created() {
    this.msg = 'hello Home';
  }
}
</script>


