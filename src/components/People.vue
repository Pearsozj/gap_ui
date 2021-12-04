<template>
  <ul>
        <li
          v-for="person in people"
          :key="person.id"
        >
          {{ person.first_name }} {{ person.last_name }} {{person.email}}
        </li>
  </ul>
</template>

<script>
import api from '@/services/api'
export default {
  name: 'People',
  data: () => ({
    people: []
  }),
  mounted () {
    api.service('people').find({}).then(
      result => {
        this.people = result.data
      }
    )
  }
}
</script>

<style>

</style>
