<template lang="html">

  <section class="experience-container">
    <h2 class="bottom-line-headline no-mar-bottom">Experience</h2>
    <div class="experience-slot">
      <div class="company-and-role dotted-shadow-separated">
        <div class="left-side">
          <span class="role">Full Stack Developer</span>
          <span class="company">Zooplus A.G</span>
        </div>
        <div class="right-side">
          <span class="dates">(04/2017 -> Present)</span>
        </div>
      </div>
      <div class="explanation dotted-shadow-separated">
        <p>
          Development, styling and deployment of serverless components using node.js,
          serverless framework and AWS lambdas, integrating Contentful CMS as database.
        </p>
        <p>
          Design, styling and implementation of components for static pages of the Zooplus page.
        </p>
        <p>
          Design, styling and implementation of plugin-extensions for Contentful CMS using Vue.js or pure HTML+JS.
        </p>
        <p>
          Development of internal backoffice applications using Vue.js and Angular.
        </p>
      </div>
    </div>
    <div class="experience-slot">
      <div class="company-and-role dotted-shadow-separated">
        <div class="left-side">
          <span class="role">Frontend Developer</span>
          <span class="company">Tecnilógica S.L</span>
        </div>
        <div class="right-side">
          <span class="dates">(05/2014 -> 04/2017)</span>
        </div>
      </div>
      <div class="explanation dotted-shadow-separated">
        <p>
          Managment of project related to fashion sector. Coordination with client
          and design agencies, JS development of features.
        </p>
        <p>
          Development of an Hybrid JS application(Titanium) for buying parking tickets from the phone.
        </p>
        <p>
          CSS styling and JS development of websites related to travel sector.
        </p>
      </div>
    </div>
    <div class="experience-slot">
      <div class="company-and-role dotted-shadow-separated">
        <div class="left-side">
          <span class="role">Frontend and Mobile Apps Developer</span>
          <span class="company">Indicalsoft</span>
        </div>
        <div class="right-side">
          <span class="dates">(09/2012 -> 04/2014)</span>
        </div>
      </div>
      <div class="explanation dotted-shadow-separated">
        <p>
          Development of hybrid mobile apps(titanium) and pure Native iOS and Android apps,
          injecting HTML5 based games through webviews.
        </p>
        <p>
          Development of Django/Python backoffice applications.
        </p>
      </div>
    </div>
  </section>

</template>

<script lang="js">
export default  {
  name: 'experience',
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
@import '../styles/common';
  .experience-container {
    .experience-slot {
      .company-and-role {
        display: flex;
        text-align: left;
        padding-top: 1rem;
        .left-side {
          flex-basis: 60%;
          display: flex;
          flex-wrap: wrap;
          .role {
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
            flex-basis: 100%;
            font-weight: 600;
          }
          .company {
            font-size: 1rem;
            font-style: italic;
          }
        }
        .right-side {
          flex-basis: 40%;
          text-align: right;
          .dates {
            font-size: 0.8rem;
            font-style: italic;
          }
        }
      }
      .explanation {
        p {
          &:last-child {
            margin-bottom: 0;
          }
        }
        &.with-padding {
          padding: 0 1.25rem 1rem 1.25rem;
        }
      }
    }
  }
</style>
