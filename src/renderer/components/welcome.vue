<template>
  <div class="welcome">
    <h1 class="name">coolcut</h1>
    <h1 class="chinese">一刀切</h1>
    <p class="version">不知道后期还会不会维护版本</p>
  </div>
</template>

<script>
  export default {
    name: 'welcome',
    mounted () {
      window.setTimeout(() => {
        this.$emit('welcomend')
      }, 1000)
    }
  }
</script>

<style lang="scss">
  .welcome {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    > .name {
      font-size: 8rem;
      text-transform: capitalize;
    }
  }
</style>
