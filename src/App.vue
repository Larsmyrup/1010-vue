<template>
    <div id="app">
        <h1>Verdens bedste 1010!</h1>
        <Board/>
        <PieceBoard/>
    </div>
</template>

<script>
  import Board from './components/Board'
  import PieceBoard from './components/PieceBoard'

  export default {
    name: 'app',
    components: {
      PieceBoard,
      Board
    }
  }
</script>

<style lang="scss">
    html, body {
        height: 100%;
        margin: 0;
        padding: 0;
        background-color: $primary;
    }

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        margin-top: 60px;
        color: $text;
    }

    .cell {
        height: 50px;
        width: 50px;
        margin: 10px;
        background-color: $text;
        border-radius: 6px;
        flex-wrap: wrap;
    }

    .row {
        display: flex;
        width: auto;
        flex-direction: row; /* make main axis vertical */
        justify-content: center; /* center items vertically, in this case */
        align-items: center;
    }
</style>
