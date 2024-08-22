<template>
  <div class="container-fluid bg-black">
    <div class="row my-5 d-flex justify-content-around mt-3 atas">
      <div class="col-lg-4 mb-5">
        <nuxt-link to="/isiPresensi" class="text-decoration-none">
          <div class="card bg-isiPresensi rounded-5 text-light">
            <div class="card-body d-flex justify-content-center align-items-center">
              <h2 class="">Isi Presensi</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
      <div class="col-lg-4 mb-5">
        <nuxt-link to="/laporanMingguan" class="text-decoration-none">
          <div class="card bg-laporanMingguan rounded-5">
            <div class="card-body d-flex justify-content-center align-items-center">
              <h2 class="solid">Laporan Mingguan</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
    <div class="row justify-content-md-center bawah">
      <div class="col-lg-4">
        <nuxt-link to="/laporanBulanan" class="text-decoration-none">
          <div class="card bg-laporanBulanan rounded-5">
            <div class="card-body d-flex justify-content-center align-items-center">
              <h2 class="p-10">Laporan Bulanan</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
<style scoped>

.bg-black{
  background: rgb(26, 26, 26) !important;
}
.card {
  color: white;
  height: 220px;
  background-color:rgb(26, 26, 26);
  box-shadow: 10px 15px 0px 10px lightblue;
  transition: width 3s, height 2s;
  border: 2px solid lightblue;
}

.card:hover{
  width: 525px;
  height: 300px;
}


h2{
  font-size: 40px;
}

.bawah{
  padding-bottom: 110px;
}

.atas{
  padding-top: 70px;
}
</style>