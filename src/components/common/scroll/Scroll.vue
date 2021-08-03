<template>
    <div class="wapp" ref="wrapper">
        <div class="content">
            <slot></slot>
        </div>
    </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
    name: "Scroll",
    data() {
        return {
            scroll: null
        }
    },
    mounted() {
        setTimeout(function(){
            this.scroll = new BScroll(document.querySelector('.wapp'), {
                click:true
        })
        },5000);

        // this.scroll.scrollTo(0,0)
    },
    methods: {
        scrollTo(x,y){
            this.scroll.scrollTo(0,0)
        }
    }
}
</script>

<style scoped>

</style>