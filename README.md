# Wahyuhidayat
# Membuat list untuk menyimpan data mahasiswa
data_mahasiswa = []

# Perulangan untuk memasukkan data
while True:
    # Meminta input dari user
    nama = input("Masukkan nama mahasiswa: ")
    tugas = float(input("Masukkan nilai tugas: "))
    uts = float(input("Masukkan nilai UTS: "))
    uas = float(input("Masukkan nilai UAS: "))

    # Menghitung nilai akhir berdasarkan bobot
    nilai_akhir = tugas * 0.30 + uts * 0.35 + uas * 0.35

    # Menyimpan data mahasiswa dalam list
    data_mahasiswa.append({
        'nama': nama,
        'tugas': tugas,
        'uts': uts,
        'uas': uas,
        'nilai_akhir': nilai_akhir
    })

    # Menanyakan apakah user ingin menambah data lagi
    lanjut = input("Apakah Anda ingin menambah data? (y/t): ").lower()
    if lanjut == 't':
        break

# Menampilkan daftar data mahasiswa
print("\nDaftar Data Mahasiswa:")
for mahasiswa in data_mahasiswa:
    print(f"Nama: {mahasiswa['nama']}, Nilai Akhir: {mahasiswa['nilai_akhir']:.2f}")
