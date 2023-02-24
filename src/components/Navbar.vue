<template>

    <v-app-bar app dark class="">
        <v-btn>
            <v-icon icon="fa:fas fa-list" class="mr-2 "></v-icon>
        </v-btn>
        <v-toolbar-title class="pa-n1"> CATALOG</v-toolbar-title>
        <div style="position: absolute; margin-left:auto;margin-right: auto; left: 0; right: 0; text-align: center;">
            <h2>shop</h2>
        </div>
        <v-spacer></v-spacer>
        <v-col cols="3">
            <v-card class="mx-auto" max-width="400" flat>
                <v-card-text>
                    <v-text-field density="compact" variant="outlined" label="Search templates"
                        append-inner-icon="fa:fas fa-search" single-line hide-details></v-text-field>
                </v-card-text>
            </v-card>
        </v-col>
    </v-app-bar>

</template>
<script setup>

</script>


<style>

</style>   
