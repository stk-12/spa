<template>
    <div class="contents">
        <div class="inner">
            <h1>HOME</h1>
            <!-- <button @click="linkAbout">Aboutへ</button> -->
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        linkAbout() {
            this.$router.push('about')
        }
    }
}
</script>