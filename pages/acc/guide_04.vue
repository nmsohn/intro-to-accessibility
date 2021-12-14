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
                    Many people don’t rely on a mouse, trackpad or touchscreen
                    to use websites. It must be possible for someone using only
                    a keyboard to access all content and complete all tasks.
                  </p>
                  <br />
                </li>
                <li>
                  <v-row>
                    <v-col xl="12" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          When navigated sequentially using the ‘Tab’ key,
                          interactive elements should receive focus in a
                          predictable, natural reading order (from left to right
                          and top to bottom, in most cases).
                        </p>
                        <pre
                          class="txt_ex"
                        ><code>`Tab` key to move next. `Shift+Tab` key to go back</code></pre>
                      </div>
                    </v-col>
                    <v-col xl="12" lg="12" md="12" sm="12">
                      <div class="wrap_img">
                        <img
                          src="../../static/consistent-focus.png"
                          alt="consistent focus"
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
                    <v-col>
                      <p>
                        Place interactive elements in the Document Object Model
                        in an order that makes sense for users who navigate
                        interactive elements sequentially, like screen reader,
                        Switch control and keyboard users
                      </p>
                      <p><strong>Code examples</strong></p>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col xl="12" lg="12" md="12" sm="12">
                      <pre
                        class="highlight"
                      ><code><span class="nt">&lt;div&gt;</span>
  <span class="nt">&lt;h3&gt;</span>Shipping Address<span class="nt">&lt;/h3&gt;</span>
  <span class="nt">&lt;label</span> <span class="na">for=</span><span class="s">"n1"</span><span class="nt">&gt;</span>Name<span class="nt">&lt;/label&gt;&lt;input</span> <span class="na">type=</span><span class="s">"text"</span> <span class="nt">/&gt;</span>
  <span class="nt">&lt;label</span> <span class="na">for=</span><span class="s">"a1"</span><span class="nt">&gt;</span>Address<span class="nt">&lt;/label&gt;&lt;input</span> <span class="na">type=</span><span class="s">"text"</span> <span class="nt">/&gt;</span>
  ...
<span class="nt">&lt;/div&gt;</span>
<span class="nt">&lt;div&gt;</span>
  <span class="nt">&lt;h3&gt;</span>Billing Address<span class="nt">&lt;/h3&gt;</span>
  <span class="nt">&lt;label</span> <span class="na">for=</span><span class="s">"n2"</span><span class="nt">&gt;</span>Name<span class="nt">&lt;/label&gt;&lt;input</span> <span class="na">type=</span><span class="s">"text"</span> <span class="nt">/&gt;</span>
  <span class="nt">&lt;label</span> <span class="na">for=</span><span class="s">"a2"</span><span class="nt">&gt;</span>Address<span class="nt">&lt;/label&gt;&lt;input</span> <span class="na">type=</span><span class="s">"text"</span> <span class="nt">/&gt;</span>
  ...
<span class="nt">&lt;/div&gt;</span>
</code></pre>
                    </v-col>
                  </v-row>
                </li>
                <br />
                <v-divider></v-divider>
                <br />
                <li>
                  <v-row>
                    <v-col>
                      <p class="txt_list">
                        Do not use positive values with tabindex.
                      </p></v-col
                    >
                  </v-row>
                  <v-row>
                    <v-col>
                      <pre
                        class="highlight"
                      ><code><span class="nt">&lt;h1</span> <span class="na">tabindex=</span><span class="s">"-1"</span><span class="nt">&gt;</span>I'm the heading for a modal dialog<span class="nt">&lt;/h1&gt;</span>
...
<span class="nt">&lt;div</span> <span class="na">tab-index=</span><span class="s">"0"</span> <span class="na">class=</span><span class="s">"fake_button"</span> <span class="na">aria-role=</span><span class="s">"button"</span><span class="nt">&gt;</span>Button Label<span class="nt">&lt;/div&gt;</span>
</code></pre>
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
  name: "Guide_01",

  data() {
    return {
      title: "Keyboard",
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

.highlight {
  background-color: #f8f8f8;
}

.highlight code {
  background-color: #f8f8f8;
}
</style>