<template>
    <v-container>
        <v-row>
            <v-col>
                <div class="header header-secondary font-weight-medium">
                    <h3 class="center text-h3 mb-4">Step-1</h3>
                </div> 
                <v-form v-model="valid" @submit.prevent="onSubmit">
                    <v-container>
                        <!-- Name section -->
                        <h4 class="mt-4 header-required">Name</h4>
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
                        <h4 class="header-required  mt-14">Location</h4>
                        <div class="name-section location-section">
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
                                        v-model="skillset"
                                        label="Skill set"
                                        required
                                    >
                                    <!-- <v-tooltip top>
                                        <template v-slot:activator="{ on, attrs }"> -->
                                            <v-icon
                                                class="grey lighten-2 round add-phone"
                                                slot="append"
                                                color="green"
                                                v-on="on"
                                                v-bind="attrs"
                                                title="add contact"
                                            >
                                            mdi-plus
                                            </v-icon>
                                        <!-- </template>
                                         <span>Add Contact</span>
                                    </v-tooltip> -->
                                    </v-text-field>
                                </v-col>
                            </v-row>
                        </div>

                        <!-- Contact -->
                        <div class="mt-14">
                            <v-row>
                                <v-col cols="12" md="8">
                                    <v-text-field
                                        v-model="phone"
                                        label="Phone"
                                        required
                                    >
                                    <!-- <v-tooltip top>
                                        <template v-slot:activator="{ on, attrs }"> -->
                                            <v-icon
                                                class="grey lighten-2 round add-phone"
                                                slot="append"
                                                color="green"
                                                v-on="on"
                                                v-bind="attrs"
                                                title="add contact"
                                            >
                                            mdi-plus
                                            </v-icon>
                                        <!-- </template>
                                         <span>Add Contact</span>
                                    </v-tooltip> -->
                                    </v-text-field>
                                </v-col>
                            </v-row>
                        </div>

                        <!-- Contact -->
                        <div class="mt-14">
                            <v-row>
                                <v-col cols="12" md="8">
                                    <v-text-field
                                        v-model="email"
                                        label="Email"
                                        required
                                    >
                                    <!-- <v-tooltip top>
                                        <template v-slot:activator="{ on, attrs }"> -->
                                            <v-icon
                                                class="grey lighten-2 round add-phone"
                                                slot="append"
                                                color="green"
                                                v-on="on"
                                                v-bind="attrs"
                                                title="add contact"
                                            >
                                            mdi-plus
                                            </v-icon>
                                        <!-- </template>
                                         <span>Add Contact</span>
                                    </v-tooltip> -->
                                    </v-text-field>
                                </v-col>
                            </v-row>
                        </div>

                        <!-- Password section -->
                        <h4 class="mt-4 header-required">Password</h4>
                        <div class="name-section">
                            <v-row>
                            <v-col
                            cols="12"
                            md="8"
                            >
                            <v-text-field
                                v-model="password"
                                label="Password"
                                required
                            ></v-text-field>
                            </v-col>

                            <v-col
                            cols="12"
                            md="8"
                            >
                            <v-text-field
                                v-model="confirmPassword"
                                :counter="10"
                                label="Confirm Password"
                                required
                            ></v-text-field>
                            </v-col>
                        </v-row>
                        </div>
                        <v-btn large color="green" dark type="submit" class="mt-6">Submit <v-icon>mdi-submit</v-icon></v-btn>
                    </v-container>
                </v-form>       
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: "Particulars",
    data(){
        return {

        }
    },
    methods: {
        onSubmit(){
            this.$router.push("/register/profile-photo");
        }
    }
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

    .add-phone:hover {
        cursor: pointer;
    }

    .header-required:after {
        content: "*";
        color: red;
    }
</style>