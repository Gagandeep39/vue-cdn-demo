# Vue

- [Vue](#vue)
  - [Steps to run](#steps-to-run)
  - [CDN](#cdn)
  - [NOTE](#note)

## Steps to run

1. Doubleclick on `index.html` to start it in browser
2. Test by adding goals

## CDN

1. Add script path `<script src="https://unpkg.com/vue@next"></script>` in html file

   - Fetch latest version at `https://v3.vuejs.org/guide/installation.html#cdn`

2. Create a Vue app

```js
Vue.createApp({
  data() {
    return {
      goals: [],
      enteredValue: '',
    };
  },
  methods: {
    addGoal() {
      this.goals.push(this.enteredValue);
    },
  },
}).mount('#app);
```

- Events
  - Methds contains various methods
  - Methods are called using `<button v-on:click="addGoal">Add Goal</button>`
- Models
  - data contains list of all variables
  - Variable binding is performed using `<input type="text" id="goal" v-model="enteredValue" />`
  - v-model binds the input field data with vue
- Control flow
  - `<li v-for="(item, index) in goals" :key="index"> {{ item }} </li>`
  - goals is an array which is rendered using for loop
- `.mount('#app')`
  - Implies where to use vue code
  - `#` implies ID selector
  - `app` is id of div

## NOTE

- In Vue, we always define how we will get the desisred results
- **Always** Make sure you re referring to Vue 3 docs and **not** Vue2
