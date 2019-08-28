# Handling-User-Input

HTML:
<html>

  <head>
    <link rel="stylesheet" href="index.css">
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  </head>

  <body>

    <div id="yee">
      <p>{{ message }}</p>
      <button v-on:click="reverseMessage">Reverse Message</button>
    </div>
    <div id="yeet">
      <p>{{ message }}</p>
      <input v-model="message">
    </div>
    <script src="index.js"></script>
  </body>

</html>

JavaScript/Vue
var yee = new Vue({
  el: '#yee',
  data: {
    message: 'HELLO WORLD'
  },
  methods: {
    reverseMessage: function() {
      this.message = this.message.split('').reverse().join('')
    }
  }
})

var yeet = new Vue({
  el: '#yeet',
  data: {
    message: 'WELCOME'
  }
})


