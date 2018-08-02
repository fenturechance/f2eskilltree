<template>
  <div id="app">
      <div class="titleWrapper"></div>
      <div class="treeWrapper"></div>
      <div class="descriptionWrapper"></div>
      <div class="footerWrapper"></div>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
    $deepPurple : #301A3B;
    $black :#10030A;
    *{
        margin: 0;
        padding: 0;
        list-style: none;
    }
    #app{
        background: linear-gradient(0deg,$deepPurple , $black);
        .titleWrapper{
            height: 30vh;
        }
        .treeWrapper{
            height: 50vh;
        }
        .descriptionWrapper{
            height: 50vh;
        }
        .footerWrapper{
            height: 30vh;
        }
    }
</style>
