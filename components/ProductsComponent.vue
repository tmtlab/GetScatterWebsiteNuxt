<template>
    <section class="maximum-width" data-aos="fade-up" >
      <div class="products">
        <nuxt-link class="product wallets" :to="localePath('products-wallets')">
          <h2>{{ $t("productscomponent.wallets.title") }}</h2>
          <p>{{ $t("productscomponent.wallets.description") }}</p>
          <img src="@/assets/wallets.png">
        </nuxt-link>
        <nuxt-link class="product blockproducers" :to="localePath('products-blockproducers')">
          <h2>{{ $t("productscomponent.blockproduction.title") }}</h2>
          <p>{{ $t("productscomponent.blockproduction.description") }}</p>
          <img src="@/assets/blockproducers.png">
        </nuxt-link>
        <nuxt-link class="product developmenttools" :to="localePath('products-developmenttools')">
          <h2>{{ $t("productscomponent.developmenttools.title") }}</h2>
          <p>{{ $t("productscomponent.developmenttools.description") }}</p>
          <img src="@/assets/developmenttools.png">
        </nuxt-link>
        <!-- <nuxt-link class="product promotionalchannels" to="/products/promotionalchannels">
          <h2>Promotional Channels</h2>
          <p>We are providing unique experiences and channels for users and apps to find one another.</p>
          <img src="../../assets/promotionalchannels.png">
        </nuxt-link> -->
      </div>
    </section>
</template>

<script>

    export default {
        name: 'ProductsComponent',
    }

</script>

<style lang="scss">
    
    @import "@/assets/_variables.scss";

    .products {
            display:flex;
            flex-direction:row;
            flex-wrap: wrap;
            padding:0 2rem;
            margin:0 auto;

            .product {
              height:480px;
              width:calc(33.33% - 4rem);
              padding:4rem;
              margin:2rem;
              border-radius:10px;
              background-color:$blue;
              transition:box-shadow 0.12s ease-in-out;
              display:flex;
              text-align:left;
              flex-direction:column;
              justify-content:flex-end;
              text-decoration: none !important;
              background-position:left top;
              background-image:url('../assets/nebula_bg.jpg');
              position:relative;

              @media (max-width: $breakpoint-mobile) {
                padding:2rem;
              }

              img {
                position:absolute;
                width:60%;
                top:4rem;
                right:4rem;

                  @media (max-width: $breakpoint-small-desktop) {
                      width:40%;
                      top:2rem;
                      right:2rem;
                  }

                  @media (max-width: $breakpoint-tablet) {
                      width:35%;
                      top:2rem;
                      right:2rem;
                  }

                  @media (max-width: $breakpoint-mobile) {
                      width:50%;
                      top:1rem;
                      right:1rem;
                  }
              }

              @media (max-width: $breakpoint-small-desktop) {
                  width:100%;
                  margin:0 2rem 2rem;
                  height:360px;
              }

              @media (max-width: $breakpoint-tablet) {
                  width:100%;
                  margin:0 0rem 2rem;
              }

              &.wallets {
                background-position:right top;
              }

              &.developmenttools {
                background-position:center top;
              }

              &.blockproducers {
                background-position:left bottom;
              }

              &.promotionalchannels {
                background-position:left top;
              }

              &:hover {
                box-shadow:inset 0 0 0 10px lighten($blue,12%);
                z-index:1;
              }

              h2, p {
                color:white;
                text-decoration:none;
                max-width:60%;
              }


              h2 {
                margin-bottom:1rem;
              }
            }
        }


</style>