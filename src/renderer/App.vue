<template>
  <div id="app">
    <transition name="component">
      <welcome v-if="welcomeing" @welcomend="welcomend" />
      <cool-cut v-else-if="file" :file="file" />
      <add-file v-else @file-change="fileChage" />
    </transition>
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
    },
    data () {
      return {
        file: null,
        welcomeing: true
      }
    },
    methods: {
      welcomend () {
        this.welcomeing = false
      },
      fileChage (file) {
        this.file = file
        // console.log('可以开始分析文件啦', file)
      }
    }
  }
</script>

<style lang="scss">
  body {
    margin: 0;
    height: 100vh;
    width: 100vw;
    font-size: 14px;
    -webkit-app-region: drag;
    background-color: #fff;
    font-family: DINRegular, "Microsoft YaHei", "\5FAE\8F6F\96C5\9ED1", "Hiragino Sans GB", STXihei, "\534E\6587\7EC6\9ED1", STHeiti, "RobotoDraft", "Roboto", "Helvetica Neue", Helvetica, Tahoma, "Droid Sans", "wenquanyi micro hei", FreeSans, Arimo, Arial, SimSun, "\5B8B\4F53", Heiti, "\9ED1\4F53", sans-serif;
  }
  p, span, a, h1, h2, h3 {
    -webkit-app-region: no-drag;
  }
  // .component {}
</style>

<style lang="scss">
  #app {
    display: flex;
    height: 100vh;
    width: 100vw;

    > .welcome {

    }
  }
</style>
