<template>

</template>

<script>
    export default {
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
                ]
            }

        }
    }
</script>

<style>

</style>
