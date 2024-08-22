<template>
  <div class="container-fluid mt-3 atas bg-black">
    <div class="row pt-3">
      <div class="col-lg">
        <nuxt-link to="/">
          <button class="btn btn-danger text-decoration-none">Kembali</button>
        </nuxt-link>
      </div>
    </div>
    <div class="row text-center pb-5 ss">
      <div class="col-lg-12 text-white">
        <h3>Presensi Mingguan</h3>
      </div>
    </div>
    <div class="container">
      <table style="width:100%; text-align: center; color: white;">
  <tr class="pp">
    <th rowspan="2">Name</th>
    <th rowspan="2">Age</th>
    <th colspan="2">Senin</th>
    <th colspan="2">Selasa</th>
    <th colspan="2">Rabu</th>
    <th colspan="2">Kamis</th>
    <th colspan="2">Jumat</th>
  </tr>
  <tr class="ps">
    <th>1</th>
    <th>2</th>
    <th>1</th>
    <th>2</th>
    <th>1</th>
    <th>2</th>
    <th>1</th>
    <th>2</th>
    <th>1</th>
    <th>2</th>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>57</td>
    <td>Sm</td>
    <td>43</td>
    <td>Sm</td>
    <td>43</td>
    <td>Sm</td>
    <td>43</td>
    <td>Sm</td>
    <td>43</td>
    <td>43</td>
  </tr>
</table>
    </div>
  </div>
</template>

<style scoped>
.atas {
  padding-bottom: 700px;
}

.ss{
  padding-top: 50px;
}

.pp{
  background: gray;
}

.ps{
  background: gray;
}

td{
  border-bottom: 2px solid #fff;
}
</style>