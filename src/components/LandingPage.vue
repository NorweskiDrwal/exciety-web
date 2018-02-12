<template>
  <v-app>

    <div id="main">
      <div id="main__wrap">
        <v-layout row wrap>
          <v-flex xs12 class="text-xs-center">
            <h1><span>F</span>OSTER <span>Y</span>OUR <span>E</span>XCIETIES</h1>
            <h2>share your favorite hobbies with <span>Exciety</span></h2>
          </v-flex>
          <v-flex xs12 sm6 class="text-sm-right text-xs-center">
            <v-btn large to='' round :ripple="{ class: 'color--ripple' }">
              <v-icon left>fa-apple</v-icon>
              apple iOS
            </v-btn>
          </v-flex>
          <v-flex xs12 sm6 class="text-sm-left text-xs-center">
            <v-btn large to='' round :ripple="{ class: 'color--ripple' }">
              <v-icon left>android</v-icon>
              android
            </v-btn>
          </v-flex>     
        </v-layout>   
      </div>
    </div>

    <div id="about">
      <div id="about__wrap"> 
        <h1><span>W</span>hat is <span>E</span>xciety?</h1>
        <v-layout row wrap>
          <v-flex xs12 sm6 class="text-sm-left text-xs-center">
          </v-flex>
          <v-flex xs12 sm6 class="text-sm-left text-xs-center">
            <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
          </v-flex>     
        </v-layout>         
      </div>
    </div>  

  </v-app>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

  #main {
    background-image: linear-gradient(rgba(0,0,0,0.3)), url('../assets/tlo_tlo.jpg');
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    height: 100vh;
    width: 100vw;

    #main__wrap {
      height: auto;
      width: 100%;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      
      .btn__content::before {opacity: 0;}
      .color--ripple {color:$orange;}
      i {color: $orange;}

      h1 {
        color: #f5f5f5;
        font-size: 70px;
        margin-bottom: 0px;
        font-weight: 600;

        span {color: $orange; font-size:85px; font-weight: 800;}
      }

      h2 {
        color: #fff;
        font-size: 25px;
        margin-top: -10px; 
        margin-bottom: 25px;
        text-transform: uppercase;

        span {color: $orange; font-size:35px; font-weight: 800;}
      }

    }

  }

  #about {
    height: auto;
    padding: 40px;
    width: 100vw;

    #about__wrap {
      text-align: center;

      h1 {
        color: $blue;
        text-transform: uppercase;

        span {
          color: $orange;
          font-size: 40px;
        }
      }
    }
  }  

</style>
