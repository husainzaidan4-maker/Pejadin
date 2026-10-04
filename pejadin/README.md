# PEJADIN (prototype)
Cara jalan di VS Code pada Windows (butuh Python 3.10+), dari folder project:

    py -m venv .venv
    .\.venv\Scripts\python.exe -m pip install -r backend\requirements.txt
    .\.venv\Scripts\python.exe -m uvicorn main:app --app-dir backend --reload --host 0.0.0.0 --port 8000

Buka http://localhost:8000. Untuk akses lewat VS Code Ports, teruskan port 8000. Database SQLite dibuat otomatis di `database/pejadin.db` beserta data contoh.
Login demo (password = username + 123): admin, operator, ppk, bendahara, pegawai (contoh: admin / admin123).

- `backend/main.py` API, mesin hitung (P1-P6), validasi V1-V9, alur status, audit, cetak HTML
- `frontend/index.html` antarmuka (satu halaman)
- `design/` acuan desain Stitch
Data pegawai/tarif adalah CONTOH; ganti dengan data klien. Tarif NTB dan Eselon I memakai angka dari contoh dokumen.
