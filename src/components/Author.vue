<template>
  <div class="author">
    <p class="author__intro">Our thoughts and musing about projects we're working on.</p>

    <p class="author__links">
      <a href="//twitter.com/hellofarnsco" target="_blank">
        <font-awesome-icon class="fa-2x social-link" :icon="['fab', 'twitter']" />@hellofarnsco
      </a>
      <a href="//instagram.com/hellofarnsco" target="_blank">
        <font-awesome-icon class="fa-2x social-link" :icon="['fab', 'instagram']" />@hellofarnsco
      </a>
    </p>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ["showTitle"]
};
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 600px;
  text-align: center;
  padding: calc(var(--space) / 2) 0;

  &__image {
    border-radius: 100%;
    width: 90px;
    height: 90px;
    margin-bottom: 1em;
  }

  &__intro {
    opacity: 0.8;
  }

  &__site-title {
    font-size: 1.5em;
  }

  &__links {
    margin-top: -0.5em;
    vertical-align: middle;
    a {
      margin: 0 0.5em;
      .social-link {
        vertical-align: middle;
        margin-right: 5px;
      }
    }
  }
}
</style>