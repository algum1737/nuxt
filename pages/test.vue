<template>
  <v-card>
    <v-card-title>
      hihihihi
    </v-card-title>
    <v-card-text>
      <v-textarea v-model="text" />
    </v-card-text>
    <v-card-actions>
      <v-btn @click="test">
        test
      </v-btn>
      <v-btn @click="hello">
        hello
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data () {
    return {
      text: 'wwww'
    }
  },
  methods: {
    async test () {
      this.text = 'fwedsf'
      const r = await this.$axios.get('/api')
      this.text = r.data
    },
    async hello () {
      this.text = 'ghjkmyuksf'
      const r = await this.$axios.get('/api/hello')
      this.text = r.data
    }
  }
}
</script>
