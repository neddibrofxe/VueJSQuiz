<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <router-link to="/siswa">Data Siswa</router-link>
    <router-link to="/kelas">Data Kelas</router-link>
    <router-view/> --> <!-- update data yg di klik -->
    <h1>{{ nama }}</h1>
    <h2>Nama: <input v-model="nama"><br></h2>
    <h2>Nilai Anda:&nbsp{{ nilai }}</h2>
    <button @click="totalnilai">Kirim </button>  
    <h2>1. Apa warna sepatu milik wahyu wahyudin kelas XX-RPL 3 ?</h2>
    <input type="radio" v-model="soal1" value="Hitam">Hitam &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Biru">Biru &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Merah">Merah &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Putih">Putih &nbsp&nbsp<br>
    <h2>2. Apa jenis Kelamin yang disukai oleh shiina ?</h2>
    <input type="radio" v-model="soal2" value="Laki-Laki">Laki-Laki &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Perempuan">Perempuan &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Ganda">Ganda &nbsp&nbsp
    <input type="radio" v-model="soal2" value="-">- &nbsp&nbsp<br>
    <h2>3. Hari apakah pasar minggu buka ?</h2>
    <input type="radio" v-model="soal3" value="Senin">Senin &nbsp&nbsp
    <input type="radio" v-model="soal3" value="Rabu">Rabu &nbsp&nbsp
    <input type="radio" v-model="soal3" value="Sabtu">Sabtu &nbsp&nbsp
    <input type="radio" v-model="soal3" value="Minggu">Minggu &nbsp&nbsp<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'*/

export default {
  name: 'app',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
      /*components: {
        HelloWorld
      }*/
    }
  },
methods: {
  totalnilai(){
    if (this.soal1 == 'Hitam' && this.soal2 == 'Laki-Laki' && this.soal3 == 'Minggu') {
      this.nilai=+3    
    }
    else if (this.soal1 == 'Hitam' && this.soal2 == 'Laki-Laki') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Hitam' && this.soal3 == 'Minggu') {
      this.nilai=+2 
    }
    else if (this.soal2 == 'Laki-Laki' && this.soal3 == 'Minggu') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Hitam') {
      this.nilai=+1 
    }
    else if (this.soal2 == 'Laki-Laki') {
      this.nilai=+1 
    }
    else if (this.soal3 == 'Minggu') {
      this.nilai=+1 
    }
    else {
      this.nilai = 0 
    }
  }
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
