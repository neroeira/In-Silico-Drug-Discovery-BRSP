# Molecular Docking TLR2 dan β-Cryptoxanthin
_Molecular docking_ adalah tahapan _virtual screening_ dalam _drug discovery_ yang bertujuan untuk menganalisis hubungan protein-ligan demi memperoleh kandidat yang cocok sebagai agen terapeutik. Pada tugas ini, saya mengidentifikasi interaksi antara _Toll-Like Receptor_ 2 (TLR2) (PDB ID: 2Z80) dengan ligan β-Cryptoxanthin.

TLR2 adalah reseptor transmembran pada sel-sel imun yang berfungsi untuk mengenali pola molekuler khas yang berasosiasi dengan patogen (_pathogen-associated molecular patterns_, PAMPs). Pengikatan PAMPs dengan TLR2 akan mengaktifkan jalur NF-κB dan MAPK, yang akhirnya mengarah pada peningkatan produksi sitokin proinflamasi seperti TNF-α, IL-1β, IL-6, dan IL-12, sehingga respons inflamasi meningkat. Respons inflamasi yang berlebihan akibat aktivasi TLR2 berkontribusi terhadap kerusakan jaringan dan perkembangan malaria berat. Oleh karena itu, TLR2 menjadi target potensial dalam pengembangan terapi antimalaria berbasis modulasi respons imun. Melalui pendekatan Structure-Based Drug Design (SBDD), β-cryptoxanthin dianalisis terhadap _binding pocket_ TLR2 untuk mengevaluasi potensinya sebagai senyawa yang dapat memodulasi aktivasi reseptor tersebut.

Tabel 1. Karakteristik protein target dan ligan pada simulasi _molecular docking_



Berdasarkan hasil analisis _network pharmacology_, TLR2 dipilih sebagai target protein untuk _molecular docking_ karena merupakan salah satu hub protein yang berperan dalam jalur malaria. Struktur tiga dimensi TLR2 diperoleh dari Protein Data Bank (RCSB PDB), sedangkan struktur β-cryptoxanthin dalam format SMILES diperoleh dari PubChem.

Analisis dilakukan secara _web-based_ melalui laman SwissDock. Kode SMILES β-cryptoxanthin dimasukkan pada kolom ligan, dan fitur _Prepare Ligand_ digunakan agar molekul siap untuk simulasi. Pada tahap preparasi reseptor, ID PDB 2Z80 dimasukkan pada kolom target, kemudian dipilih _chains_ yang digunakan, yaitu _chain_ A dan B. Opsi Heteroatoms diatur menjadi _None_ sehingga molekul non-protein, termasuk residu karbohidrat N-acetyl-D-glucosamine (NAG) yang terdapat pada struktur kristal TLR2, tidak disertakan dalam proses _docking_. Hal ini bertujuan untuk mencegah potensi gangguan terhadap prediksi interaksi antara β-cryptoxanthin dan TLR2. Koordinat pusat yang digunakan dalam _search space_ diperoleh melalui laman PrankWeb, yaitu 9.4224, -15.1802, dan -13.1093.

![Gambar _Center Box_](/Picture10.png "Gambar _Center Box_")

Gambar 1. Pencarian _center box_ terbaik melalui PrankWeb

![Gambar Pose](/Picture11.png "Gambar Pose")

Gambar 2. Visualisasi pose β-Cryptoxanthin pada _binding pocket_ reseptor TLR2

Tabel 2. Hasil afinitas _molecular docking_

![Tabel Hasil Afinitas](/Picture12.png "Tabel Hasil Afinitas")
 
Simulasi _docking_ antara ligan dan reseptor menghasilkan 2 model konformasi, dengan model 1 memberikan nilai _Calculated Affinity_ sebesar -5.201 kcal/mol. Nilai afinitas negatif ini menunjukkan bahwa β-cryptoxanthin memiliki kemampuan untuk berikatan secara spontan dengan reseptor TLR2, sehingga berpotensi membentuk kompleks ligan–reseptor yang stabil. Meskipun nilai afinitas ini tidak sekuat inhibitor dengan afinitas tinggi, hasil tersebut tetap menunjukkan adanya interaksi yang secara termodinamik menguntungkan (_energetically favorable_), sehingga β-cryptoxanthin berpotensi memodulasi aktivitas TLR2.
	
Secara visual, β-cryptoxanthin tampak berikatan pada _binding pocket_ reseptor TLR2 dengan orientasi yang stabil. Posisi ini menunjukkan bahwa β-cryptoxanthin memiliki potensi untuk berinteraksi dengan residu-residu penting pada kantong pengikatan TLR2. Meskipun demikian, hasil molecular docking belum dapat memastikan mekanisme inhibisi maupun aktivasi reseptor, sehingga diperlukan validasi lebih lanjut melalui pendekatan komputasional lanjutan maupun uji eksperimental. Selama proses simulasi menggunakan SwissDock, saya memahami bahwa pemilihan struktur protein yang sesuai, preparasi reseptor yang tepat, serta penentuan _search space_ berdasarkan prediksi _binding pocket_ dari PrankWeb sangat memengaruhi hasil docking.

Praktikum ini menunjukkan bahwa _molecular docking_ merupakan salah satu pendekatan komputasional yang penting dalam proses _drug discovery_. Pendekatan in silico seperti ini mampu mempercepat proses identifikasi kandidat senyawa yang berpotensi dikembangkan sebagai agen terapeutik.
