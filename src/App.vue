<template>
  <div id="app">
      <div class="titleWrapper">
          <div class="plant"></div>
          <h1>介面設計師轉職之路</h1>
          <h2>UI Designer Road Map</h2>
      </div>
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
    $w :#fff;
    @import url(http://fonts.googleapis.com/earlyaccess/cwtexyen.css);
    *{
        margin: 0;
        padding: 0;
        list-style: none;
        font-family: 'cwTeXYen', 'Poller One';
    }
    #app{
        background: linear-gradient(0deg,$deepPurple , $black);
        .titleWrapper{
            height: 30vh;
            color: $w;
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
