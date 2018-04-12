<template>
  <div class="add-file">
    <div class="upload">
      <input class="file-input" id="xFile" type="file" ref="file" />
      <label class="file-up-btn" for="xFile">添加文件</label>
      <p class="state" v-if="state">
        <span v-if="state === 1">上传中</span>
        <span v-if="state === 2">读取分析中</span>
      </p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'add-file',
    data () {
      return {
        state: 0
      }
    },
    mounted () {
    },
    methods: {

    }
  }
</script>

<style lang="scss">
  .add-file {
    width: 100%;
    height: 100%;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    > .upload {

      > .file-input {
        position: absolute;
        top: 0;
        left: 0;
        width: 0;
        height: 0;
        opacity: 0;
        visibility: hidden;
      }

      > .file-up-btn {
        display: block;
        width: 10rem;
        height: 4rem;
        line-height: 4rem;
        text-align: center;
        border: 3px solid #eee;
        font-size: 1.5rem;
        cursor: pointer;

        &:hover {
          background-color: #000;
        }
      }
    }
  }
</style>
