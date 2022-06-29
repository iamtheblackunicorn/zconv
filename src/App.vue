<!--
ZCONV by Alexander Abraham,
a.k.a. "The Black Unicorn", a.k.a. "Angeldust Duke".
Licensed under the MIT license.
-->

<!--
Using our component as a virtual DOM element
and adding some flowery stuff.
-->
<template>
 <!--Main heading.-->
 <h1>ZCONV</h1>

 <!--Main div holding the main component.-->
 <div class="content">
  <NumConverter/>
 </div>

</template>

<!--
Importing our component with Vue's help.
-->
<script>
// Importing the main component.
import NumConverter from './components/NumConverter.vue';

// Registering the main component.
export default {
  name: 'App',
  components: {
    NumConverter
  }
}
</script>

<!--
Styling our component.
-->
<style lang="scss">

// Importing one of my fonts.
@font-face{
  font-family: 'Lobster';
  src: url('https://blckunicorn.art/assets/fonts/Lobster.ttf') format('truetype');
}

// Setting up the app's style constants.
$stdPadding: 20px;
$stdFont: 'Lobster';
$bgColor: #FFACA5;
$stdBorderRadius: 25px;
$divGradientOne: #EA1573;
$divGradientTwo: #FF7BAC;
$contentColor: #FFFFFF;

/* DESKTOP SECTION START */
html, body {
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    margin: 0px;
    padding: 0px;
    background-color: $bgColor;
}
h1 {
    text-align: center;
    font-size: 50px;
    padding: $stdPadding;
    font-family: $stdFont;
    margin-top: 5vh;
    margin-bottom: 10px;
    margin-left: 0px;
    margin-right: 0px;
    color: $divGradientTwo;
}
div.content {
    margin: 0 auto;
    padding: $stdPadding;
    border-radius: $stdBorderRadius;
    margin-top: 0px;
    margin-bottom: 30px;
    padding: $stdPadding;
    background: linear-gradient(
        135deg,
        $divGradientOne, 
        $divGradientTwo
    );
}
p {
    text-align: left;
    color: $contentColor;
    font-size: 35px;
    padding: 0px;
    margin-right: 0px;
    margin-left: 0px;
    margin-top: 0px;
    margin-bottom: 10px;
}
button {
    width: 100%;
    padding: $stdPadding;
    text-align: center;
    color: $contentColor;
    font-size: 35px;
    padding: 0px;
    margin-right: 0px;
    margin-left: 0px;
    margin-top: 0px;
    margin-bottom: 10px;
    background-color: transparent;
    border: 4px solid $contentColor;
}
/* DESKTOP SECTION END */

/* RESPONSIVE SECTION START */
@media screen and (max-width: 800px) {
    $stdPadding: 10px;
    h1 {
        font-size: 30px;
        margin-top: 3vh;
    }
    div.content {
        margin-bottom: 20px;
    }
    p {
        font-size: 20px;
    } 
    button {
        font-size: 20px;
    }
}
/* RESPONSIVE SECTION END */
</style>
