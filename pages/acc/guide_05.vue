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
                    When a form validation error occurs, the user is informed of
                    where the error is, and what caused it, using text. This
                    ensures that the form validation error is available to
                    people who cannot see, distinguish colours, or understand
                    icons and other visual cues.
                  </p>
                  <br />
                </li>
                <li>
                  <v-row>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_txt">
                        <p class="txt_list">
                          Each form validation error should be described with
                          text, and the form input that is in error is in error
                          is clearly identified.
                        </p>
                      </div>
                    </v-col>
                    <v-col xl="6" lg="12" md="12" sm="12">
                      <div class="wrap_img">
                        <img
                          src="../../static/validation.png"
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
                    <v-col>
                      <p class="txt_list">
                        Associate an error with a text input field using
                        aria-describedby
                      </p>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col>
                      <pre
                        class="highlight"
                      ><code><span class="nt">&lt;label</span> <span class="na">for=</span><span class="s">"national-insurance-number"</span><span class="nt">&gt;</span>
  National Insurance number
<span class="nt">&lt;/label&gt;</span>

<span class="nt">&lt;span</span> <span class="na">id=</span><span class="s">"national-insurance-number-hint"</span><span class="nt">&gt;</span>
  It’s on your National Insurance card, benefit letter, payslip or P60. For
  example, ‘QQ 12 34 56 C’.
<span class="nt">&lt;/span&gt;</span>

<span class="nt">&lt;input</span>
  <span class="na">id=</span><span class="s">"national-insurance-number"</span>
  <span class="na">name=</span><span class="s">"national-insurance-number"</span>
  <span class="na">type=</span><span class="s">"text"</span>
  <span class="na">aria-describedby=</span><span class="s">"national-insurance-number-hint national-insurance-number-error"</span>
<span class="nt">/&gt;</span>

<span class="nt">&lt;span</span> <span class="na">id=</span><span class="s">"national-insurance-number-error"</span><span class="nt">&gt;</span>
  <span class="nt">&lt;span</span> <span class="na">class=</span><span class="s">"visually-hidden"</span><span class="nt">&gt;</span>Error:<span class="nt">&lt;/span&gt;</span> Enter a National Insurance number
  in the correct format
<span class="nt">&lt;/span&gt;</span>
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
  name: "Guide_05",

  data() {
    return {
      title: "Error Identification",
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