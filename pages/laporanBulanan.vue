<template>
  <div class="container-fluid bg-black atas mt-3">
    <div class="row pt-3">
      <div class="col-lg">
        <nuxt-link to="/">
          <button class="btn btn-danger text-decoration-none">Kembali</button>
        </nuxt-link>
      </div>
    </div>
    <div class="row text-center bebas">
      <div class="col-lg-12 text-white">
        <h3>Presensi Bulanan</h3>
      </div>
    </div>
    <div class="row justify-content-end pb-5">
      <div class="col-lg-2">
        <select class="form-control form-control-lg">
          <option value="">Bulan ke 1</option>
        </select>
      </div>
      <div class="col-lg-2">
        <select class="form-control form-control-lg">
          <option value="">Pilih Jurusan</option>
        </select>
      </div>
    </div>
    <div class="container">
      <table style="width:100%; text-align: center; color: white;">
        <tr class="b">
          <th rowspan="2"  >No</th>
          <th rowspan="2">Nama Murid</th>
          <th colspan="10" >Tanggal</th>
          <th colspan="3" >Absen</th>
          <th rowspan="2">Keterangan</th>
        </tr>
        <tr class="b">
          <th>1</th>
          <th>2</th>
          <th>3</th>
          <th>4</th>
          <th>5</th>
          <th>6</th>
          <th>7</th>
          <th>8</th>
          <th>9</th>
          <th>10</th>
          <th>S</th>
          <th>I</th>
          <th>A</th>
        </tr>
        <tr>
          <td>Eve</td>
          <td>Jackson</td>
          <td>Hadir</td>
          <td>Tidak</td>
          <td>Hadir</td>
          <td>Tidak</td>
          <td>Hadir</td>
          <td>Tidak</td>
          <td>Hadir</td>
          <td>Tidak</td>
          <td>Hadir</td>
          <td>Tidak</td>
          <td>1</td>
          <td>2</td>
          <td>0</td>
          <td>Malas</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<style scoped>
.btn{
  text-decoration: none;
}

.bebas{
  padding-top: 50px;
}
.atas {
  padding-bottom: 700px;
}

td{
  border-bottom: 2px solid #fff;
}

tr.b{
  background: gray;
}

</style>