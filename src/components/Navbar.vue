<template>
    <nav>
        <v-snackbar v-model="snackbar" :timeout="4000" top color="success">
            <span>Awesome! You added a new Project !!</span>
            <v-btn flat color="teal" @click="snackbar = false">Close</v-btn>
        </v-snackbar>

        <v-toolbar flat app>
            <v-toolbar-side-icon class="lime--text" @click="drawer = !drawer">
            </v-toolbar-side-icon>

            <v-toolbar-title class="text-uppercase purple--text">
                <span class="font-weight-light">VuetiFy </span>
                <span>Jholok</span>
            </v-toolbar-title>

            <v-spacer></v-spacer>

            <v-menu offset-y>
                <v-btn flat slot="activator" color="amber">
                    <v-icon left>expand_more</v-icon>
                    <span>Menu</span>
                </v-btn>
                <v-list>
                    <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
                        <v-list-tile-title>{{ link.text }}</v-list-tile-title>
                    </v-list-tile>
                </v-list>
            </v-menu>

            <v-btn flat color="purple">
                <span>Sign Out</span>
                <v-icon right>exit_to_app</v-icon>
            </v-btn>

        </v-toolbar>

        <v-navigation-drawer app v-model="drawer" class="primary">
            <v-layout column align-center>
                <v-flex class="mt-5">
                    <v-avatar size="100">
                        <img src="/avatar-5.jpg" alt="">
                    </v-avatar>
                    <p class="white--text subheading mt-1">Taylor Otwell</p>
                </v-flex>
                <v-flex class="mt-4 mb-3">
                    <Popup/>
                </v-flex>
            </v-layout>
            <v-list>
                <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-tile-action>
                        <v-icon class="white--text">{{ link.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title class="white--text" style="font-size: 19px">
                            {{ link.text }}
                        </v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>

    </nav>

</template>

<script>
    import Popup from './Popup'

    export default {
        components: {Popup},
        data() {
            return {
                drawer: false,
                links: [
                    {icon: 'home', text: 'Home', route: '/'},
                    {icon: 'dashboard', text: 'Dashboard', route: '/dashboard'},
                    {icon: 'folder', text: 'My Projects', route: '/projects'},
                    {icon: 'person', text: 'Team', route: '/team'},
                    {icon: 'folder', text: 'About', route: '/about'},
                    {icon: 'folder', text: 'visibility', route: '/visibility'},
                ],
                snackbar :true
            }

        }
    }
</script>

<style>

</style>
