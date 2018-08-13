<!-- 借贷 -->
<template>
    <Panel :class="$style.panel" title="急速接待">
        <section :class="$style.content">
            <router-link :to="{name:'home'}">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t20746/93/1719082958/12040/306a2296/5b31b40dNeefe4c3c.png?width=750&height=200" alt="">
            </router-link>
        </section>
    </Panel>
</template>

<script>
import Panel from '../core/panel.vue'
    export default {
        components:{
            Panel,
        }
    }
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel{
        @include panel;
        .content{
            padding-bottom: 40px;
            img{
                display: block;
                width: 100%;
            }
        }
    }

</style>