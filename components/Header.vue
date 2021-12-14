<template>
  <div class="header">
    <v-app-bar app fixed :id="bg">
      <v-spacer />
      <nav id="navbar" role="navigation">
        <v-btn
          id="nav-item"
          v-text="item.title"
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          :aria-label="item.title"
        ></v-btn>
      </nav>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      bg: "app-bar-transparent",
      items: [
        {
          title: "Guide",
          to: "/",
        },
        {
          title: "Tools",
          to: "/tools",
        },
      ],
    };
  },
  mounted() {
    window.onscroll = () => {
      this.changeColor();
    };
  },
  methods: {
    changeColor() {
      if (
        document.body.scrollTop > 100 ||
        document.documentElement.scrollTop > 100
      ) {
        this.bg = "app-bar";
      } else {
        this.bg = "app-bar-transparent";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
#app-bar {
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background: url("../static/top-section.jpg") center top no-repeat;
}

#app-bar-transparent {
  background: transparent;
  box-shadow: none;
}

#nav-title {
  color: #fff;
}

#navbar {
  display: flex;
}

#nav-item {
  background-color: transparent;
  color: #fff;
  display: flex;
  box-shadow: none;
}

a.v-btn--active {
    border-bottom: 2 px solid #fff;
}

#nav-item.v-btn--active {
  border-bottom: 2 px solid #fff;
  background-color: white;
  color: black;
  opacity: 0.8;
}
</style>