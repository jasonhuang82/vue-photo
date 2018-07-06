<template lang="pug">
  #app
    // HelloWorld
    //   h5(slot="title") test
    ul
      li
        router-link(to="/about") about
      li
        router-link(to="/products") products
    router-view
</template>

<script>
import VueRouter from 'vue-router';
import HelloWorld from '@/components/HelloWorld'
import Home from '@/pages/Home';
import About from '@/pages/About';
import Products from '@/pages/Products';
import Member from '@/pages/Member';
import Company from '@/pages/Company';

const NotFound =  {
  template: `<div>404</div>`
}
const AboutHome = {
  template: `<h2>AboutHome</h2>`
}
export default {
  name: 'App',
  router: new VueRouter({
    routes: [
      {path: '/', component: Home},
      {path: '/about', component: About},
      {
        // path: '/products:text', 路由不可有nest路由 
        path: '/products', 
        component: Products,
        children:[
          { path: '', component: AboutHome },
          { path: 'member', component: Member },
          { path: 'company', component: Company }
        ]
      },
      {path: '*', component: NotFound}, // 找不到路徑
    ]
  }),
  components: {
    HelloWorld,About,Home
  }
}
</script>

<style lang="scss" src="./style.scss"></style>