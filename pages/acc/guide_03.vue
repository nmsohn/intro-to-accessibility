<template>
  <div id="guide-01">
    <div class="guide_wrap">
      <h1 id="page-title">{{ title }}</h1>
    </div>
    <div class="wrap_content">
      <v-container>
        <div class="wrap_link_back">
          <a href="/" class="link_back">Go back to home</a>
        </div>
        <v-row>
          <v-col lg="2" sm="6">
            <div id="submenu" class="sub_menu fl">
              <v-navigation-drawer floating permanent>
                <v-list dense rounded>
                  <v-list-item
                    v-for="item in items"
                    :key="item.title"
                    link
                    :to="item.link"
                  >
                    <v-list-item-content>
                      <v-list-item-title class="text-h6">{{
                        item.title
                      }}</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-navigation-drawer>
            </div>
          </v-col>

          <v-col>
            <div id="subcontent">
              <ul class="list_glines">
                <li>
                  <h2>{{ title }}</h2>
                  <br />
                  <p>
                    Text that is not ‘large scale’ must a contrast ratio of at
                    least 4.5:1 against its background.
                  </p>
                  <br />
                </li>
                <li>
                  <div class="wrap_txt">
                    <p class="txt_list">
                      <strong>Colour constrast assessment tools</strong>
                    </p>
                    <div class="txt_ex">
                      <ol class="list_num">
                        <li>
                          Recommended tools:
                          <ul class="list_cca">
                            <li>
                              -
                              <a
                                href="http://www.colorsontheweb.com/Color-Tools/Color-Contrast-Analyzer"
                                target="_blank"
                                >Colour Contrast Analyzer</a
                              >
                            </li>
                            <li>
                              -
                              <a
                                href="https://snook.ca/technical/colour_contrast/colour.html#fg=33FF33,bg=333333"
                                target="_blank"
                                >Colour Contrast Check</a
                              >
                            </li>
                            <li>
                              -
                              <a
                                href="https://developer.paciellogroup.com/resources/contrastanalyser/"
                                target="_blank"
                                >Contrast Analyser</a
                              >
                            </li>
                            <li>
                              -
                              <a
                                href="http://juicystudio.com/services/luminositycontrastratio.php"
                                target="_blank"
                                >Colour Contrast</a
                              >
                            </li>
                            <li>
                              -
                              <a
                                href="http://nuli.navercorp.com/sharing/a11y/tool#cr"
                                target="_blank"
                                >Contrast Ratio</a
                              >
                            </li>
                          </ul>
                        </li>
                        <br />
                      </ol>
                    </div>
                  </div>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
                <li>
                  <v-row>
                    <div class="wrap_txt">
                      <p class="txt_list">
                        Visual information required to identify user interface
                        components (like the border or background of a text
                        input field), and what state they’re in (like focused,
                        or in error), must have a 3:1 contrast ratio against
                        adjacent colors.
                      </p>
                    </div>
                  </v-row>
                  <v-row>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <strong>OK</strong>
                      <figure>
                        <img
                          src="../../static/icon_1411_success.png"
                          height="80"
                        />
                        <figcaption>
                          <div>
                            It's clear that this icon represents Facebook,
                            because the Facebook logo uses enough colour
                            contrast.
                          </div>
                        </figcaption>
                      </figure>
                    </v-col>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <strong>Fail</strong>
                      <figure>
                        <img src="../../static/icon_1411_fail.png" height="80" />
                        <figcaption>
                          <div>
                            It's not visible enough that this icon represents
                            Facebook, because the colour contrast between the
                            green and the white is not sufficient.
                          </div>
                        </figcaption>
                      </figure>
                    </v-col>
                  </v-row>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
              </ul>
            </div>
          </v-col>
          <v-col lg="2"></v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: "Guide_03",

  data() {
    return {
      title: "Colour and contrast",
      items: [
        { title: "Text alternative", link: "guide_01" },
        { title: "Video transcript", link: "guide_02" },
        { title: "Colour and contrast", link: "guide_03" },
        { title: "Keyboard", link: "guide_04" },
        { title: "Error identification", link: "guide_05" },
      ],
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
  background: url("../../static/top-section.jpg") center top no-repeat;
}

.sub_menu {
  margin: 0 70 px 0 0;
  display: block;
}

.sub_menu aside {
  margin-top: 30px;
}

.blind,
caption {
  position: absolute;
  top: -99999 px;
  width: 0;
  height: 0;
  overflow: hidden;
}

ol,
ul {
  list-style: none;
}

.sub_ct {
  padding: 10 px 0 140 px 0;
  width: 880 px;
  display: block;
}

.sub_menu nav li {
  margin: 10 px 0;
}

.sub_menu nav li a {
  display: block;
  color: #222;
  font-size: 18px;
  padding: 5 px 30 px;
}

.list_glines li .wrap_txt {
  width: 600 px;
  display: table-cell;
}

.list_glines li .wrap_img {
  display: table-cell;
  vertical-align: middle;
  padding: 0 0 0 40 px;
  text-align: center;
}

.wrap_img img {
  object-fit: cover;
  max-width: 100%;
  height: auto;
}

.list_glines .wrap_txt .txt_ex {
  width: 500px;
  margin: 20 px 0 0;
  padding: 10 px 20 px;
  color: #222;
  font-size: 16px;
  line-height: 1.6em;
  background: #f5f5f5;
  background-repeat: no-repeat;
}
</style>