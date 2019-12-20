<template>
  <div>
    <div id="overview">
      <day-select v-bind:selected="day"></day-select>
      <div class="main">
        <movie-list v-bind:day="day" v-bind:movies="movies" v-bind:genre="genre" v-bind:time="time"></movie-list>
        <movie-filter></movie-filter>
      </div>
    </div>
  </div>
</template>

<script>
import MovieList from "./MovieList.vue";
import MovieFilter from "./MovieFilter.vue";
import DaySelect from "./DaySelect.vue";

export default {
  components: {
    MovieList,
    MovieFilter,
    DaySelect
  },
  props: ["genre", "time", "movies", "day"]
};
</script>