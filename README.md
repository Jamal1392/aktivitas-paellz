import React, { useState } from 'react';

// Data jadwal kegiatan lengkap dengan ikon, warna, dan manfaatnya
const scheduleData = [
    {
        time: '05.00 – 05.30',
        activity: 'Sholat Subuh & Dzikir Pagi',
        icon: '🕌',
        color: 'bg-blue-100 border-blue-300',
        benefits: 'Meningkatkan ketenangan jiwa, memulai hari dengan keberkahan, serta membangun fondasi spiritual yang kuat untuk aktivitas sepanjang hari.'
    },
    {
        time: '05.30 – 06.00',
        activity: 'Tilawah Qur’an / Murajaah Ringan',
        icon: '📖',
        color: 'bg-purple-100 border-purple-300',
        benefits: 'Mempertajam memori, menenangkan hati, dan mendekatkan diri kepada Tuhan, yang membantu meningkatkan konsentrasi dan kejernihan pikiran.'
    },
    {
        time: '06.00 – 07.00',
        activity: 'Belajar Ringan / Baca Buku Motivasi',
        icon: '💡',
        color: 'bg-green-100 border-green-300',
        benefits: 'Menginspirasi, menambah wawasan baru, dan mempersiapkan mental positif untuk menghadapi tantangan hari ini.'
    },
    {
        time: '07.00 – 07.30',
        activity: 'Mandi & Sarapan Sehat',
        icon: '🍽️',
        color: 'bg-yellow-100 border-yellow-300',
        benefits: 'Menyegarkan tubuh dan pikiran, serta memberikan energi esensial yang diperlukan untuk fokus dan produktif.'
    },
    {
        time: '08.15 – 12.15',
        activity: 'Pelat Sekul',
        icon: '🏫',
        color: 'bg-red-100 border-red-300',
        benefits: 'Meningkatkan pemahaman materi pelajaran sekolah, melatih kemampuan pemecahan masalah, dan mempersiapkan diri untuk ujian penting.'
    },
    {
        time: '12.15 – 12.45',
        activity: 'Break + Makan Siang',
        icon: '🍛',
        color: 'bg-indigo-100 border-indigo-300',
        benefits: 'Mengisi ulang energi setelah sesi belajar yang panjang, menjaga konsentrasi, dan memberikan jeda bagi pikiran untuk istirahat sejenak.'
    },
    {
        time: '12.45 – 15.15',
        activity: 'Try Out AC',
        icon: '📈',
        color: 'bg-orange-100 border-orange-300',
        benefits: 'Mengukur kemampuan diri, mengidentifikasi area kelemahan yang perlu diperbaiki, dan melatih manajemen waktu saat ujian yang sesungguhnya.'
    },
    {
        time: '15.15 – 15.45',
        activity: 'Zikir Sore & Baca Buku Ringan',
        icon: '🕊️',
        color: 'bg-teal-100 border-teal-300',
        benefits: 'Mengurangi stres, menenangkan pikiran, dan mengisi ulang energi mental setelah aktivitas padat seharian.'
    },
    {
        time: '16.00 – 17.30',
        activity: 'Pelat Dokmat',
        icon: '✍️',
        color: 'bg-pink-100 border-pink-300',
        benefits: 'Mendalami materi khusus, memperkuat konsep-konsep inti, dan mengembangkan keterampilan analisis serta pemecahan masalah yang kompleks.'
    },
    {
        time: '17.30 – 18.15',
        activity: 'Istirahat + Mandi Sore',
        icon: '🛀',
        color: 'bg-blue-100 border-blue-300',
        benefits: 'Merilekskan otot-otot yang tegang, membersihkan diri, dan mempersiapkan tubuh untuk sesi belajar atau aktivitas malam hari.'
    },
    {
        time: '18.30 – 21.00',
        activity: 'Pelat Koja',
        icon: '💻',
        color: 'bg-red-100 border-red-300',
        benefits: 'Latihan soal intensif, melatih kecepatan dan akurasi, serta mengembangkan strategi pengerjaan soal yang efektif.'
    },
    {
        time: '21.00 – 21.30',
        activity: 'Baca Qur’an & Murajaah Hafalan',
        icon: '📿',
        color: 'bg-purple-100 border-purple-300',
        benefits: 'Mempertahankan hafalan Al-Qur’an, memberikan ketenangan batin sebelum tidur, dan memperkuat hubungan spiritual.'
    },
    {
        time: '21.30 – 22.30',
        activity: 'Ulas Ulang Materi Hari Ini',
        icon: '🧠',
        color: 'bg-green-100 border-green-300',
        benefits: 'Menguatkan pemahaman materi yang telah dipelajari, membantu mengingat informasi lebih baik, dan mempersiapkan diri untuk pembelajaran esok hari.'
    },
];

