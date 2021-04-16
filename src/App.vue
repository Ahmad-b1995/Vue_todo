<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <input class="input" ref="input" @change="add_to_list" type="text" />
    <ul class="list">
      <template v-for="(item, index) in list">
        <input
          type="checkbox"
          id="item"
          :name="item"
          :value="item"
          :key="index"
        />
        <label :class="strike_through" for="vehicle1" :key="`label${index}`">
          {{ item }}</label
        >
        
        <br :key="`br${index}`" />
      </template>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      list: [],
    };
  },
  methods: {
    add_to_list: function (event) {
      this.list.push(event.target.value);
      this.$refs.input.value = "";
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
.input {
  margin: 50px auto;
  display: block;
}

.list {
  width: 150px;
  margin: 20px auto;
  text-align: left;
}

.strike_through {
  text-decoration: line-through;
}
</style>
