<template>
  <h2 class="title">{{ msg }}</h2>
</template>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" src="./style.scss"></style>

<script>
export default {
  name: 'Title',
  data () {
    return {
      msg: 'title'
    }
  },
  created() {
    this.msg = 'hello title';
  }
}
</script>


