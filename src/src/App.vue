<template>
  <section>
    <Navbar/>
    <Form/>
  </section>
</template>

<script>
import Navbar from "./components/friend-nav.vue"
import Form from "./components/friend-form.vue"
export default {
  components: {
    Navbar,
    Form
  }
}
</script>

<style>
#app {
  font-family: sans-serif;
  width:50%;
  margin:auto;
  padding:10px;
  text-align:center;
  border-radius:8px;
  border: red solid 2px;
  border-style: dashed ;
}
</style>
