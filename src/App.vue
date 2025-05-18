<script>
export default {
  data() {
    return {
      message: "Hello World!",
      isVisible: true,
      isChecking: true,
    };
  },
  methods: {
    handleClick(text) {
      this.isChecking = !this.isChecking;
      console.log(text);
    },
    toggle() {
      this.isVisible = !this.isVisible;
    },
    buttonHover() {
      this.message = "Welcome!";
    },
  },
};
</script>

<template>
  <div class="container">
    <h1 class="title">{{ message }}</h1>

    <button
      type="button"
      @click="handleClick('Click me button')"
      @mouseover="buttonHover"
      class="primary-button" > Click Me </button>

    <pre class="debug-text">isVisible: {{ isVisible }}</pre>

    <p v-if="isVisible" class="info-text">"Welcome to the pune"</p>
   
    <button @click="toggle" class="secondary-button">Toggle View</button>
  </div>
</template>

<style scoped>
.container {
  max-width: 600px;
  margin: 50px auto;
  padding: 20px;
  text-align: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.title {
  color: #2c3e50;
  margin-bottom: 20px;
}

.primary-button,
.secondary-button {
  margin: 10px;
  padding: 12px 24px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  border: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.primary-button {
  background-color: #3498db;
  color: white;
}

.primary-button:hover {
  background-color: #2980b9;
}

.secondary-button {
  background-color: #2ecc71;
  color: white;
}

.secondary-button:hover {
  background-color: #27ae60;
}

.info-text {
  margin-top: 20px;
  font-size: 30px;
  color:rgb(220, 14, 14);
}

.debug-text {        
  margin-top: 20px;
  font-size: 14px;
  color: #7f8c8d;
  background-color: #ecf0f1;
  padding: 10px;
  border-radius: 5px;
}
</style>


