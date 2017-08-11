<template>
  <div class="qline">
    <div v-if="checkbox">
      <input type="checkbox" id="cb1" />
    </div>
    <div v-if="radio">
      <input type="radio" id="rd1" />
    </div>
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'QLine',
  props: {
    qline: {
    }
  },
  data () {
    return {
      checkbox: false,
      radio: false,
      msg: ''
    }
  },
  created () {
    this.msg = this.qline.line
    this.checkbox = this.qline.type === 'check'
    this.radio = this.qline.type === 'radio'
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
