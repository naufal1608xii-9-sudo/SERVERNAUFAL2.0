<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nizar | Personal Portfolio</title>
  <meta name="description" content="Portfolio Naufal Nizar Muzakki, pelajar, public speaker, dan barista manual brew enthusiast dari Subang.">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css"> <!-- pakai CSS yang sudah kita gabung -->
</head>
<body>

<header>
  <h1>Nizar</h1>
  <nav>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#education">Education</a>
    <a href="#contact">Contact</a>
  </nav>
  <button onclick="toggleMode()" id="modeBtn">🌙</button>
</header>

<section class="hero">
  <div>
   <img src="https://drive.google.com/uc?export=view&id=1X1bSHD_VHvxuLlvXs6-EF4RS3Po3LOZL" 
     alt="Foto Nizar" style="border-radius:50%; width:150px; margin-bottom:20px;">

         alt="Foto Nizar" style="border-radius:50%; width:150px; margin-bottom:20px;">
    <h2>Hi, I’m <span>Nizar</span></h2>
    <p>
      Pelajar, public speaker, dan barista manual brew yang percaya bahwa
      komunikasi dan ketelitian adalah kunci dalam setiap proses.
    </p>
  </div>
</section>

<section id="about">
  <h2>About Me</h2>
  <div class="card">
    Saya pelajar SMAN 1 Subang, aktif berorganisasi dan memiliki ketertarikan
    pada public speaking serta dunia kopi manual brew.
  </div>
</section>

<section id="skills">
  <h2>Skills</h2>
  <div class="grid">

    <div class="card" onclick="openSkill(
      'Public Speaking',
      'Saya terbiasa berbicara di depan umum sebagai MC, moderator, dan pembicara dalam berbagai kegiatan sekolah maupun organisasi. Saya mampu menyampaikan pesan dengan artikulasi yang jelas, intonasi yang tepat, serta bahasa yang mudah dipahami oleh audiens.\n\nSelain itu, saya mampu membaca suasana, membangun interaksi dengan audiens, dan mengatur alur acara agar berjalan dengan baik. Kemampuan ini membantu saya menciptakan komunikasi yang efektif dan berkesan.'
    )">
      🎤 Public Speaking
    </div>

    <div class="card" onclick="openSkill(
      'Barista Manual Brew',
      'Saya memiliki ketertarikan dan pemahaman dalam dunia kopi manual brew, khususnya metode seperti V60 dan Japanese. Saya memahami dasar-dasar ekstraksi kopi, rasio air, grind size, serta teknik penyeduhan untuk menghasilkan cita rasa terbaik.\n\nMelalui ketelitian dan konsistensi, saya mampu menyajikan kopi dengan karakter rasa yang seimbang. Ketertarikan ini juga melatih kesabaran, fokus, dan perhatian terhadap detail.'
    )">
      ☕ Barista Manual Brew
    </div>

    <div class="card" onclick="openSkill(
      'Leadership',
      'Saya memiliki pengalaman kepemimpinan aktif dalam organisasi kepramukaan. Saya menjabat sebagai Wakil Ketua DKR periode 2026–2029, di mana saya berperan dalam membantu mengoordinasikan program kerja, mengawasi jalannya kegiatan, serta mendukung ketua dalam pengambilan keputusan strategis.\n\nSelain itu, saya juga dipercaya sebagai Ketua Pelaksana Gema Pramuka bagian Penggalang tahun 2025. Dalam peran ini, saya bertanggung jawab atas perencanaan, koordinasi panitia, dan kelancaran kegiatan, sehingga melatih saya untuk bersikap tegas, bertanggung jawab, serta mampu memimpin tim dalam situasi yang dinamis.'
    )">
      🤝 Leadership
    </div>

    <div class="card" onclick="openSkill(
      'Communication',
      'Saya memiliki kemampuan komunikasi yang baik, baik secara lisan maupun tulisan. Saya mampu menyampaikan ide, pendapat, dan informasi dengan jelas serta terstruktur.\n\nKemampuan komunikasi ini membantu saya dalam bekerja sama dengan orang lain, membangun relasi yang positif, serta menyelesaikan masalah secara efektif dalam berbagai situasi.'
    )">
      🗣️ Communication
    </div>

  </div>
</section>

<section id="education">
  <h2>Education</h2>
  <div class="grid">
    <div class="card">SD Negeri Soklat (2014-2020)</div>
    <div class="card">SMP IT Al-Majid (2020-2023)</div>
    <div class="card">SMA Negeri 1 Subang (2023-2026)</div>
  </div>
</section>

<section id="contact">
  <h2>Contact</h2>
  <div class="grid">
    <div class="card">
      📧 Email: <a href="mailto:beatbeekun1608@gmail.com">beatbeekun1608@gmail.com</a>
    </div>
    <div class="card">
      📞 WhatsApp: <a href="https://wa.me/6285322580511" target="_blank">085322580511</a>
    </div>
    <div class="card">
      📷 Instagram: <a href="https://instagram.com/beatbee__" target="_blank">@beatbee__</a>
    </div>
  </div>
</section>

<footer>
  © 2026 Naufal Nizar Muzakki
</footer>

<!-- MODAL SKILL -->
<div id="skillModal" class="modal" onclick="closeModal()">
  <div class="modal-content" onclick="event.stopPropagation()">
    <h3 id="modalTitle"></h3>
    <p id="modalDesc"></p>
    <button onclick="closeModal()">Tutup</button>
  </div>
</div>

<script>
  function toggleMode() {
    document.body.classList.toggle("light");
    document.getElementById("modeBtn").textContent =
      document.body.classList.contains("light") ? "🌞" : "🌙";
  }

  function openSkill(title, desc) {
    document.getElementById("modalTitle").textContent = title;
    document.getElementById("modalDesc").textContent = desc;
    document.getElementById("skillModal").classList.add("show");
  }

  function closeModal() {
    document.getElementById("skillModal").classList.remove("show");
  }
</script>

</body>
</html>
