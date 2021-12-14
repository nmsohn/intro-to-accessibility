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
                    It’s both a human right and a government mandate to make
                    videos accessible to disabled people. Accessible videos
                    improve usability for everyone and are more likely to appear
                    in search results.
                  </p>
                  <br />
                </li>
                <li>
                  <v-row>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          Audio-only content that communicates information (like
                          a podcast) should have a text transcript.
                        </p>
                      </div>
                    </v-col>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_img">
                        <img
                          src="../../static/transcript.png"
                          alt="video transcript"
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
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          Pre-recorded video content (like instructional videos,
                          ads or interviews), as well as live broadcast video,
                          must have captions that are synchronised with the
                          audio content of the video.
                        </p>
                      </div>
                    </v-col>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="">
                        <img
                          src="../../static/caption.jpg"
                          alt="background image"
                        />
                      </div>
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
  name: "Guide_02",

  data() {
    return {
      title: "Video transcript",
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