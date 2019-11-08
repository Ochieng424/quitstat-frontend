<template>
  <div>
    <Nav/>
    <nuxt />
    <Footer/>
  </div>
</template>
<script>
  import Nav from '@/components/Nav';
  import Footer from '@/components/Footer';

  export default {
    components:{
      Nav,
      Footer
    }
  }
</script>
<style>

</style>
