# Laporan Interpretasi Hasil
## Analisis Network Pharmacology Metabolit Carica papaya (Daun Pepaya) terhadap Penyakit Malaria
_Carica papaya_, atau yang biasa dikenal sebagai pepaya, adalah tumbuhan tropis yang dikenal luas di Indonesia. Daunnya sendiri telah banyak digunakan sebagai pengobatan tradisional karena kandungan antiinflamasi, antimikroba, dan aktivitas fitokimia lainnya. Di samping itu, studi oleh Arwansyah et al. (2025) melaporkan adanya kandungan metabolit yang diidentifikasi berpotensi sebagai agen antimalaria dengan menargetkan situs protein yang berperan dalam siklus hidup parasit tersebut. Analisis ini bertujuan untuk mengidentifikasi senyawa bioaktif di C. papaya yang berpotensi sebagai alternatif terapi antimalaria.

Tabel 1. Daftar metabolit _Carica papaya_ hasil identifikasi menggunakan IJAH Analytics

![Tabel Daftar Metabolit](/Picture1.png "Tabel Daftar Metabolit")
 
Sebanyak 17 metabolit aktif C. papaya  diidentifikasi melalui database IJAH Analytics (Tabel 1). Struktur SMILES masing-masing senyawa diperoleh melalui PubChem dan digunakan untuk memprediksi target protein menggunakan SwissTargetPrediction. Gen yang beruhubungan dengan malaria diperoleh dari OMIM. Analisis irisan antara target senyawa dan gen malaria menghasilkan 14 target potensial, yaitu ACP1, CCR5, TLR2, MET, IDO1, MYC, TLR4, CYP2C19, CD81, NOS2, ICAM1, ADA, TLR7, dan G6PD. Selanjutnya, Protein-Protein Interaction (PPI) _network_ dikonstruksi menggunakan STRING (confidence ≥ 0,700) dan divisualisasikan dengan Cytoscape. Analisis Gene Ontology dan KEGG pathway dilakukan menggunakan STRING (FDR < 0,05), kemudian hasilnya diintegrasikan dengan jaringan senyawa-target dan PPI menggunakan fitur Merge Network pada Cytoscape.

![Gambar Irisan Gen](/Picture2.png "Gambar Irisan Gen")
 
Gambar 1. Irisan gen target malaria dan target metabolit _Carica papaya_

Analisis menggunakan diagram Venn (Gambar 1) menunjukkan terdapat 14 gen irisan antara gen terkait malaria dan target dari metabolit _C. papaya_. Hal ini mengindikasikan potensi metabolit tersebut dalam memodulasi jalur biologis yang berkaitan dengan patofisiologi malaria. Daftar gen irisan tersebut dimasukkan ke dalam platform STRING untuk membangun jaringan protein–protein interaction (PPI) dan mengidentifikasi hub protein menggunakan plugin CytoHubba. Interaksi antara gen-gen tersebut ditunjukkan pada Gambar 2 yang direpresentasikan oleh 14 node dan 8 edge. Top 7 hub gen (Tabel 2) diidentifikasi menggunakan algoritma Maximal Clique Centrality (MCC) pada plugin CytoHubba.

Tabel 2. Nilai Maximal Clique Centrality (MCC), _degree, betweenness centrality,_ dan _closeness centrality_ dari tujuh hub protein hasil analisis jaringan PPI

![Tabel MCC](/Picture3.png "Tabel MCC")
 
Maximal Clique Centrality (MCC) merupakan metode dalam analisis jaringan yang digunakan untuk mengidentifikasi hub protein berdasarkan keterlibatan suatu node dalam _maximal clique_, yaitu kelompok protein yang saling berinteraksi secara langsung. Semakin tinggi nilai MCC, semakin besar peran protein tersebut sebagai hub dalam jaringan PPI. _Degree_ menunjukkan seberapa banyak koneksi langsung yang dimiliki satu protein dengan protein lain dalam jaringan. Semakin tinggi _degree_, semakin banyak protein lain yang berinteraksi langsung dengannya. _Betweenness centrality_ menggambarkan seberapa sering suatu protein berada pada jalur terpendek antara dua protein lain dalam jaringan. Sementara itu, _closeness centrality_ menunjukkan kedekatan suatu protein terhadap seluruh protein lain dalam jaringan, yang mencerminkan efisiensi protein tersebut dalam menjangkau atau dipengaruhi oleh protein lain melalui jalur interaksi. Berdasarkan Tabel 2, TLR4 memiliki nilai MCC tertinggi (5), diikuti oleh ICAM1 (3) dan TLR2 (2), sedangkan CCR5, NOS2, TLR7, dan CD81 masing-masing memiliki nilai MCC sebesar 1. Selain itu, TLR4 dan ICAM1 juga menunjukkan nilai _betweenness centrality_ dan _closeness centrality_ tertinggi dibandingkan dengan protein lainnya. Temuan ini mengindikasikan bahwa kedua protein tersebut berpotensi berperan sebagai protein sentral dalam jaringan PPI dan dapat menjadi target utama yang memediasi mekanisme kerja metabolit _C. papaya_ terhadap malaria.

