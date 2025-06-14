<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jadwal Kegiatan Ambis</title>
    <!-- Memuat Tailwind CSS dari CDN. Ini adalah framework CSS yang membantu styling menjadi responsif dan cepat. -->
    <!-- Pastikan ada koneksi internet saat membuka file ini agar style Tailwind terunduh. -->
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <!-- Memuat font 'Inter' dari Google Fonts untuk tampilan teks yang modern dan mudah dibaca. -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        /* Mengatur font default untuk seluruh halaman menjadi 'Inter' */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #e2e8f0; /* Latar belakang abu-abu terang untuk nuansa modern */
        }

        /* Styling kustom untuk scrollbar pada browser berbasis Webkit (Chrome, Safari) */
        .custom-scrollbar::-webkit-scrollbar {
            width: 8px; /* Lebar scrollbar */
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #f1f1f1; /* Warna latar belakang track scrollbar */
            border-radius: 10px; /* Sudut membulat pada track */
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #a0aec0; /* Warna thumb scrollbar (abu-abu sedang) */
            border-radius: 10px; /* Sudut membulat pada thumb */
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover {
            background: #718096; /* Warna thumb saat di-hover (abu-abu gelap) */
        }

        /* Styling kustom untuk scrollbar pada Firefox */
        .custom-scrollbar {
            scrollbar-width: thin; /* Lebar scrollbar */
            scrollbar-color: #a0aec0 #f1f1f1; /* Warna thumb dan track */
        }
    </style>
</head>
<body class="min-h-screen flex items-center justify-center p-4">
    <!-- Kontainer utama untuk halaman web jadwal -->
    <!-- Menggunakan kelas Tailwind untuk: lebar maksimum (max-w-md untuk tablet/desktop, w-full untuk mobile),
         tinggi tetap (h-[90vh] agar bisa di-scroll jika terlalu panjang), bayangan (shadow-xl),
         sudut membulat (rounded-lg), padding (p-6), dan latar belakang putih. -->
    <div class="bg-white rounded-lg shadow-xl w-full max-w-sm md:max-w-md lg:max-w-lg h-[90vh] overflow-y-auto custom-scrollbar">
        <!-- Header atau Judul Halaman -->
        <h1 class="text-3xl md:text-4xl font-extrabold text-center text-blue-700 mb-6 pb-3 border-b-2 border-blue-200">
            Jadwal Kegiatan Ambisku!
        </h1>

        <!-- Daftar Kegiatan -->
        <!-- Menggunakan `space-y-4` untuk memberikan jarak vertikal antar item jadwal -->
        <div class="space-y-4">
            <!-- Setiap Item Jadwal -->
            <!-- Menggunakan kelas Tailwind untuk: latar belakang putih (bg-white), padding (p-4),
                 sudut membulat (rounded-xl), bayangan (shadow-sm), efek transisi hover (transition duration-300),
                 dan efek naik saat di-hover (hover:translate-y-[-3px] hover:shadow-md).
                 Flexbox digunakan untuk menyejajarkan ikon dan teks. -->
            <div class="bg-blue-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🕌</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">05.00 – 05.30</p>
                    <p class="text-lg font-semibold text-gray-800">Sholat Subuh & dzikir pagi</p>
                </div>
            </div>
            <div class="bg-purple-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">📖</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">05.30 – 06.00</p>
                    <p class="text-lg font-semibold text-gray-800">Tilawah Qur’an / murajaah ringan</p>
                </div>
            </div>
            <div class="bg-green-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">📚</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">06.00 – 07.00</p>
                    <p class="text-lg font-semibold text-gray-800">Belajar ringan / baca buku motivasi</p>
                </div>
            </div>
            <div class="bg-yellow-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🚿</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">07.00 – 07.30</p>
                    <p class="text-lg font-semibold text-gray-800">Mandi & sarapan sehat</p>
                </div>
            </div>
            <div class="bg-red-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🏫</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">08.15 – 12.15</p>
                    <p class="text-lg font-semibold text-gray-800">Pelat Sekul</p>
                </div>
            </div>
            <div class="bg-blue-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🍛</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">12.15 – 12.45</p>
                    <p class="text-lg font-semibold text-gray-800">Break + makan siang</p>
                </div>
            </div>
            <div class="bg-orange-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">📊</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">12.45 – 15.15</p>
                    <p class="text-lg font-semibold text-gray-800">Try Out AC</p>
                </div>
            </div>
            <div class="bg-purple-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🕊️</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">15.15 – 15.45</p>
                    <p class="text-lg font-semibold text-gray-800">Zikir sore & baca buku ringan</p>
                </div>
            </div>
            <div class="bg-red-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">✍️</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">16.00 – 17.30</p>
                    <p class="text-lg font-semibold text-gray-800">Pelat Dokmat</p>
                </div>
            </div>
            <div class="bg-yellow-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🛀</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">17.30 – 18.15</p>
                    <p class="text-lg font-semibold text-gray-800">Istirahat + mandi sore</p>
                </div>
            </div>
            <div class="bg-red-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">💻</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">18.30 – 21.00</p>
                    <p class="text-lg font-semibold text-gray-800">Pelat Koja</p>
                </div>
            </div>
            <div class="bg-purple-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">📿</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">21.00 – 21.30</p>
                    <p class="text-lg font-semibold text-gray-800">Baca Qur’an & murajaah hafalan</p>
                </div>
            </div>
            <div class="bg-green-50 p-4 rounded-xl shadow-sm flex items-start transition duration-300 ease-in-out transform hover:-translate-y-1 hover:shadow-md">
                <span class="text-2xl mr-3 mt-1">🧠</span>
                <div>
                    <p class="text-sm text-gray-500 font-medium">21.30 – 22.30</p>
                    <p class="text-lg font-semibold text-gray-800">Ulas ulang materi hari ini</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
