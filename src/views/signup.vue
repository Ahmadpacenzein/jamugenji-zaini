<template>
  <div class="signup-container">
    <div class="neumorphism-card signup-card">
      <h2>Buat Akun Baru</h2>
      <p>Bergabunglah dengan kami dan rasakan manfaat jamu!</p>
      <form @submit.prevent="handleSignUp">
        <div class="form-group">
          <label for="name">Nama Lengkap</label>
          <input type="text" id="name" v-model="name" class="neumorphism-input" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" class="neumorphism-input" required>
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password" v-model="password" class="neumorphism-input" required>
        </div>
         <div class="form-group">
          <label for="confirm-password">Konfirmasi Password</label>
          <input type="password" id="confirm-password" v-model="confirmPassword" class="neumorphism-input" required>
        </div>
        <button type="submit" class="btn btn-primary">Daftar</button>
      </form>
      <p class="switch-form">Sudah punya akun? <a href="#">Login di sini</a></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SignUp',
  data() {
    return {
      name: '',
      email: '',
      password: '',
      confirmPassword: '',
    };
  },
  methods: {
    handleSignUp() {
      if (this.password !== this.confirmPassword) {
        alert('Password tidak cocok!');
        return;
      }
      // Logika sign up di sini
      console.log('Sign Up attempt:', this.email);
      alert('Fitur sign up belum diimplementasikan.');
    }
  }
}
</script>

<style scoped>
/* Gunakan style yang sama dengan Login.vue, hanya sesuaikan nama class container */
.signup-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 80vh; 
  padding: 40px 20px;
  background-color: #f0f2f5;
}

.neumorphism-card {
  background: #f0f2f5;
  border-radius: 30px;
  padding: 40px 50px;
  box-shadow: 15px 15px 30px #d1d3d6, -15px -15px 30px #ffffff;
  width: 100%;
  max-width: 480px; /* Sedikit lebih lebar untuk form tambahan */
  text-align: center;
}

h2 {
  color: #333;
  margin-bottom: 10px;
}

p {
  color: #666;
  margin-bottom: 30px;
}

.form-group {
  margin-bottom: 20px; /* Sedikit lebih rapat */
  text-align: left;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  color: #555;
  font-weight: 500;
}

.neumorphism-input {
  width: 100%;
  background: #f0f2f5;
  border: none;
  border-radius: 15px;
  padding: 15px 20px;
  box-shadow: inset 6px 6px 12px #d1d3d6, inset -6px -6px 12px #ffffff;
  font-size: 1em;
  color: #333;
  box-sizing: border-box; 
}
.neumorphism-input:focus {
    outline: none;
    box-shadow: inset 6px 6px 12px #d1d3d6, inset -6px -6px 12px #ffffff, 0 0 0 2px #e6b800;
}


.btn {
  border: none;
  padding: 15px 30px;
  border-radius: 20px;
  cursor: pointer;
  font-weight: bold;
  font-size: 1.1em;
  transition: all 0.3s ease;
  background-color: #f0f2f5;
  box-shadow: 8px 8px 16px #d1d3d6, -8px -8px 16px #ffffff;
  width: 100%;
  margin-top: 10px;
}

.btn:hover {
    box-shadow: inset 4px 4px 8px #d1d3d6, inset -4px -4px 8px #ffffff;
}

.btn-primary {
  background-color: #e6b800;
  color: white;
  box-shadow: 8px 8px 16px #c49c00, -8px -8px 16px #fff488;
}
.btn-primary:hover {
  background-color: #cda500;
  box-shadow: inset 4px 4px 8px #b18e00, inset -4px -4px 8px #fffcb0;
}

.switch-form {
  margin-top: 30px;
  font-size: 0.9em;
}

.switch-form a {
  color: #e6b800;
  text-decoration: none;
  font-weight: bold;
}
.switch-form a:hover {
  text-decoration: underline;
}
</style>