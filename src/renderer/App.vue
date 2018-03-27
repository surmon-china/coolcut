<template>
  <div id="app">
    <!-- <welcome></welcome> -->
    <cool-cut></cool-cut>
    <!-- <add-file></add-file> -->
  </div>
</template>

<script>
  import Welcome from '@/components/welcome'
  import CoolCut from '@/components/cool-cut'
  import AddFile from '@/components/add-file'
  export default {
    name: 'coolcut',
    components: {
      Welcome,
      CoolCut,
      AddFile
    }
  }
</script>

<style lang="scss">

</style>
