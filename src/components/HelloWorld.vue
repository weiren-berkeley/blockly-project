<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div id="blocklyDiv" style="height: 480px; width: 600px;"></div>
  </div>
</template>

<script>
import * as Blockly from 'google-blockly/blockly_accessible_uncompressed'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted () {
    this.programming()
  },
  methods: {
    programming () {
      var toolbox = '<xml>'
      toolbox += '  <block type="controls_if"></block>'
      toolbox += '  <block type="controls_whileUntil"></block>'
      toolbox += '</xml>'
      var workspace = Blockly.inject('blocklyDiv', {toolbox: toolbox})
      console.log(workspace)
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
