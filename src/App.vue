<template>
  <div class="Nestone">
    <h1> Data-rendering</h1>
    <p>{{ greeting }}</p>

    <h2>Toggle Visibility</h2>
    <inout v-model="name" />
    <p>Secret message: {{ message }}</p>
    <button @click="secretMessage">Here</button>

    <h2> List of Life Goals</h2>
    <ul>
<li v-for="(lifegoals. index) in lifegoals" :key="index">
  {{ index + 1 }}. {{ lifegoals }}
</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
data() {
  return {
    message: 'Hi there this is the secret message',
    lifegoals: ['Be an intellegent baddie', 'Gymbro', 'Build a portfolio'],
    secretMessage: false,
    greeting:'Hello there'
  }
},
  methods: {
secretMessage() {
  this.secretMessage="hi there"
}
  },
}
</script>
