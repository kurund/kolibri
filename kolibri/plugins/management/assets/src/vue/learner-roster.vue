<template>

  <div class="roster">
    <input type="search" placeholder="Search for learner...">
    <div>
      <button>+ Learner</button>
      <button>A-Z</button>
      <button>Z-A</button>
    </div>
    <div class="learner-roster">
      <ul>
        <li v-for="learner in learners">
          <input type="checkbox">
          <span class="vertical-divider">|</span>
          <a href="#">{{ learner.last_name + ", " + learner.first_name }}</a>
          <button>Manage</button>
        </li>
      </ul>
    </div>
  </div>
  <div class="sidebar">
    <div class="learner-count">
      <div>Total:</div>
      <div>{{ learners.length }}</div>
    </div>
  </div>

</template>


<script>

  module.exports = {
    props: {
      learners: {
        type: Array,
        default: () => [{
          last_name: 'Default',
          first_name: 'Value',
        }],
      },
    },
  };

</script>


<style lang="stylus" scoped>

  .roster, .sidebar
    display: inline-block

  .learner-count
    border: solid, 1px, black

</style>
