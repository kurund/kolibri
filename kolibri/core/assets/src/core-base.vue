<template>

  <div>
    <!-- <kolibri-nav></kolibri-nav> -->
    <main>
      <slot></slot>
    </main>
  </div>

</template>


<script>

  module.exports = {
    components: {
      'kolibri-nav': require('./navigation.vue'),
    },
  };

</script>


<style lang="stylus" scoped>

  @require '~core-theme.styl'

  main
    margin: 10px

  .base-header h1
    color: $core-action-normal
    text-align: center
    font-size: smaller

</style>
