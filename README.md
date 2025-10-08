<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kuiz Interaktif: Tindakan Antibodi</title>
<style>
  body { font-family: Arial, sans-serif; background-color: #f0f8ff; padding: 20px; }
  h1 { color: #2e8b57; text-align: center; }
  .soalan { margin-bottom: 20px; padding: 15px; background-color: #e6f7ff; border-radius: 10px; }
  .jawapan { margin-top: 10px; font-weight: bold; }
  .betul { color: green; }
  .salah { color: red; }
  button { background-color: #2e8b57; color: white; padding: 10px 20px; border: none; border-radius: 5px; cursor: pointer; }
  button:hover { background-color: #3cb371; }
  img { max-width: 100%; border-radius: 8px; margin-top: 10px; }
</style>
</head>
<body>
<h1>Kuiz Interaktif: Tindakan Antibodi</h1>

<div id="kuiz"></div>

<button onclick="semakJawapan()">Semak Jawapan</button>
<p id="skor" style="font-size: 18px; font-weight: bold; margin-top: 20px;"></p>

<script>
const soalanData = [
  {
    soalan: "1. Apakah fungsi utama antibodi dalam sistem imun?",
    pilihan: ["Membunuh sel badan", "Menyerang bakteria secara fizikal", "Mengenal dan meneutralkan antigen", "Menghasilkan sel darah merah"],
    jawapan: 2,
    gambar: "https://i.ibb.co/2N3X0pX/antibody-binding.png"
  },
  {
    soalan: "2. Apakah yang dimaksudkan dengan antigen?",
    pilihan: ["Sejenis antibodi", "Bahan yang merangsang tindak balas imun", "Sel darah putih", "Virus sahaja"],
    jawapan: 1,
    gambar: "https://i.ibb.co/YdLYRZ9/antigen.png"
  },
  {
    soalan: "3. Jenis antibodi yang terdapat dalam susu ibu adalah?",
    pilihan: ["IgG", "IgA", "IgM", "IgE"],
    jawapan: 1,
    gambar: ""
  },
  {
    soalan: "4. Antibodi mengikat antigen melalui bahagian?",
    pilihan: ["Bahagian Fc", "Bahagian Fab", "Inti sel", "Membran plasma"],
    jawapan: 1,
    gambar: "https://i.ibb.co/4S9B7Pb/antibody-structure.png"
  },
  {
    soalan: "5. Apakah yang berlaku apabila antibodi mengikat antigen?",
    pilihan: ["Netralisasi atau penandaan untuk fagositosis", "Membiak virus", "Menghasilkan hormon", "Menghancurkan DNA"],
    jawapan: 0,
    gambar: ""
  },
  {
    soalan: "6. Antibodi jenis IgE biasanya terlibat dalam?",
    pilihan: ["Reaksi alahan", "Melawan bakteria", "Menetral virus", "Pembentukan antibodi lain"],
    jawapan: 0,
    gambar: ""
  },
  {
    soalan: "7. Dalam vaksin, antibodi membantu tubuh dengan?",
    pilihan: ["Memusnahkan sel sihat", "Mengenal antigen dan memori imuniti terbina", "Membentuk sel darah merah", "Meningkatkan hormon"],
    jawapan: 1,
    gambar: "https://i.ibb.co/9rF2P0y/vaccine-antibody.png"
  },
  {
    soalan: "8. Apa perbezaan utama antara antibodi dan antibodi monoklonal?",
    pilihan: ["Monoklonal spesifik terhadap satu antigen", "Monoklonal lebih murah dihasilkan", "Tiada perbezaan", "Monoklonal menyerang sel badan sendiri"],
    jawapan: 0,
    gambar: ""
  },
  {
    soalan: "9. Sel B dalam tindak balas imun berfungsi untuk?",
    pilihan: ["Menghasilkan antibodi", "Memusnahkan sel darah merah", "Mengangkut oksigen", "Menghasilkan hormon"],
    jawapan: 0,
    gambar: "https://i.ibb.co/k9t1xjJ/B-cell.png"
  },
  {
    soalan: "10. Apa yang dimaksudkan dengan 'netralisasi' oleh antibodi?",
    pilihan: ["Menghancurkan sel badan", "Mengikat antigen supaya tidak membahayakan badan", "Meningkatkan sel darah putih", "Menghasilkan antibodi baru"],
    jawapan: 1,
    gambar: ""
  }
];

function binaKuiz() {
  const kuizDiv = document.getElementById('kuiz');
  soalanData.forEach((item, index) => {
    let html = `<div class="soalan"><p>${item.soalan}</p>`;
    if (item.gambar) {
      html += `<img src="${item.gambar}" alt="Ilustrasi Soalan ${index+1}">`;
    }
    item.pilihan.forEach((pilihan, i) => {
      html += `<input type="radio" name="soalan${index}" value="${i}"> ${pilihan}<br>`;
    });
    html += `<div class="jawapan" id="jawapan${index}"></div></div>`;
    kuizDiv.innerHTML += html;
  });
}

function semakJawapan() {
  let skor = 0;
  soalanData.forEach((item, index) => {
    const jawapan = document.querySelector(`input[name="soalan${index}"]:checked`);
    const jawapanDiv = document.getElementById(`jawapan${index}`);
    if (jawapan) {
      if (parseInt(jawapan.value) === item.jawapan) {
        jawapanDiv.innerHTML = "<span class='betul'>Betul!</span>";
        skor++;
      } else {
        jawapanDiv.innerHTML = `<span class='salah'>Salah! Jawapan betul: ${item.pilihan[item.jawapan]}</span>`;
      }
    } else {
      jawapanDiv.innerHTML = `<span class='salah'>Belum pilih jawapan! Jawapan betul: ${item.pilihan[item.jawapan]}</span>`;
    }
  });
  document.getElementById('skor').innerText = `Anda mendapat ${skor} daripada ${soalanData.length} soalan.`;
}

binaKuiz();
</script>
</body>
</html>
