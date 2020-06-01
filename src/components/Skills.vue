<template lang="html">

  <section class="skills-container">
    <h2 class="bottom-line-headline">Skills</h2>
    <div class="skills-list">
      <div class="tech-skills dotted-shadow-separated">
        <h3 class="mar-bottom-small" >Technical Skills: </h3>
        <div class="skills-wrapper" :key="techKey" v-for="(techValue, techKey) in techSkills">
          <h4 class="mar-bottom-tiny">{{techKey}}: </h4>
          <ul>
            <li :key="value" v-for="value in techValue">
              {{value}}
            </li>
          </ul>
        </div>
      </div>
      <div class="languages dotted-shadow-separated">
        <h3 class="mar-bottom-small">Languages:</h3>
        <div :key="language" v-for="(language, langKey) in languages">
          <ul>
            <li>
              <span>{{langKey}}: </span><span>{{language}}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>

</template>

<script lang="js">
  export default  {
    name: 'skills',
    data() {
      return {
        techSkills: {
          'Javascript': ['ES6, ','Vue.js,','Vuex,','Node.js,','Angular,'],
          'Testing': ['Mocha','Chai','Sinon'],
          'Layout and Styling': ['HTML5,', 'CSS,', 'SASS,', 'Handlebars'],
          'Task Automatization': ['Webpack,', 'Gulp,', 'Jenkins'],
          'AWS Services':['S3,', 'Lambda,', 'Cloudfront,', 'API Gateway']
        },
        languages: {
          'Spanish': 'Native',
          'English': 'Full',
          'Italian': 'Professional'
        }
      }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/common';
  .skills-container {
    .skills-list {
      h4 {
        font-weight: 600;
      }
      .languages {
        padding-top: 1rem;
      }
      .skills-wrapper {
        padding-left: 0.5rem;
      }
      .tech-skills {
        padding-bottom: 0.25rem;
      }
      ul {
        display: flex;
        padding-left: 0.5rem;
        li {
          margin-right: 0.5rem;
          margin-bottom: 1rem;
          &:last-child {
            margin-right: 0;
          }
        }
      }
      .languages {
        ul {
          padding-left: 0.8rem;
          li {
            margin-bottom: 0.5rem;
            span {
              &:first-child {
                display: inline-block;
                text-align: left;
                min-width: 75px;
                font-weight: 600;
              }
            }
          }
        }
      }
    }
  }
</style>
