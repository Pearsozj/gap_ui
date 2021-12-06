<template>
  <v-container>
  <v-list-item two-line>
      <v-list-item-content
        v-for="person in people"
        :key="person.id">
        <v-img
      height="100%"
      src="http://www.newdesignfile.com/postpic/2014/11/people-icon_58743.png"></v-img>
        <v-list-item-title>{{ person.first_name }} {{ person.last_name }}</v-list-item-title>
        <v-list-item-subtitle> {{person.email}}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-btn
        href="http://172.28.109.44:8080/"
        target="_blank"
        color="primary"
        text
      >
      <v-icon>mdi-arrow-left</v-icon>
        <span class="mr-2">Back to Home</span>
      </v-btn>
  </v-container>
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
