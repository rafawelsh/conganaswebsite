<template>
  <div class="container">

    <div class="hero">
      <div class="heroBanner">
        <p><span>Porque Nos Dijeron</span></p>
        <p><span>Que No Podiamos</span></p>
      </div>
    </div>

    <div class="firstDesign">
      <div class="soldout">
        <h2>First Design</h2>
        <h3>Sould Out</h3>
      </div>
      <div class="sold"></div>
    </div>

    <div class="profiles">
      <div class="one">
        <p>Celebrating Latinx People.</p>
      </div>
      <div class="two">
        <p>Showcasing Our Identities.</p>
      </div>
      <div class="three">
        <p>For Everyone To Embrace.</p>
      </div>
    </div>
    <div class="things">
      <HelloWorld msg="Welcome to Your Vue.js App" />
    </div>
  </div>
      <!-- <img alt="Vue logo" src="../assets/hero.jpg" /> -->
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>

<style lang="scss">
  @mixin parallax {
    background-attachment: fixed;
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
  };

  @mixin centerFlex($align-items) {
    display: flex;
    justify-content: center;
    align-items: $align-items;
  }
  .hero {
    background-image: url("../assets/hero.jpg");
    height: 90vh;
    @include parallax();
    @include centerFlex(flex-end);
    
    .heroBanner {
      text-transform: uppercase;
      padding-bottom: 4rem;
        p {
          line-height: 1.1;
          color: white;
        }
        span {
          font-size: 2rem;
          background-color: rgba(40, 39, 40);
        }
    }
  }

  .firstDesign {
    display: grid;
    grid-template-columns: 1fr 1fr;
    height: 100vh;
    

    .soldout {
      background: rgba(40, 39, 40);
      color: white;
      @include centerFlex(center);
      flex-direction: column;
      line-height: 0.2;
        h2{
          font-size: 5rem;
        }
        h3{
          font-size: 3rem;
        }
    };

    .sold {
      background-image: url("../assets/soldout.jpg");
      background-size: cover;
      background-position: right;
    };

  }

  .profiles {
    @include centerFlex(center);
    height: 50vh;
    width: 100%;
    padding: 0.5rem 0rem;
    
    .one {
      background-image: url('../assets/raniprofile.jpg');
      background-size: cover;
      background-position: center;
      height: inherit;
      width: inherit;

      &:hover {
      opacity: 0.8;
      display: block;
      height: inherit;
      width: inherit;
      }
    }

    
            // p {
            //   color: white;
            //   position: relative;
            //   transform: translateY(10rem);
            // };
        

    .two {
      background-image: url('../assets/ryanprofile.jpg');
      background-size: cover;
      background-position: center;
      height: inherit;
      width: inherit;
    }

    .three {
      background-image: url('../assets/melanieprofile.jpg');
      background-size: cover;
      background-position: center;
      height: inherit;
      width: inherit;
    }
    
  }
</style>