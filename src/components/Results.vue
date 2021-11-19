<template>
  <h1>You took {{ score }} ms to click the box!</h1>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'E-Sports level'
        } else if (this.score < 400) {
            this.rank = 'Casual gamer'
        } else {
            this.rank = 'Grandpa?'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.7em;
        color: #251857;
        font-weight: bold;
    }
</style>