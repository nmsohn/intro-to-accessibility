<template>
  <section class="top-section">
    <h1 class="top-title" aria-label="Accessibility Guide">Accessibility Guide</h1>
    <p class="top-content">
     Web accessibility is about inclusion — making sure everyone,
      <br />
      including disabled people and those using assistive
      <br />
      technologies, can access online information and services.
      <br />
      All public service and non-public service agencies must meet
      <br />
      the NZ Government Web Accessibility Standard 1.1
    </p>
    <div class="btn-wrapper">
      <v-btn href="https://www.digital.govt.nz/standards-and-guidance/design-and-ux/accessibility/" justify-center id="info-btn" aria-label="More Information" color="white">More information</v-btn>
    </div>
    
  </section>
</template>

<style lang="scss" scoped>
.top-visual {
  padding-top: 200px;
}

.top-title {
  text-align: center;
  overflow: hidden;
}

h1.top-title {
  height: 78px;
  color: #fff;
  display: block;
  font-size: 4em;
  font-weight: bold;
  margin-block-start: 0.83em;
  margin-block-end: 0.83em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
}

.top-content {
  text-align: center;
  color: #fff;
  font-size: 21px;
  line-height: 1.5;
  letter-spacing: -1px;
  margin: 0;
  padding: 0;
}

#info-btn {
  margin-top: 40px;
}

.btn-wrapper {
  text-align: center;
}

</style>