<template>
    <div class="text-center">
        <h2 class="text-3xl font-bold">{{text}}</h2>
        <div class="text-2xl mt-4 mb-10">
          <span class="bg-blue-100 text-gray-700 text-xl mt-2 mb-2 p-2 rounded">
            <em>Last Updated:</em>
          </span>
            {{timestamp}}
        </div>
    </div>
</template>

<script>
import moment from 'moment';

export default {
  name: 'DataTitle',
  props: ['text', 'dataDate'],
  computed: {
    timestamp() {
      return moment(this.dataDate).format('MMMM Do YYYY, hh:mm:ss a');
    },
  },
};
</script>
