<template>
  <div class="cool-cut">
    <div class="preview">预览区</div>
    <div class="layer">
      <div class="layer-tree">
        <layer-tree></layer-tree>
      </div>
    </div>
  </div>  
</template>

<script>
  import LayerTree from './layer-tree'
  // const PSD = require('psd')
  // console.log('PSD', PSD)
  export default {
    name: 'cool-cut',
    props: ['file'],
    components: {
      LayerTree
    },
    mounted () {
      console.log('cool-cut 哈哈哈哈，在这里分析读取文件了', this.file)
    }
  }
</script>