<template>
  <section class="second-section">
    <div class="wrap_list_acc_guide">
      <p class="title-02">Design/UX</p>
      <ul class="list_acc_glines">
        <li class="acc_glines_01">
          <dl>
            <dt>
              <a href="/acc/guide_01"
                ><strong class="title">Text alternative</strong>
              </a>
            </dt>
            <dd>
              Provide alternative text for images. Make sure it conveys the same
              message.
            </dd>
          </dl>
        </li>
        <li class="acc_glines_02">
          <dl>
            <dt>
              <a href="/acc/guide_02"
                ><strong class="title">Video transcript</strong></a
              >
            </dt>
            <dd>
              It’s both a human right and a government mandate to make videos
              accessible to disabled people.
            </dd>
          </dl>
        </li>
        <li class="acc_glines_03">
          <dl>
            <dt>
              <a href="/acc/guide_03"
                ><strong class="title">Colour and contrast</strong></a
              >
            </dt>
            <dd>
              It’s important to consider how you use colour in your online
              content (web pages, PDFs, or other online material) <br />
              to ensure that people with colour blindness, colour vision
              deficiencies, partial sight or low vision, can access all the
              information in that content.
            </dd>
          </dl>
        </li>
        <li class="acc_glines_04">
          <dl>
            <dt>
              <a href="/acc/guide_04"
                ><strong class="title">Keyboard</strong></a
              >
            </dt>
            <dd>
              Make sure every task can be completed using just the keyboard.
            </dd>
          </dl>
        </li>
        <li class="acc_glines_05">
          <dl>
            <dt>
              <a href="/acc/guide_05"
                ><strong class="title">Error identification</strong></a
              >
            </dt>
            <dd>
              When someone makes a mistake filling in a form, they should be
              able to identify where the error is, and describe it in text
            </dd>
          </dl>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
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