<template>
  <div data-spy="scroll" data-offset="80">
    <Loader />
    <HeaderStyle1
      :logo-img="logo"
      :nav-item-list="navItems"
      :styled-logo="styleLogo"
    />
    <nuxt />
  </div>
</template>
<script>
import logoImg from "../assets/images/logo_horie.png";
import { menu } from "~/config/constant";
export default {
  name: "LandingPage1",
  data() {
    return {
      styleLogo: false,
      logo: logoImg,
      navItems: [
        {
          href: "#iq-home",
          title: "Home",
          active: true,
          children: true,
          child: menu,
        },
        { href: "#how-it-works", title: "Sobre nós" },
        { href: "#software-features", title: "Serviços" },
        /* { href: '#great-screenshots', title: 'Screenshots' }, */
        { href: "#pricing", title: "Preços" },
        { href: "#team", title: "Team" },
        { href: "#blog", title: "Blog" },
        { href: "#contact-us", title: "Contate-nos" },
      ],
    };
  },
  mounted() {},
  head() {
    return {
      bodyAttrs: {
        "data-spy": "scroll",
        "data-offset": "80",
      },
    };
  },
};
</script>
<style>
@import url("../assets/css/color/style.css");
.wow {
  visibility: hidden;
}
@keyframes fadeInUp {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, 30%, 0);
    -ms-transform: translate3d(0, 30%, 0);
    transform: translate3d(0, 30%, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    -ms-transform: none;
    transform: none;
  }
}

.fadeInUp {
  animation-name: fadeInUp;
  animation-timing-function: ease-out;
}
</style>
