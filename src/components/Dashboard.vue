<template>
  <div class="dashboard">
  Hello {{username}}
  </div>
</template>

<script>
export default {
  name: 'dashboard',
  data() {
    return {
      username: this.$env.get('USERNAME'),
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
