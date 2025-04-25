# Sentiment Analysis on Israel-Palestine Conflict using Reddit Data

Project Overview


Proyek ini bertujuan untuk menganalisis sentimen publik terkait konflik Israel-Palestina berdasarkan komentar dan postingan pengguna Reddit. Analisis ini bertujuan untuk memberikan wawasan objektif yang dapat digunakan oleh perusahaan media dalam membuat laporan berita yang akurat dan relevan.

Goals
	•	Membangun pipeline ETL untuk memproses data media sosial dengan cepat (kurang dari 12 jam).
	•	Melakukan analisa sentimen menggunakan teknik NLP (Natural Language Processing).
	•	Menyajikan visualisasi data menggunakan Tableau.
	•	Menghasilkan insight tentang opini publik terhadap konflik Israel-Palestina, terutama sejak Oktober 2023 hingga gencatan senjata di November 2024.

Tools & Technologies
	•	Python (Pandas, NLTK)
	•	Tableau
	•	PostgreSQL
	•	Great Expectations (untuk validasi data)
	•	Kaggle API & ACLED Data

Data Sources
	1.	Reddit Public Opinion Dataset
	•	Kaggle: Reddit on Israel-Palestine (https://www.kaggle.com/datasets/asaniczka/reddit-on-israel-palestine-daily-updated)
	2.	Israel Political Violence Events
	•	ACLED Dataset

Data Pipeline
	1.	Extract: Mengambil data dari Kaggle dan ACLED.
	2.	Transform:
	•	Label sentimen (positif, netral, negatif) menggunakan nltk.sentiment.
	•	Membuat kolom month_year.
	•	Menggabungkan dan membersihkan data.
	3.	Validate:
	•	Menggunakan Great Expectations untuk memastikan data sesuai ekspektasi (format, tipe data, non-null).
	4.	Load:
	•	Memasukkan data ke PostgreSQL dalam bentuk dimensi dan fakta (fact_comment, fact_assault, dim_user, dim_post, dim_date).

Key Insights
	•	Total komentar: 2.3 juta+
	•	Distribusi Sentimen:
	•	Negatif: 45.8%
	•	Netral: 21.3%
	•	Positif: 32.9%
	•	Topik dominan: Israel, diikuti oleh Palestina dan netral.
	•	Sentimen publik terhadap PBB didominasi oleh opini negatif.
	•	Uji T menunjukkan perubahan signifikan sentimen dari Oktober 2023 ke November 2024.

Success Stories
	•	Pipeline berjalan otomatis untuk ETL dari Kaggle ke PostgreSQL.
	•	Visualisasi sentimen berhasil ditampilkan di Tableau.
	•	Wawasan mendalam berhasil diperoleh, termasuk tren dukungan terhadap Israel dan Palestina.

Challenges & Future Improvements
	•	Integrasi cloud database (untuk efisiensi dan aksesibilitas).
	•	Data pengguna kurang lengkap (misalnya lokasi, umur akun).
	•	Potensi eksplorasi hubungan antara peristiwa besar dengan lonjakan sentimen.
