<template>
  <div class="container-fluid bg-black">
    <div class="row text-center pp">
      <div class="col">
        <h1 class="text-white">Presensi Kelas</h1>
      </div>
    </div>
    <div class="row justify-content-center ps">
      <div class="col-lg-6 d-flex justify-content-center">
        <div class="card rounded-5 text-center pt-4">
          <h3 class="text-white">Login</h3>
          <div class="card-body d-flex justify-content-center pt-5">
            <form>
              <input type="text" class="form-control form-control-lg rounded-3 akn text-center" placeholder="Email">
              <input type="text" class="form-control form-control-lg rounded-3 akn text-center" placeholder="Password">
              <nuxt-link to="/halUtama">
                <button class="btn btn-success">Login</button>
              </nuxt-link>
            </form>
          </div>
        </div>
      </div>
    </div>
    <div class="row kbl">
      <div class="col-lg-3">
        <nuxt-link to="/">
          <button class="btn btn-danger">Kembali</button>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<style scoped>
.kbl{
  padding: 40px;
}

.btn{
  width: 150px;
  height: 40px;
}
.akn{
  width: 300px;
  margin-bottom: 50px;
}
*{
  margin: 0px;
  padding: 0px;
}
.pp{
  padding-top: 100px;
  padding-bottom: 150px
}

.card{
  width: 400px;
  height: 400px;
  box-shadow: 15px 15px 0px 5px gray;
  border: 2px solid gray;
  background: rgb(26, 26, 26);
}

.ps{
  padding-bottom: 100px;
}
</style>

<script setup>
definePageMeta({
  layout:'login'
})
</script>