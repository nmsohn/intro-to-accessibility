<template>
  <div>
    <div class="hero">
      <TopSection />
    </div>
    <div class="accessibility-1">
      <SecondSection />
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style lang="scss" scoped>
.hero {
  position: relative;
  height: 650px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background: url("../static/top-section.jpg") center top no-repeat;
}

.accessibility-1 {
  margin: 0 auto;
  position: relative;
  background: #fff;
  margin: 0 auto;
}
</style>