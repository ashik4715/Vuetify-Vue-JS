<template>
  <div class="dashboard">
    <h1 class="subheading white--text">Dashboard</h1>

      <v-container fluid class="my-5">

        <v-layout row class="mb-3">
            <v-btn small flat color="yellow lighten-4" @click="sortBy('title')">
                <v-icon left large>folder</v-icon>
                <span class="caption text-lowercase">By Project Name</span>
            </v-btn>
            <v-btn small flat color="pink darken-4" @click="sortBy('person')">
                <v-icon left large>person</v-icon>
                <span class="caption text-lowercase">By Person</span>
            </v-btn>
        </v-layout>

        <v-card flat v-for="project in projects" :key="project.title">
          <v-layout row wrap :class="`pa-3 project ${project.status}`">
            <v-flex xs12 md6>
              <div class="caption grey--text">Project title</div>
              <div>{{ project.title }}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
              <div class="caption grey--text">Person</div>
              <div>{{ project.person }}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
              <div class="caption grey--text">Due by</div>
              <div>{{ project.due }}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
              <div class="right">
                <v-chip small :class="`${project.status} white--text caption my-2`">{{ project.status }}</v-chip>
              </div>
            </v-flex>
          </v-layout>
          <v-divider></v-divider>
        </v-card>

      </v-container>

  </div>
</template>

<script>
  export default {
    data(){
        return{
           projects: [
               { title: 'Design A New Website', person:'Therap BD', due:'1st March 2019', status:'ongoing',content:'Lorem ipsum dolor, Basta !'},
               { title: 'Maintain Existing Projects', person:'MazeGeek, Inc.', due:'2nd March 2019', status:'complete',content:'Dorem ipsum dolor, Basta !'},
               { title: 'Code up the Homepage', person:'Tiger IT', due:'3rd March 2019', status:'overdue',content:'Corem ipsum dolor, Basta !'},
               { title: 'Give Support Application', person:'Enosis', due:'4th March 2019', status:'ongoing',content:'Sorem ipsum dolor, Basta !'},
           ]
        }
    },
      methods: {
        sortBy(prop){
            this.projects.sort((a,b) => a[prop] < b[prop] ? -1 : 1)
        }
      }
  }
</script>

<style>
  .project.complete{
    border-left: 5px solid #3cd1c2;
  }
  .project.ongoing{
    border-left: 5px solid orange;
  }
  .project.overdue{
    border-left: 5px solid tomato;
  }
  .v-chip.complete{
    background: darkturquoise;
  }
  .v-chip.ongoing{
    background: #ffaa2c;
  }
  .v-chip.overdue{
    background: #f83e70;
  }
</style>