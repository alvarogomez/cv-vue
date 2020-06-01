<template lang="html">

  <section v-bind:class="{ inverse: inverse }" class="separator-container">
    <div class="separator solid"></div>
    <div class="separator dotted"></div>
  </section>

</template>

<script lang="js">
  export default  {
    name: 'separator',
    props: {
      inverse: Boolean,
    }
  }
</script>

<style scoped lang="scss">
@import '../styles/common';
.separator-container {
  display: flex;
  margin-left: -1rem;
  margin-right: -1rem;
  @media (min-width: 768px) {
    margin-left: 0;
    margin-right: 0;
  }
  &.inverse {
    .separator {
      &.solid {
        flex-basis: 90%;
      }
      &.dotted {
        flex-basis: 10%;
      }
    }
  }
  .separator {
    flex-wrap: nowrap;
    &.solid {
      flex-basis: 90%;
      border-bottom: $separators-width solid $separators-color;
    }
    &.dotted {
      flex-basis: 10%;
      border-bottom: $separators-width dotted $separators-color;
    }
  }
}
</style>
