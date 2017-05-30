<template>
  <div id="app">
    <h1>vue-event-calendar</h1>
    <h2 class="t-center">Custom template</h2>
    <vue-event-calendar :events="demoEvents">
      <template scope="props">
        <div v-for="(event, index) in props.showEvents" class="event-item">
          {{event}}
        </div>
      </template>
    </vue-event-calendar>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      demoEvents: [{
        date: '2017/05/29',
        title: 'eat',
        desc: 'longlonglong description'
      },{
        date: '2017/05/12',
        title: 'this is a title'
      },
      {
        date: '2017/05/30',
        title: 'this is a title'
      }]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 30px;
}

h1, h2, h3 {
  font-weight: normal;
  margin: 0;
  padding: 0;
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
.t-center{
  text-align: center;
  margin: 20px;
}
</style>
