<template>
    <div>
        <TheNavbar></TheNavbar>
        <div class="container">
            <h1>Helloo {{message}}</h1>

            <h2>Posts List</h2>
        </div>
    </div>
</template>

<script>
    import TheNavbar from './frontend/components/TheNavbar.vue';
    export default{
        components: { TheNavbar },
        data() {
            return {
                message: "Hiii"
            }
        }
    }
</script>