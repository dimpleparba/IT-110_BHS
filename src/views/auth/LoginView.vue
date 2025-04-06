<script setup>
import { ref } from 'vue'

const theme = ref('light')
const visible = ref(false)

function onClick() {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}
</script>

<template>
  <v-responsive class="border rounded text-align: left">
    <v-app :theme="theme">
      <v-app-bar class="px-3 py-3" color="red-darken-2" style="height: 95px">
        <v-img class="mx-auto" max-width="100" src="/Images/BHSlogo.png"></v-img>
        <v-spacer />
        <v-img src="/Images/Blogo.png" max-width="100" alt="Logo" />
      </v-app-bar>
      <v-main>
        <v-container>
          <v-card
            class="mx-auto pa-6 mt-0"
            elevation="8"
            rounded="lg"
            style="max-width: 90%; width: 500px; height: 610px"
          >
            <div class="text-subtitle-1 text-medium-emphasis">Account</div>

            <v-text-field
              density="compact"
              placeholder="Email address"
              prepend-inner-icon="mdi-email-outline"
              variant="outlined"
            ></v-text-field>

            <div
              class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between"
            >
              Password

              <a
                class="text-caption text-decoration-none text-blue"
                href="#"
                rel="noopener noreferrer"
                target="_blank"
              >
                Forgot login password?</a
              >
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

            <v-menu>
              <template #activator="{ props }">
                <v-btn v-bind="props" color="primary">Menu</v-btn>
              </template>

              <v-list>
                <v-list-item title="Municipal Admin" @click="select('Municipal Admin')" />
                <v-list-item title="Barangay Admin" @click="select('Barangay Admin')" />
              </v-list>
            </v-menu>

            <v-card class="mb-12 mt-10" color="surface-variant" variant="tonal">
              <v-card-text class="text-medium-emphasis text-caption">
                Warning: After 3 consecutive failed login attempts, you account will be temporarily
                locked for three hours. If you must login now, you can also click "Forgot login
                password?" below to reset the login password.
              </v-card-text>
            </v-card>

            <v-btn class="mb-8" color="blue" size="large" variant="tonal" block> Log In </v-btn>

            <v-card-text class="text-center">
              <a
                class="text-blue text-decoration-none"
                
                rel="noopener noreferrer"
                target="_blank"
              >
               <router-link to="/register"> Sign up here</router-link> <v-icon icon="mdi-chevron-right"></v-icon>
              </a>
            </v-card-text>
          </v-card>
        </v-container>
      </v-main>

      <v-footer color="red-darken-2" border app>
        2025 - Barangay Health Care</v-footer
      >
    </v-app>
  </v-responsive>
</template>
<style scoped>
.v-main {
  background-color: #ff8a80;
}

.center {
  text-align: center;
}
</style>
