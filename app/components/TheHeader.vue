<template>
  <header>
    <head>
      <link
        rel="stylesheet"
        href="https://use.fontawesome.com/releases/v5.6.3/css/all.css"
      />
    </head>
    <nav>
      <ul id="nav">
        <!-- <li>
          <span class="logo">
            <i class="fab fa-pied-piper-alt"></i>
          </span>
        </li> -->
        <li>
          <nuxt-link to="/"><i class="fas fa-home" /> HOME</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about"
            ><i class="far fa-meh-blank" /> ABOUT</nuxt-link
          >
        </li>
        <li>
          <nuxt-link to="/skills"><i class="fab fa-java" /> SKILLS</nuxt-link>
        </li>
        <!-- <li>
          <nuxt-link to="/contact"
            ><i class="far fa-envelope-open" /> CONTENTS</nuxt-link
          >
        </li> -->
      </ul>
    </nav>
  </header>
</template>
<script>
export default {
  transition: 'bounce',
  computed: {
    currentPage() {
      return this.$router.path
    }
  },
  watch: {
    currentPage: function(newValue) {
      alert(newValue)
    }
  }
}
</script>

<style scoped>
.logo {
  font-size: 20px;
}
#header {
  padding: 10px;
}
#nav {
  /* リスト項目の左にでる・を削除する */
  list-style-type: none;
  /* 横並びメニューをつくるためにflexにする */
  display: flex;
  justify-content: flex-end;
  font-family: 'Courier New', Courier, monospace;
}
#nav li {
  padding: 10px 22px;
  text-align: center;
}
#nav li a {
  /* aリンクの下線を削除 */
  text-decoration: none;
  font-weight: bold;
}
#nav li a:hover {
  opacity: 0.7;
}
.nuxt-link-exact-active {
  opacity: 0.7;
}
</style>
