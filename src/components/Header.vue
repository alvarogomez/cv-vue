<template>
  <section class="cv-header">
    <h1>{{headline}}</h1>
    <span class="sub-headline">{{subHeadline}}</span>
  </section>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      showSeparator: false,
      showHeadlines: false,
      headline : 'Álvaro Gómez´s Curriculum Vitae',
      subHeadline: 'Senior Frontend Engineer'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '../styles/common';
  .cv-header {
    .sub-headline {
      display: block;
      margin-top: $texts-separation;
      text-align: left;
      font-size: 0.9rem;
      color: $light-black;
      font-style: italic;
    }
  }
</style>
