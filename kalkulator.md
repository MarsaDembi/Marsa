<!DOCTYPE html>
<html>
  <head>
    <title>Kalkulator Sederhana</title>
    <script>
      function hitung() {
        var angka1 = parseFloat(document.getElementById("angka1").value);
        var angka2 = parseFloat(document.getElementById("angka2").value);
        var operator = document.getElementById("operator").value;
        var hasil;

        if (operator == "tambah") {
          hasil = angka1 + angka2;
        } else if (operator == "kurang") {
          hasil = angka1 - angka2;
        } else if (operator == "kali") {
          hasil = angka1 * angka2;
        } else if (operator == "bagi") {
          hasil = angka1 / angka2;
        } else if (operator == "modulus") {
          hasil = angka1 % angka2;
        }

        document.getElementById("hasil").value = hasil;
      }
    </script>
  </head>
  <body>
    <h1>Kalkulator Sederhana</h1>
    <form>
      <label for="angka1">Angka 1:</label>
      <input type="number" id="angka1"><br>

      <label for="operator">Operator:</label>
      <select id="operator">
        <option value="tambah">+</option>
        <option value="kurang">-</option>
        <option value="kali">*</option>
        <option value="bagi">/</option>
        <option value="modulus">%</option>
      </select><br>

      <label for="angka2">Angka 2:</label>
      <input type="number" id="angka2"><br>

      <button type="button" onclick="hitung()">Hitung</button><br>

      <label for="hasil">Hasil:</label>
      <input type="text" id="hasil" readonly>
    </form>
  </body>
</html>
