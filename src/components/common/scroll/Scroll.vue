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
                observeImage: true,
                ObserveDom:true,
                click:true
        })
        },5000);
    }
}
</script>

<style scoped>

</style>