<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <input class="input" type="text">
  </div>
</template>

<script>
export default {
  name: "App",
  date(){
    return{
      list:[]
    }
  },
  methods:{
    add_to_list:{

    }
  }
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
.input{
  margin: 50px auto;
display: block;
}
</style>
