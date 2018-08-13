<template>
    <Panel :class="$style.panel" :title="title">
        <section :class="$style.content">
            <div :class="$style.item">
                <h4>下载APP<span :class="$style.red">送888元礼包</span></h4>
                <p :class="$style.gray">新手专享</p>
                <svg class="icon" aria-hidden="true">
                    <use xlink:href="#icon-xinshoulibao"></use>
                </svg>
            </div>
            <div :class="$style.item">
                <ul>
                    <li>
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-07"></use>
                        </svg>
                        <h4 :class="$style.red">领128元新手红包</h4>
                        <p :class="$style.gray">立即开通</p>
                    </li>
                    <li>
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-jingdongbaitiao"></use>
                        </svg>
                        <h4 :class="$style.red">打白条<span :class="$style.red">享免息</span></h4>
                        <p :class="$style.gray">立即开通享好礼</p>
                    </li>
                </ul>
            </div>
        </section>
    </Panel>
</template>

<script>
import Panel from '../core/panel.vue'
    export default {
        data(){
            return{
                title:"新手专享"
            }
        },
        components:{
            Panel
        }
    }
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
    @include panel;
    >h4{
        border-bottom: 1px solid #ddd;
    }
    .content{
        @include list(row);
        .item{
            width: 50%;
            box-sizing: border-box;
            &:first-child{
                padding: 32px 20px;
                text-align: center;
                svg{
                    width: 132px;
                    height: 132px;
                    margin: 20px auto;
                }
                border-right: 1px solid #ddd;
            }
            h4{
                font-size: 26px;
                line-height: 40px;
                .red{
                    color: red;
                }
            }
            .gray{
                color: #999;
                font-size: 24px;
            }
            p{
                margin-top: 6px;
                font-size: 24px;
            }
            ul{
                width: 100%;
                li{
                    height: 144px;
                    width: 100%;
                    padding: 32px 28px;
                    box-sizing: border-box;
                    &:first-child{
                        border-bottom: 1px solid #ddd;
                    }
                    h4{
                        white-space: nowrap;
                        text-overflow: ellipsis;
                        overflow: hidden;
                        text-align: left;
                    }
                    svg{
                        width: 80px;
                        height: 80px;
                        float: right;
                    }
                }
            }
        }
    }
}
</style>