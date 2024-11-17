<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Materi Algoritma</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            padding: 20px;
            max-width: 1000px;
            margin: 0 auto;
        }

        h1 {
            text-align: center;
            margin-bottom: 30px;
        }

        h2 {
            color: #2c3e50;
            margin: 20px 0;
        }

        h3 {
            color: #34495e;
            margin: 15px 0;
        }

        .algorithm {
            background: #f9f9f9;
            padding: 20px;
            border-radius: 5px;
            margin: 20px 0;
        }

        pre {
            background: #f4f4f4;
            padding: 15px;
            border-radius: 5px;
            overflow-x: auto;
        }

        .flowchart {
            width: 100%;
            height: 400px;
            background: #fff;
            border: 1px solid #ddd;
            margin: 10px 0;
        }

        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <h1>Materi Algoritma</h1>

    <div class="algorithm">
        <h2>1. Menghitung Luas Persegi</h2>
        
        <h3>Notasi Deskriptif</h3>
        <pre>
1. Mulai
2. Masukkan nilai sisi
3. Hitung luas = sisi × sisi
4. Tampilkan luas
5. Selesai</pre>

        <h3>Flowchart</h3>
        <div class="flowchart">
            <!-- Flowchart akan ditambahkan menggunakan JavaScript -->
        </div>

        <h3>Code C++</h3>
        <pre>
#include &lt;iostream&gt;
using namespace std;

int main() {
    float sisi, luas;
    
    cout << "Masukkan panjang sisi: ";
    cin >> sisi;
    
    luas = sisi * sisi;
    
    cout << "Luas persegi adalah: " << luas;
    return 0;
}</pre>
    </div>

    <div class="algorithm">
        <h2>2. Menentukan Bilangan Ganjil atau Genap</h2>
        
        <h3>Notasi Deskriptif</h3>
        <pre>
1. Mulai
2. Masukkan bilangan
3. Jika bilangan mod 2 = 0
   - Tampilkan "Bilangan Genap"
   Jika tidak
   - Tampilkan "Bilangan Ganjil"
4. Selesai</pre>

        <h3>Flowchart</h3>
        <div class="flowchart">
            <!-- Flowchart akan ditambahkan menggunakan JavaScript -->
        </div>

        <h3>Code C++</h3>
        <pre>
#include &lt;iostream&gt;
using namespace std;

int main() {
    int bilangan;
    
    cout << "Masukkan bilangan: ";
    cin >> bilangan;
    
    if(bilangan % 2 == 0)
        cout << "Bilangan Genap";
    else
        cout << "Bilangan Ganjil";
    
    return 0;
}</pre>
    </div>

    <div class="algorithm">
        <h2>3. Menghitung Rata-rata dari N Bilangan</h2>
        
        <h3>Notasi Deskriptif</h3>
        <pre>
1. Mulai
2. Masukkan jumlah bilangan (N)
3. Set total = 0
4. Untuk i = 1 sampai N, lakukan:
   - Masukkan bilangan ke-i
   - total = total + bilangan
5. Hitung rata-rata = total / N
6. Tampilkan rata-rata
7. Selesai</pre>

        <h3>Flowchart</h3>
        <div class="flowchart">
            <!-- Flowchart akan ditambahkan menggunakan JavaScript -->
        </div>

        <h3>Code C++</h3>
        <pre>
#include &lt;iostream&gt;
using namespace std;

int main() {
    int N, bilangan;
    float total = 0, rata;
    
    cout << "Masukkan jumlah bilangan: ";
    cin >> N;
    
    for(int i = 1; i <= N; i++) {
        cout << "Masukkan bilangan ke-" << i << ": ";
        cin >> bilangan;
        total += bilangan;
    }
    
    rata = total / N;
    cout << "Rata-rata = " << rata;
    
    return 0;
}</pre>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/8.11.0/mermaid.min.js"></script>
    <script>
        mermaid.initialize({startOnLoad: true});
        
        // Flowchart definitions
        const flowcharts = document.querySelectorAll('.flowchart');
        
        // Luas Persegi
        flowcharts[0].innerHTML = `
        <div class="mermaid">
        graph TD
            A[Mulai] --> B[Masukkan sisi]
            B --> C[Hitung luas = sisi × sisi]
            C --> D[Tampilkan luas]
            D --> E[Selesai]
        </div>`;
        
        // Ganjil Genap
        flowcharts[1].innerHTML = `
        <div class="mermaid">
        graph TD
            A[Mulai] --> B[Masukkan bilangan]
            B --> C{bilangan mod 2 = 0?}
            C -->|Ya| D[Tampilkan "Bilangan Genap"]
            C -->|Tidak| E[Tampilkan "Bilangan Ganjil"]
            D --> F[Selesai]
            E --> F
        </div>`;
        
        // Rata-rata
        flowcharts[2].innerHTML = `
        <div class="mermaid">
        graph TD
            A[Mulai] --> B[Masukkan N]
            B --> C[total = 0]
            C --> D[i = 1]
            D --> E{i <= N?}
            E -->|Ya| F[Masukkan bilangan ke-i]
            F --> G[total = total + bilangan]
            G --> H[i = i + 1]
            H --> E
            E -->|Tidak| I[rata = total / N]
            I --> J[Tampilkan rata]
            J --> K[Selesai]
        </div>`;
    </script>
</body>
</html>
