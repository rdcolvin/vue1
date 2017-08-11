<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <rich></rich>
    <div v-for="qline in poll">
      <qline :qline="qline"></qline>
    </div>
  </div>
</template>

<script>
import Rich1 from './Rich1'
import QLine from './QLine'

export default {
  name: 'hello',
  components: {
    'rich': Rich1,
    'qline': QLine
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      'poll': [
        {line: 'line0', type: 'check'},
        {line: 'line1', type: 'radio'},
        {line: 'line2', type: 'check'}
      ],
      line1Msg: 'line one'
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
