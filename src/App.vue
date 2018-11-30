<template>
<div>
  <div>
    <h3>My Identicon Generator</h3>
  </div>
  <div>
  Input:
  <input v-on:input="onInput" />
  </div>

  <div>
  Output:
  <div v-html="identicon"></div>
  </div>
</div>
</template>

<script>
export default {
el: '#app',
data: { // Initialize our list of 'ingredients'
textInput: ''
},
computed: { // Turn data into viewable values
identicon: function() {
return jdenticon.toSvg(this.textInput, 200);
}
},
methods: { // Use these functions to change data
onInput: function(event) {
this.textInput = event.target.value;
}
}
}
</script>