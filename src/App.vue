<template>
  <div id='app'>

    <main class='wrapper'>
      <div class='content'>
        <div class='download-group'>
          <div class='label'>
            Mac OSX, 0.0.3-alpha
          </div>
            <form method='get' action='https://download.thewilljustice.com/download/latest'>
            <button type='submit' class='download' name='download'>Download!</button>
          </form>
        </div>
      </div>
    </main>

  </div>
</template>

<script>
export default {
  data () {
    return {
      latestVersion: ''
    }
  },
  methods: {},
  created: function () {
    let url = 'https://download.thewilljustice.com'

    // fetch(`${url}/api/versions`, {
    //   mode: 'no-cors'
    // })
    // .then(response => {
    //   console.log(response)
    // })
    // .catch(err => {
    //   console.log('err', err)
    // })

  }
}
</script>

<style lang='sass'>
  @import './scss/main.scss';
  $ultramarine: #6866FF;
  $background: #6866FF;
  $secondary: white

  ::-moz-selection {
    color: white;
    background: pink;
  }

  ::selection {
    color: white;
    background: pink;
  }

  body {
    background: $background;
    color: white;
    font-family: 'Courier New', 'Courier';
    overflow: hidden;
  }

  h1 {
    font-size: 1.6em;
    font-weight: 100;
  }
  .wrapper{
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    justify-content: center;
  }
  .content {
    width: 66.7%;
    max-width: 800px;
    flex-flow: row wrap;
    align-items: center;
    transform: translateY(-22.7%);
    display: flex;
    justify-content: center;
  }
  button {
    color: $secondary;
    font-size: 12px;
    font-family: inherit;
    background: $ultramarine;
    border: 1px solid $secondary;
    box-shadow: 0px 2px 0px 0px $secondary;
    transform: translate(0, 0);
    transition: color .2s;
    border-radius: 3px;
    padding: 7px;
    outline: none;
    cursor: pointer;
  }
  .download-group {
    text-align: center;
    width: 250px;
    .label {
      margin-bottom: .2em;
    }
    button.download {
      font-size: 2em;
      width: 100%;
    }
  }

</style>
