<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jadwal Kegiatan Harian</title>
    <!-- Memuat Tailwind CSS dari CDN untuk styling yang responsif dan modern -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Memuat font 'Inter' dari Google Fonts untuk tampilan teks yang bersih dan mudah dibaca -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        /* Mengatur font default untuk seluruh halaman */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #e2e8f0; /* Latar belakang abu-abu terang untuk kontras */
        }

        /* Styling kustom untuk scrollbar (Webkit browsers seperti Chrome, Safari) */
        .custom-scrollbar::-webkit-scrollbar {
            width: 8px; /* Lebar scrollbar */
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #f1f1f1; /* Warna track scrollbar yang terang */
            border-radius: 10px; /* Sudut membulat */
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #cbd5e0; /* Warna thumb scrollbar yang sedikit gelap */
            border-radius: 10px; /* Sudut membulat */
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover {
            background: #a0aec0; /* Warna thumb saat di-hover */
        }

        /* Styling kustom untuk scrollbar (Firefox) */
        .custom-scrollbar {
            scrollbar-width: thin; /* Lebar scrollbar */
            scrollbar-color: #cbd5e0 #f1f1f1; /* Warna thumb dan track */
        }
    </style>
</head>
<body class="min-h-screen flex items-center justify-center p-4">
    <!-- Kontainer utama halaman web jadwal -->
    <!-- Latar belakang kontainer utama tetap putih untuk menciptakan kontras yang kuat dengan item jadwal berwarna gelap -->
    <div class="bg-white rounded-2xl shadow-2xl w-full max-w-sm md:max-w-md lg:max-w-lg h-[90vh] overflow-y-auto p-6 custom-scrollbar">
        <!-- Header atau Judul Halaman -->
        <h1 class="text-4xl md:text-5xl font-extrabold text-center text-indigo-800 mb-6 pb-3 border-b-4 border-indigo-500">
            Jadwal Kegiatan Harianmu!
        </h1>

        <!-- Daftar Kegiatan -->
        <!-- Menggunakan `space-y-4` untuk memberikan jarak vertikal antar item jadwal -->
        <div class="space-y-4">
            <!-- Setiap Item Jadwal -->
            <!-- Setiap item memiliki latar belakang warna cerah yang berbeda, bayangan, border kiri tebal,
                 dan efek hover (scale-105 untuk membesar, shadow-lg untuk bayangan lebih besar).
                 Warna teks disesuaikan agar mudah dibaca di latar belakang cerah. -->

            <div class="bg-blue-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-blue-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🕌</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">05.00 – 05.30</p>
                    <p class="text-lg font-bold text-gray-800">Sholat Subuh & Dzikir Pagi</p>
                </div>
            </div>
            <div class="bg-purple-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-purple-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">📖</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">05.30 – 06.00</p>
                    <p class="text-lg font-bold text-gray-800">Tilawah Qur’an / Murajaah Ringan</p>
                </div>
            </div>
            <div class="bg-green-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-green-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">💡</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">06.00 – 07.00</p>
                    <p class="text-lg font-bold text-gray-800">Belajar Ringan / Baca Buku Motivasi</p>
                </div>
            </div>
            <div class="bg-yellow-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-yellow-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🍽️</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">07.00 – 07.30</p>
                    <p class="text-lg font-bold text-gray-800">Mandi & Sarapan Sehat</p>
                </div>
            </div>
            <div class="bg-red-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-red-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🏫</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">08.15 – 12.15</p>
                    <p class="text-lg font-bold text-gray-800">Pelat Sekul</p>
                </div>
            </div>
            <div class="bg-indigo-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-indigo-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🍛</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">12.15 – 12.45</p>
                    <p class="text-lg font-bold text-gray-800">Break + Makan Siang</p>
                </div>
            </div>
            <div class="bg-orange-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-orange-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">📈</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">12.45 – 15.15</p>
                    <p class="text-lg font-bold text-gray-800">Try Out AC</p>
                </div>
            </div>
            <div class="bg-teal-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-teal-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🕊️</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">15.15 – 15.45</p>
                    <p class="text-lg font-bold text-gray-800">Zikir Sore & Baca Buku Ringan</p>
                </div>
            </div>
            <div class="bg-pink-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-pink-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">✍️</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">16.00 – 17.30</p>
                    <p class="text-lg font-bold text-gray-800">Pelat Dokmat</p>
                </div>
            </div>
            <div class="bg-lime-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-lime-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🛀</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">17.30 – 18.15</p>
                    <p class="text-lg font-bold text-gray-800">Istirahat + Mandi Sore</p>
                </div>
            </div>
            <div class="bg-cyan-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-cyan-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">💻</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">18.30 – 21.00</p>
                    <p class="text-lg font-bold text-gray-800">Pelat Koja</p>
                </div>
            </div>
            <div class="bg-fuchsia-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-fuchsia-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">📿</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">21.00 – 21.30</p>
                    <p class="text-lg font-bold text-gray-800">Baca Qur’an & Murajaah Hafalan</p>
                </div>
            </div>
            <div class="bg-emerald-100 p-4 rounded-xl shadow-md flex items-start border-l-4 border-emerald-300
                        transition transform duration-300 ease-in-out hover:scale-105 hover:shadow-lg">
                <span class="text-3xl mr-4 mt-0.5">🧠</span>
                <div>
                    <p class="text-sm text-gray-600 font-medium">21.30 – 22.30</p>
                    <p class="text-lg font-bold text-gray-800">Ulas Ulang Materi Hari Ini</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
