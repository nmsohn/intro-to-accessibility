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
                  <h2>{{title}}</h2>
                  <br />
                  <p>
                    For people who use speech input software or screen readers,
                    provide alternate text so they can perceive information
                    convyed via images.
                  </p>
                  <br />
                </li>
                <li>
                  <v-row>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          Make sure all image elements (img) have alternate text
                          values (alt).
                        </p>
                        <pre
                          class="txt_ex"
                        ><code>&lt;img src="160314.png" <span class="c_red">alt="Accessibility for everyone"</span>&gt;</code></pre>
                      </div>
                    </v-col>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_img">
                        <img
                          src="../../static/read-this.png"
                          alt="image with alternative text"
                        />
                      </div>
                    </v-col>
                  </v-row>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
                <li>
                  <v-row>
                    <v-col xl="12" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          If background image, put an empty value e.g.
                          &lt;alt=""&gt; so the screen reader does not read the
                          image.
                        </p>
                        <pre
                          class="txt_ex"
                        ><code>&lt;img src="160314.png" <span class="c_red">alt=""</span>&gt;</code></pre>
                      </div>
                    </v-col>
                    <v-col xl="12" lg="12" md="12" sm="12">
                      <div class="">
                        <img
                          src="https://business.z.co.nz/_assets/media/home_terminal-gate-pricing.jpg"
                          alt="background image"
                        />
                      </div>
                    </v-col>
                  </v-row>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
                <li>
                  <v-row>
                    <v-col col="6" xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          Image information such as QR code or barcode should
                          provide url in alternate text (alt).
                        </p>
                        <pre
                          class="txt_ex"
                        ><code>&lt;a href="<span class="c_red">url.com</span>"&gt;&lt;img src="" alt="<span class="c_red">a link to url.com</span> QR code" width="150"<br>height="110"&gt;&lt;/a&gt;</code></pre>
                      </div>
                    </v-col>
                    <v-col col="6" xl="6" lg="12" md="12" sm="12">
                      <div class="">
                        <img src="../../static/qr.png" alt="QR code" />
                      </div>
                    </v-col>
                  </v-row>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
                <li>
                  <v-row>
                    <v-col col="6" xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          Provide alternate text in input element such as
                          buttons
                        </p>
                        <pre
                          class="txt_ex"
                        ><code>&lt;input type="image" src="next.gif" alt= "<span class="c_red">View more</span>"&gt;</code></pre>
                      </div>
                    </v-col>

                    <v-col col="6" xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_img">
                        <img
                          src="../../static/icon-menu.jpg"
                          alt="menu with icon buttons"
                        />
                      </div>
                    </v-col>
                  </v-row>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
                <li>
                  <v-row>
                    <v-col col="6" xl="6" lg="12" md="12" sm="12">
                      <p class="txt_list">
                        If an image CAPTCHA is used, provide, provide an
                        additional way to read the text information. Given the
                        accessibility issues with CAPTCHAs, Government
                        organisations are encouraged to avoid them where
                        possible and instead implement a number of alternative
                        techniques to prevent or reduce access by bots.
                      </p></v-col
                    >
                    <v-col col="6" xl="6" lg="12" md="12" sm="12">
                      <p class="txt_ex">
                        <img
                          src="../../static/captcha.png"
                          alt="CAPTCHA image with audio support"
                        /></p
                    ></v-col>
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
  name: "Guide_01",

  data() {
    return {
      title: "Text Alternative",
      items: [
        { title: "Text alternative", link: "guide_01" },
        { title: "Video transcript", link: "guide_02" },
        { title: "Color and contrast", link: "guide_03" },
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
</style>