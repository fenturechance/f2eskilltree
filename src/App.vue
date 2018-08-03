<template>
  <div id="app">
      <div class="titleWrapper">
          <div class="startGroup">
              <i class="fas fa-star" v-for="s in 8"></i>
          </div>
          <div class="plant imgBG"></div>
          <div class="titleGroup">
            <h1>介面設計師轉職之路</h1>
            <h2>UI Designer Road Map</h2>
          </div>
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
    $shaBlue : #0093FF;
    @import url(http://fonts.googleapis.com/earlyaccess/cwtexyen.css);
    *{
        margin: 0;
        padding: 0;
        list-style: none;
        font-family: 'cwTeXYen', 'Poller One';
        box-sizing: border-box;
    }
    .imgBG{
        background-size: cover;
        background-position: center center;
    }
    #app{
        background: linear-gradient(0deg,$deepPurple , $black);
        padding: 20px 30px;
        .titleWrapper{
            display: flex;
            height: 25vh;
            color: $w;
            align-items: center;
            padding: 0 30px;
            position: relative;
            .startGroup{
                position: absolute;
                z-index: 1;
                height: 100%;
                width: 100%;
                top: 0;
                left: 0;
                .fa-star{
                    position: absolute;
                    &:nth-child(1){
                        left: 0%;
                        top: 10%;
                        font-size: 5px;
                    }
                    &:nth-child(2),&:nth-child(3),&:nth-child(4),&:nth-child(6),&:nth-child(8){
                        opacity: 0.4;
                        font-size: 1px;
                    }
                    &:nth-child(2){
                        left: 2%;
                        top: 30%;
                    }
                    &:nth-child(3){
                        left: 20%;
                        top: 5%;
                    }
                    &:nth-child(4){
                        left: 35%;
                        top: 10%;
                    }
                    &:nth-child(5){
                        right: 45%;
                        top: -10%;
                    }
                    &:nth-child(6){
                        right: 20%;
                        top: 10%;
                    }
                    &:nth-child(7){
                        right: 10%;
                        top: 15%;
                    }
                    &:nth-child(8){
                        right: 0%;
                        bottom: 20%;
                    }
                }
                &:before,&:after{
                    content: '. . . . . . . . .';
                    position: absolute;
                    font-size: 1px;
                    width: 2px;
                    height: 100%;
                    line-height: 20px;
                }
                &:before{
                    left: 5%;
                    top: -30%;
                }
                &:after{
                    right: 30%;
                    top: -20%;
                }
            }
            .plant{
                width: 150px;
                height: 150px;
                background-image: url('/dist/images/img_planet.png');
            }
            .titleGroup{
                margin: 0 0 0 20px;
                h1,h2{
                    text-shadow: 2px 2px 0px $shaBlue;
                }
                h1{
                    font-size: 52px;
                    letter-spacing: 5px;
                }
                h2{
                    font-size: 30px;
                    letter-spacing: 3px;
                }
            }
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
