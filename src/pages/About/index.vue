<template>
  <h2 class="About">{{ msg }}</h2>
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="./style.scss"></style>

<script>
export default {
  name: 'About',
  data () {
    return {
      msg: 'About'
    }
  },
  created() {
    this.msg = 'hello About';
  }
}
</script>


