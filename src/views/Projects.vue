<template>
    <div class="projects">
        <h2 class="heading white--text">Projects</h2>

        <v-container class="my-5">
            <v-expansion-panel>
                <v-expansion-panel-content v-for="project in projects" :key="project.title">
                    <div slot="header">{{project.title}}</div>
                    <v-card>
                        <v-card-text class="px-4 light-blue--text">
                            <div class="font-weight-bold">Due : {{project.due}}</div>
                            <div>{{project.content}}</div>
                        </v-card-text>
                    </v-card>
                </v-expansion-panel-content>
            </v-expansion-panel>
        </v-container>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                projects: [
                    {
                        title: 'Design A New Website',
                        person: 'Therap BD',
                        due: '1st March 2019',
                        status: 'ongoing',
                        content: 'Lorem ipsum dolor, Basta !'
                    },
                    {
                        title: 'Maintain Existing Projects',
                        person: 'MazeGeek, Inc.',
                        due: '2nd March 2019',
                        status: 'complete',
                        content: 'Dorem ipsum dolor, Basta !'
                    },
                    {
                        title: 'Code up the Homepage',
                        person: 'Tiger IT',
                        due: '3rd March 2019',
                        status: 'overdue',
                        content: 'Corem ipsum dolor, Basta !'
                    },
                    {
                        title: 'Give Support Application',
                        person: 'Enosis',
                        due: '4th March 2019',
                        status: 'ongoing',
                        content: 'Sorem ipsum dolor, Basta !'
                    },
                ]
            }
        },
        computed:{
            myProjects(){
                return this.projects.filter(project =>{
                    return project.person === 'The Net Ninja'
                })
            }
        }
    }
</script>