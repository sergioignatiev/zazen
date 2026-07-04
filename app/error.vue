<template>
  <div class="error-container">
    <div class="error-content">
      <h1> {{ error?.statusCode }}</h1>
      <p v-if="error.message">
        Проблема  'Что-то пошло не так...'
      </p>
      <p v-else>
        F rfr
      </p>
      <button
        class="btn-home"
        @click="handleClearError"
      >
        Вернуться на главную
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
// Nuxt передает объект ошибки через пропсы
defineProps({
  error: {
    type: Object,
    required: true
  }
})

// Функция для очистки ошибки и редиректа
const handleClearError = () => {
  clearError({ redirect: '/' })
}
</script>

<style scoped>
.error-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
  font-family: sans-serif;
  background-color: #f4f4f9;
}

.error-content h1 {
  font-size: 5rem;
  margin: 0;
  color: #ff4757;
}

.btn-home {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #2f3542;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
}

.btn-home:hover {
  background-color: #57606f;
}
</style>
