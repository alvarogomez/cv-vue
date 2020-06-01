<template lang="html">

  <section class="personal-info-vue">
    <h2 class="bottom-line-headline">Personal Info</h2>
    <ul class="info-container dotted-shadow-separated">
      <li class="info">
        <a :href="'tel:'+ phoneNumber" title="Phone Number">
          <font-awesome-icon aria-hidden="true" class="icon" icon="mobile-alt"/>
          <span class="text">{{phoneNumber}}</span>
        </a>
      </li>
      <li class="info">
        <a :href="'mailto:' + mailAddress" title="Mail Address">
          <font-awesome-icon aria-hidden="true" class="icon" icon="at"/>
          <span class="text">{{mailAddress}}</span>
        </a>
      </li>
      <li class="info">
        <a :href="'https://' + githubUrl" title="Mail Address">
          <font-awesome-icon aria-hidden="true" class="icon" :icon="{ prefix: 'fab', iconName: 'github' }"/>
          <span class="text">{{githubUrl}}</span>
        </a>
      </li>
      <li class="info">
        <a :href="'https://www.' + linkedinUrl" title="Mail Address">
          <font-awesome-icon aria-hidden="true" class="icon" :icon="{ prefix: 'fab', iconName: 'linkedin' }"/>
          <span class="text">{{linkedinUrl}}</span>
        </a>
      </li>
    </ul>
  </section>

</template>

<script lang="js">
  export default  {
    name: 'personal-info-vue',
    props: [],
    mounted() {

    },
    data() {
      return {
        phoneNumber: '+34651510306',
        mailAddress: 'alvaro.gomez.sastre@gmail.com',
        githubUrl: 'github.com/alvarogomez',
        linkedinUrl: 'linkedin.com/in/alvarogomezsastre'
      }
    },
    methods: {

    },
    computed: {

    }
}
</script>

<style scoped lang="scss">
@import '../styles/common';
  .personal-info-vue {
    .info-container {
      .info {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        cursor: pointer;
        padding: $texts-separation 0;
        a {
          color: $black;
          text-decoration: none;
        }
        .icon {
          min-width: 20px;
          padding-right: $texts-separation;
          color: $icons-color;
        }
      }
    }
  }
</style>
