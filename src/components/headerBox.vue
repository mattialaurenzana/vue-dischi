<template>
    <header>
        <img src="../assets/spotify-brands.svg" alt="">
        <select v-model="selectedOption" @change="$emit('search',selectedOption)">
            <option disabled value="">Please select your genre</option>
            <option>Pop</option>
            <option>Rock</option>
            <option>Jazz</option>
            <option>Metal</option>
            <option>All</option>
        </select>
            <select v-model="selectedArtist" @change="$emit('artistResearch',selectedArtist)">
            <option disabled value="">Please select your artist</option>
            <option>Bon Jovi</option>
            <option>Queen</option>
            <option>Sting</option>
            <option>Steve Gadd Band</option>
            <option>Iron Maiden</option>
            <option>Eric Clapton</option>
            <option>Deep Purple</option>
            <option>Metallica</option>
            <option>Dave Weckl</option>
            <option>Michael Jacjson</option>
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