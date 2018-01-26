<template>
  <div id="main-container">

        <!-- Placeholders for title and description -->
        <header class="main-header">
            <h1>{{title}}</h1>
            <p>{{subtitle}}</p>
        </header>
        

        <!-- REACTIVE COLUMNS FOR LAYOUT -->
        <!-- https://purecss.io/ -->
        <div class="pure-g" id="content-container">
            <div class="pure-u-1 pure-u-md-14-24 pure-u-lg-14-24">
                <!-- Add main text content here -->
                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/antenna.svg" width="70px" height="70px">
                    <h3>Always connected</h3>
                </div>
                <p>
                    Our goal is to bring quality affordable internet by reinventing the infrastructure and underlying technology behind web connectivity.
                    <br><br>
                    We are working on creating a device that will be, primarily, a wifi router and internet modem. It can be for personal use or for businesses. 
                    However unlike standard routers it will require no setup and share internet with all of those in range. 
                    That means that if you own the device you are guaranteed the best possible internet experience however you can also benefit those around you 
                    without compromising your browsing experience or web security.      
                    <br><br>
                    Free access users will be able to download and upload up to 500Mb of data daily. However with as much as $10/month you will have unlimited
                    access to internet through any of our devices anywhere in the world. We will never throttle your bandwith, our devices are prepared to serve multiple users.  
                </p>
                </div>
                
                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/hardware.svg" width="70px" height="70px">
                    <h3>Smart hardware</h3>
                </div>
                <p>
                    You don't need to be an expert to setup or secure your wifi. 
                    Our devices can communicate with each other through wireless technology to create a larger network. 
                    That means you can either plug it to ethernet and become a host - earning you credit towards your account - 
                    or just turn your device on, let it connect to the network and you are good to go.
                </p>
                </div>

                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/net.svg" width="70px" height="70px">
                    <h3>Blockchain</h3>
                </div>
                <p>
                    Thanks to Blockchain technology, it is now possible to implement a fully decentralized network model in a highly secure and reliable fashion. 
                    That means that applications can be "hosted" in the blockchain and can be accessed through secure transactions, similarly to how web requests work.
                    <br><br>
                    What's really special about this is that no one server or company holds the backend of an application. Instead, it is forever in the blockchain 
                    and as long as you have its address and miners are working to append the transaction ledger, it will be avaiable. By mining a private blockchain in our network devices 
                    we can serve <a href="https://github.com/DavidJohnstonCEO/DecentralizedApplications" target="_blank">Ɖapps</a> without ever needing to leave our private network.
                </p>
                </div>

                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/team.svg" width="70px" height="70px">
                    <h3>Net neutrality</h3>
                </div>
                <p>
                    The repeal of net neutrality was purely motivated by the interests of big corporations looking to raise their profits without improving their services.
                    We believe access to internet is crucial to living in our modern world and limiting the access to such an essetial resource is not the way to way move forward.
                    <br><br>
                    Our technology aims to create a modern infrastructure that can provide quality internet without having to rely on big corporations.
                    We are committed to taking the internet ownership out of ISP giants and returning it to users.   
                </p>
                </div>

                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/secure.svg" width="70px" height="70px">
                    <h3>Security</h3>
                </div>
                <p>
                    All communication happenning between our devices follows military encryption standards so you can be certain your data will not be compromised on it's way to hosts.
                    <br><br>
                    In addition to that our push to implement decentralized applications on our blockchain are an effort to increase reliability and security from service providers. 
                </p>
                </div>

                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/web_config.svg" width="70px" height="70px">
                    <h3>Web Services</h3>
                </div>
                <p>
                    Our true goal is to push internet to the next level. 
                    By creating this network we have an opportunity empower many business by giving them the necessary tools to implement real world solutions harnessing of the blockchain.
                    <ol>
                        <li>Developer cli</li>
                            <ul><li>Develop and test projects on your own machine.</li></ul>
                        <li>Ɖapp deployer</li>
                            <ul><li>Deploy your dapps on our network for the best performance and reliability for our users.</li></ul>
                        <li>Activity monitorying</li>
                            <ul><li>Monitor you application's transactions on our network in real time.</li></ul>
                    </ol> 
                </p>
                </div>

                <div class="text-container">
                    <div class="text-title-container">
                    <img src="static/timeline.svg" width="70px" height="70px">
                    <h3>Our timeline</h3>
                </div>
                <p style="color:grey">Coming soon...</p>
                </div>




                <!-- endof -->
            </div>
            <div class="pure-hidden-phone pure-u-md-2-24 pure-u-lg-2-24">
                <!-- SPACING -->
            </div>
            <div class="pure-u-1 pure-u-md-8-24 pure-u-lg-8-24 quick-action-panel">
                <center class="pure-hidden-desktop">
                    <button class="main-action" v-for="x in mainActions" :key="x.name" :style="x.style" v-on:click="hello(x.name)">{{x.label}}</button>
                </center>
                <div class="pure-hidden-phone">
                    <button class="main-action" v-for="x in mainActions" :key="x.name" :style="x.style" v-on:click="hello(x.name)">{{x.label}}</button>
                </div>
                </div>
        </div>

    </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    
    #main-container{
        margin-bottom: 5em;
    }

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
        color: whitesmoke;
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
        background-color: rgb(238, 238, 238);
    }

    img, h3{
        display: inline-block;
        vertical-align: -webkit-baseline-middle;
    }

    .text-container{
        padding: 1em;
        padding-left: 3em;
        padding-top: 3em;
    }

    img{
        margin-right: 1em;
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
