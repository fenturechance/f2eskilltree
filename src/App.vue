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
      <div class="treeWrapper">
          <div class="leftGroup">
                <div v-for="c in leftGroup" :class="c.class" class="frameOuter">
                    <div class="blueFrame frame">
                        <div class="imgBG"></div>
                    </div>
                    <div class="arrow"></div>
                    <p>{{ c.title }}</p>
                </div>
          </div>
          <div class="centerGroup">

          </div>
          <div class="rightGroup">

          </div>
      </div>
      <div class="descriptionWrapper"></div>
      <div class="footerWrapper"></div>
  </div>
</template>

<script>
export default {
  data () {
    return {
        leftGroup: [
            {
                class : 'designRule',
                title: '設計規範'
            },
            {
                class : 'goods',
                title: '爬梳乾貨'
            },
            {
                class : 'uxThink',
                title: 'UX思維'
            },
            {
                class : 'designThink',
                title: '設計思考'
            },
            {
                class : 'psychology',
                title: '心理學'
            },
        ]
    }
  }
}
</script>

<style lang="scss">
    $deepPurple : #301A3B;
    $black :#10030A;
    $w :#fff;
    $shaBlue : #0093FF;
    $borBlue : #5791FF;
    $innerBlue : #0C467E;
    $arrowLineWidth : 15px;
    $frameWidth : 80px;
    $arrowWidth : 20px;
    @import url(http://fonts.googleapis.com/earlyaccess/cwtexyen.css);
    *{
        margin: 0;
        padding: 0;
        list-style: none;
        font-family: '微軟正黑體', 'Poller One';
        box-sizing: border-box;
    }
    .imgBG{
        background-size: cover;
        background-position: center center;
        background-repeat: no-repeat;
    }
    .frameOuter{
        position: relative;
    }
    .frame{
        border: 5px solid $shaBlue;
        box-shadow: 0 0 0 5px $borBlue;
        background-color: $innerBlue;
        width: $frameWidth;
        height: $frameWidth;
        position: absolute;
        border-radius: 30px;
        .imgBG{
            position: absolute;
            width: 120%;
            height: 120%;
            top: 50%;
            left: 50%;
            transform: translateX(-50%) translateY(-50%);
            background-size: contain;
        }
    }
    .arrow{
        width: 100%;
        height: $frameWidth;
        position: relative;
        &:before,&:after{
            content: '';
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
        }
        &:before{
            height: $arrowLineWidth;
            background-color: $w;
        }
        &:after{
            width: 0;
            height: 0;
            border-left: $arrowWidth solid $w;
            border-top: $arrowWidth solid transparent;
            border-bottom: $arrowWidth solid transparent;
        }
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
                background-image: url('../dist/images/img_planet.png');
            }
            .titleGroup{
                margin: 0 0 0 20px;
                h1,h2{
                    font-family: 'cwTeXYen', 'Poller One';
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
            display: flex;
            color: $w;
            font-size: 20px;
            text-shadow: 1px 1px 0px $shaBlue;
            font-weight: bold;
            .leftGroup{
                position: relative;
                width: 30%;
                display: flex;
                flex-wrap: wrap;
                p{
                    margin: 10px 0 0 0;
                }
                .designRule{
                    width: 50%;
                    .frame{
                        .imgBG{
                            background-image: url('../dist/images/img_blade-1.png');
                        }
                    }
                    .arrow{
                        &:before{
                            width: calc( 100% - 120px );
                            left: 100px;
                        }
                        &:after{
                            right: 10px;
                        }
                    }
                }
                .goods{
                    width: 50%;
                    .frame{
                        .imgBG{
                            background-image: url('../dist/images/img_meat.png');
                        }
                    }
                    .arrow{
                        &:before{
                            width: calc( 60% - 120px );
                            left: 100px;
                        }
                        &:after{
                            border: none;
                            width: 15px;
                            height: 200px;
                            background-color: $w;
                            right: calc( 60% - 40px );
                            top: 50%;
                            transform: translateY(-7px);
                        }
                    }
                }
                .uxThink{
                    width: 30%;
                    .frame{
                        .imgBG{
                            background-image: url('../dist/images/img_shield.png');
                        }
                    }
                    .arrow{
                        &:before{
                            width: calc( 100% - 120px );
                            left: 100px;
                        }
                        &:after{
                            right: 10px;
                        }
                    }
                }
                .designThink{
                    width: 40%;
                    .frame{
                        .imgBG{
                            background-image: url('../dist/images/img_hat.png');
                        }
                    }
                    .arrow{
                        &:before{
                            width: calc( 100% - 120px );
                            left: 100px;
                        }
                        &:after{
                            right: 10px;
                        }
                    }
                }
                .psychology{
                    width: 30%;
                    p{
                        margin: 90px 0 0 0;
                    }
                    .frame{
                        .imgBG{
                            background-image: url('../dist/images/img_horn.png');
                        }
                    }
                    .arrow{
                        position: absolute;
                        top: -60%;
                        &:before{
                            width: calc( 100% - 60px );
                            left: 40px;
                        }
                        &:after{
                            right: 10px;
                        }
                    }
                }
            }
            .centerGroup{
                width: 40%;
            }
            .rightGroup{
                width: 30%;
            }
        }
        .descriptionWrapper{
            height: 50vh;
        }
        .footerWrapper{
            height: 30vh;
        }
    }
</style>
