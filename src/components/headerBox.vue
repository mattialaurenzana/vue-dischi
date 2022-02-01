<template>
    <header>
        <img src="../assets/spotify-brands.svg" alt="">
        <select name="" id="" v-model="selectedOption" @click="$emit('search',selectedOption)">
            <option disabled value="">Please select your genre</option>
            <option>Pop</option>
            <option>Rock</option>
            <option>Jazz</option>
            <option>Metal</option>
            <option>All</option>
        </select>
     
    </header>
</template>

<script>
export default {
    data(){
        return{
            selectedOption: "",
            selectedArtist: "",
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/header.scss'
</style>