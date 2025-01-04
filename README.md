<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Menu</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            scroll-behavior: smooth;
        }
        .menu-item {
            border: 1px solid #e63946;
            border-radius: 8px;
            padding: 16px;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        .menu-item h4 {
            color: #e63946;
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Header with Language Switch -->
    <header class="bg-gradient-to-r from-red-400 to-yellow-500 text-white py-4 shadow-md">
        <div class="container mx-auto px-4 flex justify-between items-center">
            <h1 class="text-2xl font-bold">Smart Menu</h1>
            <div class="flex space-x-4">
                <button class="bg-white text-red-500 font-bold py-1 px-3 rounded">RO</button>
                <button class="bg-white text-red-500 font-bold py-1 px-3 rounded">EN</button>
            </div>
        </div>
    </header>

    <!-- Main Menu Section -->
    <section class="container mx-auto px-4 py-8">
        <h2 class="text-3xl font-bold text-center text-gray-800 mb-8">Our Menu</h2>
        <div class="grid md:grid-cols-2 gap-6">
            <!-- Brunch -->
            <div class="menu-item">
                <h4 class="font-bold text-lg">Brunch</h4>
                <button class="bg-red-500 text-white py-1 px-3 rounded">View</button>
            </div>
            <!-- Gustari si Salate -->
            <div class="menu-item">
                <h4 class="font-bold text-lg">Gustari Si Salate</h4>
                <button class="bg-red-500 text-white py-1 px-3 rounded">View</button>
            </div>
            <!-- Supe si Ciorbe -->
            <div class="menu-item">
                <h4 class="font-bold text-lg">Supe Si Ciorbe</h4>
                <button class="bg-red-500 text-white py-1 px-3 rounded">View</button>
            </div>
            <!-- Paste -->
            <div class="menu-item">
                <h4 class="font-bold text-lg">Paste</h4>
                <button class="bg-red-500 text-white py-1 px-3 rounded">View</button>
            </div>
        </div>
    </section>

    <!-- Food Detail Section -->
    <section class="container mx-auto px-4 py-8 bg-white shadow-lg rounded-lg">
        <h2 class="text-2xl font-bold text-gray-800 mb-4">Burger de vita</h2>
        <div class="flex space-x-4">
            <img src="https://via.placeholder.com/150" alt="Burger de vita" class="rounded-lg">
            <div>
                <p class="text-gray-700">1 pastila carne vita (170 g), 1 chifla cu susan (86 g), 30 g ketchup, 50 g rosii...</p>
                <p class="text-lg font-bold text-red-500 mt-2">37,00 Lei</p>
            </div>
        </div>
        <div class="mt-6">
            <h3 class="font-bold text-lg">Informatii nutritionale</h3>
            <ul class="list-disc list-inside text-gray-600">
                <li>Valoare energetica: 1234 kcal</li>
                <li>Grasimi: 58 g</li>
                <li>Proteine: 58 g</li>
            </ul>
        </div>
    </section>

    <!-- Footer with Actions -->
    <footer class="bg-gradient-to-r from-gray-800 via-gray-900 to-black text-white py-6">
        <div class="container mx-auto text-center">
            <div class="flex justify-center space-x-6 mb-4">
                <button class="bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded">Cere nota</button>
                <button class="bg-yellow-500 hover:bg-yellow-600 text-white py-2 px-4 rounded">Cheama ospatarul</button>
            </div>
            <p>&copy; 2025 Smart Menu. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
