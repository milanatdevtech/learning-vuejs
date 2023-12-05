<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ subTitle }}</h2>
    <ul id="task-list">
       <li v-for="link in links">
         <a :href="link.url">{{ link.title }}</a>
       </li>
     </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Passing data to template',
      subTitle: 'Use loop itteration',
      links: [
        {
          'title': 'Core Docs',
          'url': 'https://vuejs.org'
        },
        {
          'title': 'Forum',
          'url': 'https://forum.vuejs.org'
        },
        {
          'title': 'Community Chat',
          'url': 'https://chat.vuejs.org'
        },
        {
          'title': 'Templates',
          'url': 'http://vuejs-templates.github.io/webpack/'
        },
      ]
    }
  }
}
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
