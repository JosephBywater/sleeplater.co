<template>
  <div class="page">
    <h1 class="bg-title fade-in">sleep later</h1>
    <products-display></products-display>
    <cart-button v-bind:items-count="itemsCount" v-on:click.native="cartOpen = true"></cart-button>
    <cart v-bind:hidden="!cartOpen" v-on:close="cartOpen = false"></cart>
  </div>
</template>

<script src="./script.js"></script>
<style scoped lang="sass" src="./style.sass"></style>
