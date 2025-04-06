<script setup>

import { ref } from 'vue'

const theme = ref('light')
const visible = ref(false)

function onClick() {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}

</script>