<template>
  <div id="tools">
    <div class="guide_wrap">
      <h1 id="page-title">{{ title }}</h1>
    </div>
    <div class="wrap_list_acc_guide">
      <p class="title-02">Tools</p>
      <ul class="list_acc_glines">
        <li class="acc_glines_01">
          <dl>
            <dt>
              <a href="https://github.com/microsoft/accessibility-insights-web"
                ><strong class="title">MS Accessibility Insights for Web & Android</strong>
              </a>
            </dt>
          </dl>
        </li>
        <li class="acc_glines_02">
          <dl>
            <dt>
              <a href="https://www.tpgi.com/color-contrast-checker/"
                ><strong class="title">TPGi Color Analyzer</strong></a
              >
            </dt>
          </dl>
        </li>
        <li class="acc_glines_03">
          <dl>
            <dt>
              <a href="https://github.com/IBMa/equal-access"
                ><strong class="title">IBM Equal Access</strong></a
              >
            </dt>
          </dl>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Tools",

  data() {
    return {
      title: "Tools",
    };
  },
};
</script>

<style lang="scss" scoped>
#guide-01 {
  position: relative;
}

#page-title {
  color: white;
}

v-content {
  padding: 34px 0 0 0;
}

#subcontent {
  margin-top: 40px;
}

.guide_wrap {
  position: relative;
  height: 350px;
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

.second-section {
  display: block;
}

.wrap_list_acc_guide {
  padding-top: 40px;
  padding-left: 40px;
}

.title-02 {
  color: #222;
  font-size: 38px;
  font-weight: normal;
  letter-spacing: -2px;
  padding-bottom: 20px;
}

ol,
ul {
  list-style: none;
}

a {
  text-decoration: none;
}

.list_acc_glines li dt strong.tit {
  display: inline-block;
  margin: 0 5 px 0 0;
  color: #222;
  font-size: 28px;
  vertical-align: middle;
}

.list_acc_glines li .btn_more {
  display: inline-block;
  padding: 7 px 10 px;
  color: #fff;
  font-size: 14px;
  vertical-align: middle;
  background: #757575;
}

ul {
  display: block;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 40px;
}

ul li {
  padding-bottom: 25px;
}

ul li a {
  color: black;
}

ul li a:hover {
  color: grey;
}
</style>