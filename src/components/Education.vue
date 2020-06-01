<template lang="html">

  <section class="education-container">
    <h2 class="bottom-line-headline no-mar-bottom">Education</h2>
    <div class="degree-container dotted-shadow-separated">
      <div class="left-side">
        <span class="degree">Computer Science Engineering</span>
        <span class="university">University of Valladolid</span>
      </div>
      <div class="right-side">
        <span class="dates">2003-2012</span>
      </div>
    </div>
  </section>

</template>

<script lang="js">
  export default  {
    name: 'education',
    data() {
      return {

      }
    }
}
</script>

<style scoped lang="scss">
  .education-container {
    .degree-container {
      display: flex;
      text-align: left;
      padding-top: 1rem;
      .left-side {
        flex-basis: 80%;
        display: flex;
        flex-wrap: wrap;
        .degree {
          margin-bottom: 0.5rem;
          font-size: 1.1rem;
          flex-basis: 100%;
          font-weight: 600;
        }
        .university {
          font-size: 1rem;
          font-style: italic;
        }
      }
      .right-side {
        flex-basis: 20%;
        text-align: right;
        .dates {
          font-size: 0.8rem;
          font-style: italic;
        }
      }
    }
  }
</style>