![Gambar PPI](/Picture4.png "Gambar PPI")

Gambar 2. Jaringan Protein-Protein Interaction (PPI) dari 14 gen irisan hasil konstruksi STRING

![Gambar Network](/Picture5.png "Gambar Network")
 
Gambar 3. Visualisasi jaringan interaksi senyawa–target–_pathway_

Gambar 3 menunjukkan visualisasi _network pharmacology_ yang mengintegrasikan 13 metabolit aktif _C. papaya_ yang terhubung dalam jaringan, protein target hasil irisan, dan sembilan KEGG pathway yang signifikan. Hasil ini menunjukkan bahwa metabolit aktif _C. papaya_ berpotensi bekerja secara multi-target melalui berbagai jalur biologis yang saling berkaitan, dengan _Malaria_ sebagai _pathway_ utama yang menjadi fokus penelitian, disertai jalur terkait lainnya seperti _Toll-like receptor signaling pathway, African trypanosomiasis, leishmaniasis, toxoplasmosis,_ dan _Chagas disease_. Berdasarkan jumlah koneksi (_degree_) pada jaringan, TLR4 merupakan protein dengan interaksi terbanyak (_degree_ = 20), diikuti oleh TLR2 (_degree_ = 11) dan ICAM1 (_degree_ = 7). Dari sisi metabolit, Glucotropeolin dan β-cryptoxanthin menunjukkan jumlah koneksi tertinggi (_degree_ = 3), mengindikasikan potensi keduanya dalam memodulasi beberapa protein target secara bersamaan. Selain itu, _Malaria pathway_ memiliki jumlah koneksi tertinggi (_degree_ = 5), menunjukkan bahwa jalur tersebut merupakan fokus utama interaksi antara metabolit aktif _C. papaya_ dan protein target yang terkait dengan malaria.

![Gambar BP](/Picture6.png "Gambar BP")

![Gambar MF](/Picture7.png "Gambar MF")

![Gambar KEGG Pathway](/Picture8.png "Gambar KEGG Pathwa")

Gambar 4. Hasil _enrichment analysis Gene Ontology (Biological Process, Molecular Function)_ dan KEGG Pathway terhadap target irisan

Analisis _Gene Ontology (Biological Process)_ menunjukkan bahwa protein target hasil irisan diperkaya pada berbagai proses yang berkaitan dengan respons imun dan inflamasi. Proses dengan tingkat pengayaan tertinggi meliputi _I-kappaB phosphorylation, nitric oxide metabolic process,_ dan _positive regulation of interleukin-8 production,_ yang ditandai oleh nilai signal tinggi dan FDR yang rendah. Temuan ini menunjukkan bahwa target protein berpotensi memodulasi jalur inflamasi dan respons imun yang berperan dalam patogenesis malaria. Pada kategori _Molecular Function_, ditemukan pengayaan signifikan pada _pattern recognition receptor activity,_ yang sejalan dengan keberadaan TLR4 dan TLR2 sebagai salah satu hub gene dominan pada jaringan PPI (Gambar 2). Sementara itu, analisis KEGG pathway menunjukkan keterlibatan protein target pada jalur _Malaria,_ yang merupakan jalur sentral dalam patogenesis penyakit tersebut. Secara keseluruhan, hasil enrichment ini memperkuat indikasi bahwa metabolit aktif _C. papaya_ berpotensi memodulasi malaria melalui regulasi respons imun bawaan dan proses inflamasi, terutama yang dimediasi oleh _Toll-like receptors,_ produksi sitokin proinflamasi, serta metabolisme nitric oxide.

__Referensi:__

Arwansyah, A., Rahmawati, S., Nuryanti, S., Yusuf, Y., Hartono and Arif, A.R. (2025). Molecular investigation on active compounds in papaya leaves (Carica papaya Linn) as anti-malaria using network pharmacology, molecular docking, clustering-based analysis and molecular dynamics simulation. Phytomedicine Plus, 5(1), p.100713. doi:10.1016/j.phyplu.2024.100713.
