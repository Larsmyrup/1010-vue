<template>
    <div class="row pieceBoard">

        <OneTimesOne/>
        <OneTimesOne/>
        <OneTimesOne/>

    </div>
</template>

<script>
  import OneTimesOne from './pieces/OneTimesOne'

  export default {
    name: 'PieceBoard',
    components: { OneTimesOne },

    data () {
      return {
        property: 'Blank'
      }
    },

    computed: {
      propertyComputed () {
        console.log('I change when this.property changes.')
        return this.property
      }
    },

    created () {
      this.property = 'Example property update.'
      console.log('propertyComputed will update, as this.property is now reactive.')
    }
  }


</script>

<style scoped lang="scss">
    .pieceBoard {
        width: 800px;
        background-color: $secondary;
        border-radius: 10px;
        margin-top: 20px;
        margin-left: auto;
        margin-right: auto;
        height: 300px;
        justify-content: space-evenly;
    }
</style>
