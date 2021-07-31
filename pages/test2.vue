<template>
  <div class="container">
    <div class="ASM">
      <nuxt-link class="button" to="/blag">Play</nuxt-link>
    </div>
  </div>
</template>

<script>
</script>

<style>
.button {
  border: 1px solid var(--color-5);
  padding: 1em 2em;
  border-radius: 50px;
  font-size: 14px;
  color: var(--color-5);
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 2.002px;
  /*left: 47%;*/
  /* overflow: hidden; */
  transition: background-color 0.3s, color 0.3s;
}
.button:hover {
  background-color: var(--color-5);
  color: var(--color-1);
}

.button:focus {
  background-color: var(--color-5);
  color: var(--color-1);
}
</style>