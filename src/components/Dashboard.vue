<template>
  <div class="dashboard">
  Hello {{username}}
  <weather 
        :api-key="this.$env.get('DARKSKY_API_KEY')"
        title="Weather For Pinner, UK"
        :latitude="this.$env.get('LAT')"
        :longitude="this.$env.get('LONG')"
        language="en"
        units="uk">
    </weather>
  </div>
</template>

<script>
import VueWeatherWidget from 'vue-weather-widget';
import 'vue-weather-widget/dist/css/vue-weather-widget.css';

export default {
  name: 'dashboard',
  data() {
    return {
      username: this.$env.get('USERNAME'),
    };
  },
  components: {
    weather: VueWeatherWidget,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
