<template>
  <div v-bind:class="{ invalid: showValidation && !valid }">
    <label v-bind:class="{ raised: this.value.length || this.focused }">{{title}}{{required ? '*' : ''}}</label>
    <input
      v-bind:type="type || 'text'"
      v-bind:value="value" v-on:input="$emit('input', $event.target.value)"
      v-on:focus="focused = true" v-on:blur="focused = false"
      v-on:keypress="checkInput"
    >
  </div>
</template>

<script src="./script.js"></script>

<style scoped lang="sass" src="./style.sass"></style>