// Komponen utama aplikasi React
function App() {
    // State untuk menyimpan aktivitas yang dipilih (untuk menampilkan detail manfaat)
    const [selectedActivity, setSelectedActivity] = useState(null);
    // State untuk mengontrol tampilan modal (pop-up)
    const [isModalOpen, setIsModalOpen] = useState(false);

    // Fungsi untuk menangani klik pada item jadwal
    const handleItemClick = (activity) => {
        setSelectedActivity(activity); // Set aktivitas yang dipilih
        setIsModalOpen(true); // Buka modal
    };

    // Fungsi untuk menutup modal
    const closeModal = () => {
        setIsModalOpen(false); // Tutup modal
        setSelectedActivity(null); // Kosongkan aktivitas yang dipilih
    };

    return (
        // Wrapper utama halaman web dengan latar belakang gradien dan centering
        <div className="min-h-screen bg-gradient-to-br from-blue-300 to-indigo-500 flex items-center justify-center p-4">
            {/* Kontainer utama jadwal, responsif dan bisa di-scroll */}
            <div className="bg-white rounded-2xl shadow-2xl w-full max-w-sm md:max-w-md lg:max-w-lg h-[90vh] overflow-y-auto p-6 relative">
                {/* Judul Halaman */}
                <h1 className="text-4xl font-extrabold text-center text-blue-800 mb-6 pb-3 border-b-4 border-blue-400">
                    Jadwal Kerenku!
                </h1>

                {/* Grid untuk elemen grafis matematis (jika diinginkan, bisa ditambahkan di sini) */}
                {/* Contoh: <div className="absolute inset-0 opacity-10 bg-grid-pattern z-0"></div> */}

                {/* Daftar Kegiatan */}
                <div className="space-y-4 relative z-10">
                    {scheduleData.map((item, index) => (
                        <div
                            key={index} // Key unik untuk setiap item dalam list
                            className={`p-4 rounded-xl border-l-4 ${item.color} shadow-md flex items-start cursor-pointer 
                                transition transform hover:-translate-y-1 hover:shadow-lg hover:border-r-4`}
                            onClick={() => handleItemClick(item)} // Menangani klik item
                        >
                            <span className="text-3xl mr-4 mt-0.5">{item.icon}</span>
                            <div>
                                <p className="text-sm text-gray-600 font-medium">{item.time}</p>
                                <p className="text-lg font-bold text-gray-800">{item.activity}</p>
                            </div>
                        </div>
                    ))}
                </div>
            </div>

            {/* Modal untuk menampilkan detail manfaat */}
            {isModalOpen && selectedActivity && (
                <div className="fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center p-4 z-50 animate-fade-in">
                    <div className="bg-white rounded-lg p-6 max-w-sm w-full shadow-2xl relative animate-scale-in">
                        {/* Tombol Tutup Modal */}
                        <button
                            onClick={closeModal}
                            className="absolute top-3 right-3 text-gray-500 hover:text-gray-800 text-2xl font-bold transition duration-200"
                        >
                            &times;
                        </button>
                        <h2 className="text-2xl font-bold text-gray-800 mb-4 border-b pb-2">
                            {selectedActivity.icon} {selectedActivity.activity}
                        </h2>
                        <p className="text-gray-700 leading-relaxed">
                            {selectedActivity.benefits}
                        </p>
                    </div>
                </div>
            )}

            {/* Tailwind CSS Customization (bisa di-load melalui CDN di head, tapi disematkan di sini untuk contoh) */}
            <style>
                {`
                /* Animasi Fade In untuk Modal Overlay */
                @keyframes fade-in {
                    from { opacity: 0; }
                    to { opacity: 1; }
                }
                .animate-fade-in {
                    animation: fade-in 0.3s ease-out forwards;
                }

                /* Animasi Scale In untuk Konten Modal */
                @keyframes scale-in {
                    from { transform: scale(0.9); opacity: 0; }
                    to { transform: scale(1); opacity: 1; }
                }
                .animate-scale-in {
                    animation: scale-in 0.3s ease-out forwards;
                }

                /* Custom Scrollbar */
                .overflow-y-auto::-webkit-scrollbar {
                    width: 8px;
                }
                .overflow-y-auto::-webkit-scrollbar-track {
                    background: #f0f0f0;
                    border-radius: 10px;
                }
                .overflow-y-auto::-webkit-scrollbar-thumb {
                    background: #cbd5e0;
                    border-radius: 10px;
                }
                .overflow-y-auto::-webkit-scrollbar-thumb:hover {
                    background: #a0aec0;
                }
                `}
            </style>
        </div>
    );
}

export default App;
