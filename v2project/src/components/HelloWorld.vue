<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    {{ htmlString }}
    <v-linkify :html="htmlString" />
    <div v-html="scriptString"></div>
    <v-linkify :html="scriptString" />
  </div>
</template>

<script>
import vLinkify from 'vue-linkify-v2';

export default {
  name: 'HelloWorld',
  components: {
    vLinkify
  },
  data: function() {
    return {
      htmlString: 'For help with http://github.com.',
      scriptString: '<div onmouseover="alert(1+1)">focus</div>',
    }
  },
  props: {
    msg: String
  }
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
