<template>

<v-card
              class="mx-auto pa-6 mt-0"
              elevation="8"
              rounded="lg" 
              style="max-width: 90%; width: 700px; height: 610px"
            >
              <div class="text-subtitle-1 text-medium-emphasis"><b>Register</b></div>
  
              <v-text-field
                density="compact"
                placeholder="Firstname"
                variant="outlined"
              ></v-text-field>

              <v-text-field
                density="compact"
                placeholder="Laststname"
                variant="outlined"
              ></v-text-field>

              <v-text-field
                density="compact"
                placeholder="Email"
                variant="outlined"
              ></v-text-field>

              <v-text-field
                density="compact"
                placeholder="Role"
                variant="outlined"
              ></v-text-field>
              <div
                class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between"
              >
                Password
              </div>
             
  
              <v-text-field
                :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
                :type="visible ? 'text' : 'password'"
                density="compact"
                placeholder="Enter your password"
                prepend-inner-icon="mdi-lock-outline"
                variant="outlined"
                @click:append-inner="visible = !visible"
              ></v-text-field>

              <div
                class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between"
              >
                Confirm Password
              </div>
             
  
              <v-text-field
                :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
                :type="visible ? 'text' : 'password'"
                density="compact"
                placeholder="Enter your password"
                prepend-inner-icon="mdi-lock-outline"
                variant="outlined"
                @click:append-inner="visible = !visible"
              ></v-text-field>

              <v-btn class="mb-8" color="blue" size="large" variant="tonal" block> Register </v-btn>

              <v-divider class="my-5"></v-divider>
              <h5 class="text-center"> Already have an account? <router-link to="/login">Click here to login</router-link></h5>

            </v-card>




</template>