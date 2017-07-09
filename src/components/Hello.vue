<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div id="app-3"><p v-if="seen">You can show me!</p></div>
    <div id="app-4">
      <ol>
        <li v-for="todo in todos">
          {{todo.text}}
        </li>
      </ol>
    </div>
    <div id="app-5">
      <p>{{ message }}</p>
      <button v-on:click="reverseMessage">메세지뒤집기</button>
    </div>
    <div id="app-6">
      <p>{{ message1 }}</p>
      <input v-model="message1">
    </div>
    <div id="app-5"></div>
    <div id="app-5"></div>
    <div id="app-5"></div>
    <div id="app-5"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  methods: {
    reverseMessage() {
      this.message = this.message.split('').reverse().join('');
    },
  },
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      seen: true,
      todos: [
        { text: 'Vue.js' },
        { text: 'Cassandra' },
        { text: 'NGINX' },
      ],
      message: '안녕하세요. Vue.js!',
      message1: '안녕하세요. Vue.js!',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
