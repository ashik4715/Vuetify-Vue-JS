<template>
  <div class="dashboard">

    <div class="container">
      <h1 class="heading white--text">Dashboard</h1>

      <v-container fluid class="my-5">
        <v-btn class="hidden-md-and-down">click me</v-btn>

        <v-layout row wrap>
          <v-flex xs12 md6>

            <v-btn outline block class="info">1</v-btn>

          </v-flex>

          <v-flex xs4 md2>
            <v-btn outline block class="error">2</v-btn>
          </v-flex>
          <v-flex xs4 md2>
            <v-btn outline block class="error">3</v-btn>
          </v-flex>
          <v-flex xs4 md2>
            <v-btn outline block class="error">2</v-btn>
          </v-flex>

        </v-layout>

        <v-layout row wrap justify-space-around>
          <v-flex xs4 md3>
            <v-btn outline block class="error">4</v-btn>
          </v-flex>
          <v-flex xs4 md3>
            <v-btn outline block class="error">5</v-btn>
          </v-flex>
        </v-layout>

      </v-container>

    </div>

  </div>
</template>

<script>
  export default {

  }
</script>
