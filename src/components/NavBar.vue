<template>
    <nav>
        <v-app-bar flat app>
            <v-app-bar-nav-icon class="grey--text" @click="drawer=!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Viji</span>
                <span>Clientele</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="grey" dark>
                <span>Sign Out</span>
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-app-bar>
        <v-navigation-drawer app class="cyan accent-4" v-model="drawer">
            <v-list>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-item-action>
                        <v-icon>{{link.icon}}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>{{link.text}}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            drawer: false,
            links: [
                {icon: 'mdi-view-dashboard', text:'Dashboard', route:"/"},
                {icon: 'mdi-account-star', text:'My Clients', route:"/my-clients"},
                {icon: 'mdi-account-group', text:'All Clients', route:"/all-clients"},
            ]
        }
    },
}
</script>