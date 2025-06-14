<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jadwal Kegiatan Saya</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Mengatur font default untuk seluruh body */
        body {
            font-family: 'Nunito Sans', sans-serif;
            background-color: #f7fafc; /* Warna latar belakang umum */
        }
        /* Styling untuk setiap item jadwal */
        .schedule-item {
            background-color: white; /* Latar belakang putih */
            border-radius: 0.5rem; /* Sudut membulat */
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06); /* Bayangan lembut */
            transition: transform 0.2s ease-in-out; /* Transisi untuk efek hover */
        }
        /* Efek saat kursor di atas item jadwal */
        .schedule-item:hover {
            transform: translateY(-3px); /* Sedikit naik saat di-hover */
        }
        /* Styling untuk scrollbar kustom pada browser berbasis Webkit (Chrome, Safari) */
        .custom-scrollbar::-webkit-scrollbar {
            width: 8px; /* Lebar scrollbar */
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #f1f1f1; /* Warna latar belakang track scrollbar */
            border-radius: 10px; /* Sudut membulat pada track */
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #cbd5e0; /* Warna thumb scrollbar (abu-abu terang) */
            border-radius: 10px; /* Sudut membulat pada thumb */
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover {
            background: #a0aec0; /* Warna thumb saat di-hover (abu-abu lebih gelap) */
        }
        /* Styling untuk scrollbar kustom pada Firefox */
        .custom-scrollbar {
            scrollbar-width: thin; /* Lebar scrollbar */
            scrollbar-color: #cbd5e0 #f1f1f1; /* Warna thumb dan track */
        }
    </style>
</head>
<body class="bg-gray-100 min-h-screen flex items-center justify-center p-4">
    <div class="bg-white rounded-lg shadow-xl w-full max-w-sm md:max-w-md lg:max-w-lg h-[90vh] overflow-y-auto p-6 custom-scrollbar">
        <h1 class="text-3xl font-bold text-center text-gray-800 mb-6 border-b-2 border-gray-200 pb-3">Jadwal Kegiatan Saya</h1>
        <div class="space-y-4">
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">🕌</span> <div>
                    <p class="text-sm text-gray-500 font-medium">05.00 – 05.30</p>
                    <p class="text-lg font-semibold text-gray-800">Sholat Subuh & dzikir pagi</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">📖</span> <div>
                    <p class="text-sm text-gray-500 font-medium">05.30 – 06.00</p>
                    <p class="text-lg font-semibold text-gray-800">Tilawah Qur’an / murajaah ringan</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">📘</span> <div>
                    <p class="text-sm text-gray-500 font-medium">06.00 – 07.00</p>
                    <p class="text-lg font-semibold text-gray-800">Belajar ringan / baca buku motivasi</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">🍽️</span> <div>
                    <p class="text-sm text-gray-500 font-medium">07.00 – 07.30</p>
                    <p class="text-lg font-semibold text-gray-800">Mandi & sarapan sehat</p>
                </div>
            </div>
             <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">🏫</span> <div>
                    <p class="text-sm text-gray-500 font-medium">08.15 – 12.15</p>
                    <p class="text-lg font-semibold text-gray-800">Pelat Sekul</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">🍛</span> <div>
                    <p class="text-sm text-gray-500 font-medium">12.15 – 12.45</p>
                    <p class="text-lg font-semibold text-gray-800">Break + makan siang</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">📊</span> <div>
                    <p class="text-sm text-gray-500 font-medium">12.45 – 15.15</p>
                    <p class="text-lg font-semibold text-gray-800">Try Out AC</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">🕊️</span> <div>
                    <p class="text-sm text-gray-500 font-medium">15.15 – 15.45</p>
                    <p class="text-lg font-semibold text-gray-800">Zikir sore & baca buku ringan</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">✍️</span> <div>
                    <p class="text-sm text-gray-500 font-medium">16.00 – 17.30</p>
                    <p class="text-lg font-semibold text-gray-800">Pelat Dokmat</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">🚿</span> <div>
                    <p class="text-sm text-gray-500 font-medium">17.30 – 18.15</p>
                    <p class="text-lg font-semibold text-gray-800">Istirahat + mandi sore</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">💻</span> <div>
                    <p class="text-sm text-gray-500 font-medium">18.30 – 21.00</p>
                    <p class="text-lg font-semibold text-gray-800">Pelat Koja</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">📿</span> <div>
                    <p class="text-sm text-gray-500 font-medium">21.00 – 21.30</p>
                    <p class="text-lg font-semibold text-gray-800">Baca Qur’an & murajaah hafalan</p>
                </div>
            </div>
            <div class="schedule-item p-4 flex items-start">
                <span class="text-2xl mr-3 mt-1">📚</span> <div>
                    <p class="text-sm text-gray-500 font-medium">21.30 – 22.30</p>
                    <p class="text-lg font-semibold text-gray-800">Ulas ulang materi hari ini</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
