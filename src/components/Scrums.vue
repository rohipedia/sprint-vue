<template>
  <div>
    <div class="row">
      <button class="btn btn-link" @click="toggleScrums()">{{ buttonLabel }}</button>
    </div>
    <div class="row" v-if="showScrums">
      <table class="table table-striped table-responsive">
        <thead>
          <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Iteration</th>
            <th>Feature</th>
            <th>Status</th>
            <th>Dependencies</th>
            <th>Release</th>
            <th>Branch</th>
            <th>Environment</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="scrum in scrums" :key="scrum.id">
            <td>{{ scrum.name }}</td>
            <td>{{ scrum.type }}</td>
            <td>{{ iteration }}</td>
            <td>{{ scrum.feature }}</td>
            <td class="status">
                <app-stories-status :status="scrum.status"></app-stories-status>
            </td>
            <td>{{ scrum.dependencies }}</td>
            <td>{{ scrum.release }}</td>
            <td>{{ scrum.branch }}</td>
            <td>{{ scrum.environment }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script>
/* eslint-disable */
import scrums from "../data/scrums.js";
import appStoriesStatus from './StoriesStatus.vue';
export default {
  data() {
    return {
      scrums: scrums,
      showScrums: true,
      buttonLabel: "Hide Scrums",
      iteration: 'PI34.3'
    };
  },
  components: {
      'appStoriesStatus': appStoriesStatus
  },
  methods: {
    toggleScrums() {
      this.showScrums = !this.showScrums;
      this.buttonLabel = this.showScrums ? "Hide Scrums" : "Show Scrums";
    }
  }
};
</script>
<style>
ul {
  list-style-type: none;
}

.status {
  font-size: 75%;
}

table {
  font-size: 90%;
}
</style>
