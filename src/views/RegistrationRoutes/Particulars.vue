<template>
    <v-container>
        <v-row>
            <v-col>
                <div class="header header-secondary font-weight-medium">
                    <h3 class="center text-h3 mb-4">Step-1</h3>
                </div> 
                <v-form v-model="valid">
                    <v-container>
                        <!-- Name section -->
                        <div class="name-section">
                            <v-row>
                            <v-col
                            cols="12"
                            md="5"
                            >
                            <v-text-field
                                v-model="firstname"
                                label="First name"
                                required
                            ></v-text-field>
                            </v-col>

                            <v-col
                            cols="12"
                            md="5"
                            offset-md="1"
                            >
                            <v-text-field
                                v-model="middlename"
                                :counter="10"
                                label="Middle name"
                                required
                            ></v-text-field>
                            </v-col>

                            <v-col
                            cols="12"
                            md="5"
                            >
                            <v-text-field
                                v-model="lastname"
                                label="Last Name"
                                required
                            ></v-text-field>
                            </v-col>
                            <v-col
                            cols="12"
                            md="5"
                            offset-md="1"
                            >
                            <v-text-field
                                v-model="lastname"
                                label="Last Name"
                                required
                            ></v-text-field>
                            </v-col>
                        </v-row>
                        </div>

                        <!-- Location section -->
                        <div class="name-section location-section mt-14">
                            <v-row>
                            <v-col
                            cols="12"
                            md="5"
                            >
                            <v-text-field
                                v-model="region"
                                label="Region"
                                required
                            ></v-text-field>
                            </v-col>

                            <v-col
                            cols="12"
                            md="5"
                            offset-md="1"
                            >
                            <v-text-field
                                v-model="town"
                                label="Town"
                                required
                            ></v-text-field>
                            </v-col>

                            <v-col
                            cols="12"
                            md="5"
                            >
                            <v-text-field
                                v-model="suburb"
                                label="Suburb"
                                required
                            ></v-text-field>
                            </v-col>
                        </v-row>
                        </div>

                        <!-- Skillset -->
                        <div class="mt-14">
                            <v-row>
                                <v-col cols="12" md="8">
                                    <v-text-field
                                        v-model="phone"
                                        label="Phone"
                                        required
                                    >
                                    <v-icon
                                    class="grey lighten-2 round"
                                    slot="append"
                                    color="green"
                                    >
                                    mdi-plus
                                    </v-icon>
                                    </v-text-field>
                                </v-col>
                            </v-row>
                        </div>
                    </v-container>
                </v-form>       
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    
}
</script>

<style> 
    .name-section {
        border: 1px solid rgb(136, 135, 135);
        border-radius: 3px;
        padding: 0 10px;
    }

    .round {
        border-radius: 50%;
    }
</style>