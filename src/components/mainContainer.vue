<template>
    <div>
        <div class="container">
            <div class="row">
                <card-box v-for="(item,index) in discList" :key="index" :disk="item"/>
                
            </div>
        </div>
    </div>
</template>

<script>
import cardBox from './cardBox.vue'
export default {
    components: {
        cardBox,
    },
    props: {
        discList : Array
    }
}
</script>

<style lang="scss" scoped>

</style>