<template>
  <div id="cool-cut" class="cool-cut-view">
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
  export default {
    name: 'cool-cut',
    components: {
      LayerTree
    }
  }
</script>