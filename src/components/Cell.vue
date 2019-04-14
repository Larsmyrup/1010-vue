<template>
    <div class="cell">

    </div>
</template>

<script>
  export default {
    name: 'Cell',
    props: {
      color: String
    },
    computed: {
      style() {
        return 'background-color: ' + this.color
      }
    }
  }
</script>

<style scoped>

</style>
