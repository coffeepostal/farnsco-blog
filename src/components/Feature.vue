<template>
  <div class="feature">
    <h1 v-if="showTitle" class="author__site-title">{{ $static.metaData.siteName }}</h1>
    <h1>
      FarnsCo
      <span>Project</span>
    </h1>
    <h2>Blog</h2>
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
.feature {
  background-image: url("../assets/images/cristofer-jeschke-1389563-unsplash.jpg");
  background-size: cover;
  padding: 200px;
  h1,
  h2 {
    color: white;
    text-transform: uppercase;
    margin: 0;
    padding: 0;
    line-height: 1;
    span {
      font-size: 70%;
    }
  }
  h2 {
    font-size: 80px;
    font-weight: 300;
  }
  @media screen and (max-width: 1010px) {
    padding: 100px 50px;

    h1,
    h2 {
      span {
        font-size: 100%;
      }
    }

    h2 {
      font-size: 60px;
    }
  }
}
</style>
