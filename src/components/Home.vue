<template>
  <div id="main-container">

        <!-- Placeholders for title and description -->
        <header class="main-header">
            <h1>{{logo ? "" : title }}<img :src="logo" width="80px"></h1>
            <p>{{subtitle}}</p>
        </header>
        

        <!-- REACTIVE COLUMNS FOR LAYOUT -->
        <!-- https://purecss.io/ -->
        <div class="pure-g" id="content-container">
            <div class="pure-u-1 pure-u-md-14-24 pure-u-lg-14-24">
                <h3>HERE'S</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
            <div class="pure-hidden-phone pure-u-md-2-24 pure-u-lg-2-24">
                <!-- SPACING -->
            </div>
            <div class="pure-u-1 pure-u-md-8-24 pure-u-lg-8-24 quick-action-panel">
                <button class="main-action" v-for="x in mainActions" :key="x.name" :style="x.style" v-on:click="hello(x.name)">{{x.label}}</button>
            </div>
        </div>

    </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    
    header{
        padding: 1em;
        padding-top: 2em;
        padding-bottom: 2em;
        margin: 0;
        margin-top: -1.4em;
        text-align: center;
        box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);

        background: -moz-linear-gradient(270deg, rgba(22,192,240,1) 0%, rgba(140,46,255,1) 100%); /* ff3.6+ */
        background: -webkit-gradient(linear, left top, left bottom, color-stop(0%, rgba(22,192,240,1)), color-stop(100%, rgba(140,46,255,1))); /* safari4+,chrome */
        background: -webkit-linear-gradient(270deg, rgba(22,192,240,1) 0%, rgba(140,46,255,1) 100%); /* safari5.1+,chrome10+ */
        background: -o-linear-gradient(270deg, rgba(22,192,240,1) 0%, rgba(140,46,255,1) 100%); /* opera 11.10+ */
        background: -ms-linear-gradient(270deg, rgba(22,192,240,1) 0%, rgba(140,46,255,1) 100%); /* ie10+ */
        background: linear-gradient(180deg, rgba(22,192,240,1) 0%, rgba(140,46,255,1) 100%); /* w3c */
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#16C0F0', endColorstr='#8C2EFF',GradientType=0 ); /* ie6-9 */
    }

    header > h1{
        margin-bottom: .2em;
        color: whitesmoke;
    }

    header > p{
        padding: 0;
        margin: 0;
    }

    #content-container{
        padding: 1em;
    }

    #content-container h3, #content-container p, #content-container button{
        font-family: 'Anonymous Pro', monospace;
    }
    
    .quick-action-panel{
        margin-top: 2em;
    }

    .main-action{
        color: rgb(56, 56, 56);
        background-color: rgb(255, 255, 255);
        border: none;
        border-radius: .2em;
        padding: .5em;
        padding-left: 2em;
        padding-right: 2em;
        display: block;
        margin-top: 1em;
        border: solid 1px rgb(56, 56, 56);
        border-bottom: solid 5px black; 
        outline: none;
    }
    .main-action:hover{
        cursor: pointer;
        opacity: .8;
    }

</style>


<script>
// import flux_logo from "./assets/flux_logo.png"

export default {
  name: 'Home',
  data () {
    return {
        title: "<TITLE>",
        subtitle : "Own your internet.",
        logo: "",
        menuSections : [
            {title: 'hello'},
            {title: 'hello'},
            {title: 'hello'},
            {title: 'hello'},
            {title: 'hello'},
        ],
        mainActions: [
            {name:"contact", label: "📲 CONTACT US", style: {'border-bottom-color':"#00d639", 'color':"#00d639"} },
            {name:"recruit", label: "👨🏾‍💻 WORK WITH US", style: {'border-bottom-color':"#3a9bff", 'color':"#3a9bff"} },
            {name:"paper", label: "📄 READ WHITE PAPER", style: {'border-bottom-color':"#8c2eff", 'color':"#8c2eff"} },
        ]
    }
  },
  methods: {
      hello: (name) => {
          const actionList = {
              contact:  () => { window.location.href = "mailto:igorp@bu.edu?subject=🦈 shark-net"; },
              recruit:  () => { const url = "https://goo.gl/forms/VAPp6apjFu72ZCiM2"; window.open(url,'_blank'); },
              paper:    () => { const url = "https://goo.gl/wGjxBc"; window.open(url,'_blank'); } // alternative link https://docs.google.com/document/d/1saBIWnagS3SBVxe89iDIvH_TgO6-pe813muS7W3GIg4/edit?usp=sharing
          }
          let action = actionList[name];
          action();
      },
  }
}

</script>
