<template>
    <router-view/>
</template>


<script>
export default {
  name: 'app'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Open+Sans:300,400,700');
@import url('https://fonts.googleapis.com/css?family=Anonymous+Pro');
@import url('https://unpkg.com/purecss@1.0.0/build/pure-min.css');
@import url('https://unpkg.com/purecss@1.0.0/build/grids-responsive-min.css');


body {
    font-family: 'Open Sans', sans-serif;
    padding: 0em;
}

@media (min-width:767px){
    .pure-visible-phone{display:none}
    .pure-visible-tablet{display:none}
    .pure-hidden-desktop{display:none}
}
@media (max-width:767px){
    .pure-hidden-phone{display:none}
    .pure-visible-desktop{display:none}
}
@media (min-width:768px) and (max-width:979px){
    .pure-hidden-tablet{display:none}
    .pure-visible-desktop{display:none}
}

</style>
