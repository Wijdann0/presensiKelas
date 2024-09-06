<template>
  <div class="container">
    <div class="row d-flex justify-content-center pt-5">
      <div class="col-lg-8">
        <form @submit.prevent="kirimData">
          <div class="mb-4">
            <select v-model="form.tingkat" class="jurusan form-control form-control-lg rounded-4 fs-3 text-center">
              <option value="">Tingkat</option>
              <option value="10">10</option>
              <option value="11">11</option>
              <option value="12">12</option>
            </select>
          </div>
          <div class="mb-3">
            <div class="row mb-5">
              <div class="col-md-6">
                <select v-model="form.jurusan" class="jurusan form-control form-control-lg rounded-4 fs-3 text-center">
                  <option value="">JURUSAN</option>
                  <option value="pplg">PPLG</option>
                  <option value="TJKT">TJKT</option>
                  <option value="TSM">TSM</option>
                  <option value="DKV">DKV</option>
                  <option value="TOI">TOI</option>
                </select>
              </div>
              <div class="col-md-6">
                <select @change="cek" v-model="form.kelas"
                  class="jurusan form-control form-control-lg rounded-4 fs-3 text-center">
                  <option value="">KELAS</option>
                  <option value="1">1</option>
                  <option value="2">2</option>
                  <option value="3">3</option>
                  <option value="4">4</option>
                </select>
              </div>
            </div>
          </div>
          <div v-if="form.kelas == 1">
            <div class=" col d-flex justify-content-center">
              <select v-model="form.nama" class="form-control form-control nama fs-3 text-center mb-4">
                <option value="">Nama</option>
                <option v-for="(member, i) in members" :key="i" :value="member.nama">{{ member.nama }}</option>
              </select>
            </div>
            <div class="col d-flex justify-content-center">
              <select v-model="form.keterangan" class="form-control form-control nama fs-3 text-center mb-5">
                <option value="">Keterangan</option>
                <option v-for="(item, i) in objectives" :key="i" :value="item.nama">{{ item.nama }}</option>
              </select>
            </div>
            <div class="col d-flex justify-content-center">
              <button type="submit" class="btn btn-success krm">Kirim</button>
            </div>
          </div>
        </form>
      </div>
    </div>
    <nuxt-link to="/halUtama">
      <button type="button" class="btn btn-dark bck mt-5 mb-5">Kembali</button>
    </nuxt-link>
  </div>
</template>


<script setup>
const supabase = useSupabaseClient()

const kelas = ref([])
const members = ref([])
const objectives = ref([])

const form = ref({
  nama: "",
  tingkat: "",
  jurusan: "",
  kelas: "",
  keterangan: ""
})

async function cek() {
  let { data, error } = await supabase
    .from('siswa')
    .select('*')
    .eq('tingkat', form.value.tingkat)
    .eq('jurusan', form.value.jurusan)
    .eq('kelas', form.value.kelas)
  if (data) console.log(data)
}

const getSiswa = async () => {
  const { data, error } = await supabase
    .from('siswa')
    .select('*')
  if (data) members.value = data
}

const getKelas = async () => {
  const { data, error } = await supabase
    .from('siswa')
    .select('*, kelas')
  if (data) kelas.value = data
}
const getKeterangan = async () => {
  const { data, error } = await supabase
    .from('keterangan')
    .select('*')
  if (data) objectives.value = data
}

const kirimData = async () => {
  console.log(form.value)
  const { error } = await supabase
    .from('presensi')
    .insert([form.value])
  if (!error) navigateTo('/index')
}

const isi = async () => {
  const { data, error } = await supabase
    .from('siswa')
    .select('*')
    .eq('Tingkat', form.tingkat)
    .eq('kelas', form.kelas)
    .eq('jurusan', form.jurusan)
}

onMounted(() => {
  getSiswa()
  getKelas()
  getKeterangan()
})
</script>


<style scoped>
.hei {
  min-height: 90vh;
  background: rgb(26, 26, 26);
}

.jurusan {
  height: 100px;
  color: white;
  background: rgb(26, 26, 26) !important;
  box-shadow: 10px 10px 0px 2px lightblue;
  border: 2px solid lightblue;
}

.link {
  width: 500px;
  height: 50px;
  color: white;
  background-color: black;
  box-shadow: 10px 10px 0px 5px lightblue;
  border: 2px solid lightblue;
  transition: width 1.5s, height 1.5s;
  text-decoration-style: none;
}

.atas {
  padding-top: 100px;
}

.nama {
  color: white;
  background: rgb(26, 26, 26) !important;
  width: 500px;
  height: 70px;
  box-shadow: 10px 10px 0px 3px lightblue;
  border: 2px solid lightblue;
}

.krm {
  width: 100px;
  height: 50px;
  box-shadow: 5px 5px 0px 1.5px lightblue;
  border: 2px solid lightblue;
  background: rgb(26, 26, 26);
}
</style>