<template>
  <div class="container-fluid atas mt-3">
    <div class="row pt-3">
      <div class="col-lg">
        <nuxt-link to="/halUtama">
          <button class="btn btn-light text-decoration-none">Kembali</button>
        </nuxt-link>
      </div>
    </div>
    <div class="row text-center bebas">
      <div class="col-lg-12 text-white">
        <h3>Presensi Bulanan</h3>
      </div>
    </div>
    <form @submit.prevent="getPresensi">
      <div class="row justify-content-end pb-5">
        <div class="col-lg-2">
          <p style="color: white;">Start Date</p>
          <input type="date" class="form-control form-control-lg">
        </div>
        <div class="col-lg-2 ">
          <p style="color: white;">End Date</p>
          <input type="date" class="form-control form-control-lg">
        </div>
      </div>
      <div class=" container">
        <table style="width:100%; text-align: center; color: white;">
          <tr class="b">
            <th rowspan="2">No</th>
            <th rowspan="2">Nama Murid</th>
            <th colspan="3">Absen</th>
            <th rowspan="2">Keterangan</th>
          </tr>
          <tr class="b">
            <th>S</th>
            <th>I</th>
            <th>A</th>
          </tr>
          <tr>
            <td>{{ visitors.id }}</td>
            <td>{{ visitors.idSiswa }}</td>
            <td>{{ visitors.keterangan }}</td>
            <td>{{ visitors.keterangan }}</td>
            <td>{{ visitors.keterangan }}</td>
            <td>{{ visitors.keterangan }}</td>
          </tr>
        </table>
      </div>
    </form>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const visitors = ref([])

const getPresensi = async () => {
  let {data,error} = await supabase
  .from('presensi')
  .select('*')
  if(data) visitors.value = data
}

onMounted(() => {
  getPresensi()
})
</script>

<style scoped>
.btn {
  text-decoration: none;
}

.bebas {
  padding-top: 50px;
}

.atas {
  min-height: 150vh;
  background: rgb(26, 26, 26);
}

td {
  border-bottom: 2px solid #fff;
}

tr.b {
  background: gray;
}
</style>