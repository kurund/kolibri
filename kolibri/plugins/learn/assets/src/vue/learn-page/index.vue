<template>

  <div>
    <div v-for="(title, block) in contents">
      <h1>{{ title }}</h1>
      <div class="card-list">
        <content-card
          v-for="content in block"
          class="card"
          linkhref="#"
          :title="content.title"
          :thumbsrc="content.thumbnail"
          :kind="content.kind"
          :progress="content.progress"
          :pk="content.id">
        </content-card>
      </div>
    </div>
  </div>

</template>


<script>

  module.exports = {
    components: {
      'content-card': require('../content-card'),
    },
    vuex: {
      getters: {
        // better practice would be to define vuex getter functions globally
        contents: state => state.recommended,
      },
    },
  };

</script>


<style lang="stylus" scoped>

  @require '~core-theme.styl'

</style>
