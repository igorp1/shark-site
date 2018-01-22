<template>
  <div id="main-container">

        <!-- Placeholders for title and description -->
        <h1 :style="main_color">{{logo ? "" : title }}<img :src="logo" width="80px"></h1>
        <p>{{subtitle}}</p>

        <!-- REACTIVE COLUMNS FOR LAYOUT -->
        <!-- https://purecss.io/ -->
        <div class="pure-g">
            <div class="pure-u-1 pure-u-md-1-2 pure-u-lg-1-4">
                <h3>HERE'S</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
            <div class="pure-u-1 pure-u-md-1-2 pure-u-lg-1-4">
                <h3>SOME</h3>
                <p>Morbi quis neque nec ante maximus fringilla at eget nisi.</p>
            </div>
            <div class="pure-u-1 pure-u-md-1-2 pure-u-lg-1-4">
                <h3>REACTIVE</h3>
                <p>Mauris laoreet justo feugiat tincidunt vehicula.</p>
            </div>
            <div class="pure-u-1 pure-u-md-1-2 pure-u-lg-1-4">
                <h3>COLUMNS</h3>
                <p>Etiam congue libero dictum eleifend blandit.</p>
            </div>
        </div>

    </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>


<script>
// import flux_logo from "./assets/flux_logo.png"

export default {
  name: 'Home',
  data () {
    return {
        title: "🦈 SHARK",
        subtitle : "Build, connect and empower",
        logo: "",
        main_color : {'color':"#3053C4"}
    }
  }
}
</script>
