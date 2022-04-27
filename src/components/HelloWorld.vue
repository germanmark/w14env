<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="printSecret">Click</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    printSecret() {
      // These variables are expected to be in a file called .env.local in the project root folder
      // Any time that these variables change, 'npm run serve' needs to be re-run
      console.log(process.env.VUE_APP_API_KEY);
      console.log(process.env.VUE_APP_API_URL);
      console.log(process.env.VUE_APP_TEST_VAR);
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
