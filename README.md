<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator Items</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 10px;
            background-color: #ffe6f2; /* Pink pastel background */
            color: #ff1a75; /* Dark pink text */
        }

        h2 {
            color: #ff66b2; /* Darker pink for headings */
            font-size: 24px; /* Adjust font size */
            margin-bottom: 5px; /* Add margin for separation */
        }

        p {
            font-size: 12px; /* Smaller font size for description */
            color: #ff1a75; /* Dark pink text */
            margin-bottom: 10px; /* Add margin for separation */
        }

        form {
            background-color: #ffd9e6; /* Light pink form background */
            padding: 15px;
            border-radius: 10px;
            display: inline-block;
            margin-top: 10px;
        }

        label, select, button {
            margin: 5px;
            font-size: 14px; /* Adjust font size */
        }

        #result {
            margin-top: 10px;
            font-weight: bold;
        }

        .footer {
            font-size: 10px; /* Smaller font size for footer */
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h2>Calculator Items</h2>
    <p>This Calculator is run by <a href="https://x.com/PlatoNeeds" target="_blank">PlatoNeeds</a></p>
    
    <form id="calculatorForm">
        <label for="jenisItems">Jenis Items:</label>
        <select id="jenisItems" required>
            <option value="9">Items Shop</option>
            <option value="12">Items Rare</option>
        </select>

        <br> <!-- Spasi ke bawah -->

        <label for="hargaItems">Harga Items:</label>
        <select id="hargaItems" required>
            <!-- Opsi harga items -->
            <!-- Anda dapat menambahkan lebih banyak opsi sesuai kebutuhan -->
            <option value="50">50 coins</option>
            <option value="100">100 coins</option>
            <option value="150">150 coins</option>
            <option value="200">200 coins</option>
            <option value="250">250 coins</option>
            <option value="500">500 coins</option>
            <option value="750">750 coins</option>
            <option value="1000">1000 coins</option>
            <option value="1250">1250 coins</option>
            <option value="1500">1500 coins</option>
            <option value="1750">1750 coins</option>
            <option value="2000">2000 coins</option>
            <option value="2500">2500 coins</option>
            <option value="2750">2750 coins</option>
            <option value="3000">3000 coins</option>
            <option value="3500">3500 coins</option>
            <option value="4000">4000 coins</option>
            <option value="4500">4500 coins</option>
            <option value="5000">5000 coins</option>
            <option value="5500">5500 coins</option>
            <!-- Dan seterusnya sesuai kelipatan 500 hingga 10000 -->
            <option value="6000">6000 coins</option>
            <option value="6500">6500 coins</option>
            <option value="7000">7000 coins</option>
            <option value="7500">7500 coins</option>
            <option value="8000">8000 coins</option>
            <option value="8500">8500 coins</option>
            <option value="9000">9000 coins</option>
            <option value="9500">9500 coins</option>
            <option value="10000">10000 coins</option>
        </select>

        <br> <!-- Spasi ke bawah -->

        <button type="button" onclick="calculateTotal()">Hitung Total</button>
    </form>

    <div id="result"></div>

    <p>Kalkulator ini digunakan untuk memeriksa harga items Plato yang ingin customers beli. Jika ingin mengecek nama dan harga items lebih detail, bisa cek melalui web <a href="https://platopedia.com/items" target="_blank">platopedia.com/items</a> lalu jumlahkan di web ini.</p>

    <br> <!-- Spasi ke bawah -->

    <p class="footer">Last Update: 24/02/2024 | <a href="https://x.com/PlatoNeeds" target="_blank">@PlatoNeeds</a></p>

    <script>
        // Fungsi untuk menghitung total dan menampilkan hasil
        function calculateTotal() {
            var jenisItems = parseInt(document.getElementById("jenisItems").value);
            var hargaItems = parseInt(document.getElementById("hargaItems").value);
            var totalHarga;

            // Menggunakan rumus sesuai dengan jenis items yang dipilih
            if (jenisItems === 9) {
                totalHarga = jenisItems * hargaItems;
            } else if (jenisItems === 12) {
                totalHarga = hargaItems < 5001 ? 12 * hargaItems : 11 * hargaItems;
            }

            // Tampilkan hasil
            var resultDiv = document.getElementById("result");
            resultDiv.textContent = `Total Harga: Rp${totalHarga.toLocaleString()}`;
        }
    </script>
</body>
</html>
