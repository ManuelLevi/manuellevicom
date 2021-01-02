<template>
    <nav>
        <v-navigation-drawer v-model="drawer" dark app mini-variant mini-variant-width="100" class='cyan darken-4'>

            <v-list>
                <v-list-item class="mb-12">
                    <v-list-item-action>
                    </v-list-item-action>
                </v-list-item>
            </v-list>
            <v-list flat>
                <v-list-item router to='/'>
                    <v-list-item-content>
                        <v-list-item-subtitle align="center">Home</v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
            </v-list>

            <v-list style="position: absolute; bottom:0" class="ml-3" flat>
                <v-list-item router to='/'>
                    <v-list-item-action>
                        <v-list-item-subtitle>Signout</v-list-item-subtitle>
                    </v-list-item-action>
                </v-list-item>

            </v-list>
        </v-navigation-drawer>

    </nav>

</template>