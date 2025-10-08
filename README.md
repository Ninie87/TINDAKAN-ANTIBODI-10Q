<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tindakan Antibodi - Biologi Tingkatan 4</title>
    <style>
        body {font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f0f8ff;}
        header {background-color: #4CAF50; color: white; padding: 20px; text-align: center;}
        nav {background-color: #333; overflow: hidden;}
        nav a {float: left; color: white; text-align: center; padding: 14px 16px; text-decoration: none;}
        nav a:hover {background-color: #ddd; color: black;}
        section {padding: 20px;}
        .interactive-diagram {display: flex; justify-content: center; margin: 20px 0;}
        .antibody {width: 100px; cursor: pointer; transition: transform 0.3s;}
        .antibody:hover {transform: scale(1.2);}
        .quiz {background: #e0f7fa; padding: 20px; border-radius: 10px; max-width: 800px; margin: auto;}
        .quiz button {margin-top: 10px; padding: 10px 20px;}
        footer {background-color: #4CAF50; color: white; text-align: center; padding: 10px; position: fixed; bottom: 0; width: 100%;}
    </style>
</head>
<body>

<header>
    <h1>Tindakan Antibodi</h1>
    <p>Subjek: Biologi Tingkatan 4</p>
</header>

<nav>
    <a href="#pengenalan">Pengenalan</a>
    <a href="#jenis">Jenis Antibodi</a>
    <a href="#tindakan">Proses Tindakan</a>
    <a href="#kuiz">Kuiz Interaktif</a>
</nav>

<section id="pengenalan">
    <h2>Pengenalan</h2>
    <p>Antibodi ialah protein yang dihasilkan oleh sistem imun untuk mengenal pasti dan meneutralkan patogen seperti bakteria dan virus.</p>
</section>

<section id="jenis">
    <h2>Jenis Antibodi</h2>
    <ul>
        <li>IgG - Antibodi utama dalam darah</li>
        <li>IgM - Antibodi pertama dalam tindak balas</li>
        <li>IgA - Antibodi pada mukosa</li>
        <li>IgE - Antibodi berkaitan alergi</li>
        <li>IgD - Antibodi pada permukaan sel B</li>
    </ul>
</section>

<section id="tindakan">
    <h2>Proses Tindakan Antibodi</h2>
    <div class="interactive-diagram">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Antibody_mechanism.png" alt="Antibody Action" class="antibody" onclick="showStep()">
    </div>
    <p id="step-description" style="text-align:center; font-weight:bold;">Klik pada antibodi untuk lihat langkah-langkah tindak balas.</p>
</section>

<section id="kuiz">
    <h2>Kuiz Interaktif - Pilihan Jawapan (10 Soalan)</h2>
    <div class="quiz">
        <ol>
            <li>Apakah fungsi pengaglutinan?<br>
                <input type="radio" name="q1" value="a"> Menandakan patogen untuk fagosit<br>
                <input type="radio" name="q1" value="b"> Menggumpalkan patogen<br>
                <input type="radio" name="q1" value="c"> Memecahkan antigen<br>
            </li>
            <li>Apakah tindakan pengopsoninan?<br>
                <input type="radio" name="q2" value="a"> Menghalang toksin memasuki sel<br>
                <input type="radio" name="q2" value="b"> Menggumpalkan antigen<br>
                <input type="radio" name="q2" value="c"> Menandakan patogen untuk dimakan oleh fagosit<br>
            </li>
            <li>Apakah maksud peneutralan?<br>
                <input type="radio" name="q3" value="a"> Menghalang toksin atau virus daripada memasuki sel<br>
                <input type="radio" name="q3" value="b"> Menggumpalkan patogen<br>
                <input type="radio" name="q3" value="c"> Menguraikan antigen<br>
            </li>
            <li>Apakah yang berlaku semasa penguraian?<br>
                <input type="radio" name="q4" value="a"> Memecahkan antigen<br>
                <input type="radio" name="q4" value="b"> Menandakan patogen<br>
                <input type="radio" name="q4" value="c"> Menghalang virus<br>
            </li>
            <li>Apakah pemendakan antigen?<br>
                <input type="radio" name="q5" value="a"> Menggumpalkan antigen terlarut menjadi pepejal<br>
                <input type="radio" name="q5" value="b"> Memecahkan antigen<br>
                <input type="radio" name="q5" value="c"> Menandakan patogen untuk fagosit<br>
            </li>
            <li>Pengaglutinan membantu sistem imun dengan cara:<br>
                <input type="radio" name="q6" value="a"> Memudahkan fagosit menelan patogen<br>
                <input type="radio" name="q6" value="b"> Menghalang antigen<br>
                <input type="radio" name="q6" value="c"> Mengeluarkan antibodi<br>
            </li>
            <li>Contoh pengopsoninan ialah:<br>
                <input type="radio" name="q7" value="a"> Fagosit menelan patogen<br>
                <input type="radio" name="q7" value="b"> Menggumpalkan antigen<br>
                <input type="radio" name="q7" value="c"> Menandakan virus<br>
            </li>
            <li>Peneutralan mencegah jangkitan dengan:<br>
                <input type="radio" name="q8" value="a"> Menghalang patogen memasuki sel<br>
                <input type="radio" name="q8" value="b"> Memecahkan antigen<br>
                <input type="radio" name="q8" value="c"> Menggumpalkan patogen<br>
            </li>
            <li>Perbezaan antara penguraian dan pemendakan:<br>
                <input type="radio" name="q9" value="a"> Penguraian memecahkan antigen, pemendakan menggumpalkan antigen<br>
                <input type="radio" name="q9" value="b"> Penguraian menggumpalkan, pemendakan memecah<br>
                <input type="radio" name="q9" value="c"> Kedua-duanya sama<br>
            </li>
            <li>Pemendakan penting kerana:<br>
                <input type="radio" name="q10" value="a"> Memudahkan sistem imun menghapuskan antigen<br>
                <input type="radio" name="q10" value="b"> Menghalang virus<br>
                <input type="radio" name="q10" value="c"> Menghasilkan antibodi<br>
            </li>
        </ol>
        <button onclick="checkAnswers()">Hantar Jawapan</button>
        <p id="quiz-feedback" style="font-weight:bold; color:green;"></p>
    </div>
</section>

<footer>
    &copy; 2025 Biologi Tingkatan 4 - Tindakan Antibodi
</footer>

<script>
let step = 0;
const steps = [
    "Antibodi mengenal pasti antigen pada patogen.",
    "Antibodi melekat pada antigen, menandakan patogen untuk dimusnahkan.",
    "Sel imun menyerang dan meneutralkan patogen.",
    "Patogen dimusnahkan, sistem imun kembali normal."
];

function showStep() {
    document.getElementById('step-description').innerText = steps[step];
    step = (step + 1) % steps.length;
}

function checkAnswers() {
    const correctAnswers = ['b','c','a','a','a','a','a','a','a','a'];
    let score = 0;
    for(let i=1; i<=10; i++){
        const options = document.getElementsByName('q'+i);
        for(let o of options){
            if(o.checked && o.value === correctAnswers[i-1]){
                score++;
            }
        }
    }
    document.getElementById('quiz-feedback').innerText = 'Skor anda: ' + score + ' / 10';
}
</script>

</body>
</html>
