<template>
    <div class="abd container-fluid">
        <form>
          <div class="row d-flex justify-content-around mt-3">
            <div class="col-lg-5">
              <div class="mt-5">
                <select class="jurusan form-control form-control-lg rounded-3 fs-3 text-center">
                  <option class="" value="">Pilih Jurusan</option>
                  <option value="PPLG">PPLG</option>
                </select>
              </div>
            </div>
            <div class="col-lg-5">
              <div class="mt-5">
                <select class="jurusan form-control form-control-lg rounded-3 fs-3 text-center">
                  <option class="" value="">Pilih Kelas</option>
                  <option value="PPLG">XII PPLG 1</option>
                  <option value="PPLG">XII PPLG 2</option>
                  <option value="PPLG">XII PPLG 3</option>
                  <option value="PPLG">XII PPLG 4</option>
                </select>
              </div>
            </div>
          </div>
          <div class="row bawah d-flex justify-content-center">
            <div class="col-lg-4">
              <nuxt-link to="/presensi">
                <button class="link form-control form-control-lg d-flex justify-content-center fs-4 text-decoration-none">Klik Link Presensi</button>
              </nuxt-link>
            </div>
          </div>
        </form>
          <div class="row bck">
            <div class="col-lg-1">
              <nuxt-link to="/">
                <button type="button" class="btn btn-light">Kembali</button>
              </nuxt-link>
            </div>
          </div>
    </div>
</template>

<style scoped>
.jurusan{
  height: 100px;
  color: white;
  background-color:black;
  box-shadow: 0px 0px 20px 10px lightblue;
}

.abd {
  background: black;
  padding-bottom: 30px;
}
.bawah{
  padding-top: 250px;
}

.bck{
  padding-top: 200px;
}

.link {
  color: white;
  background-color:black;
  box-shadow: 0px 0px 20px 10px lightblue;
}
</style>