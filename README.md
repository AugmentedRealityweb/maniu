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
        .menu-section {
            border: 2px solid #e63946;
            border-radius: 12px;
        }
        .menu-section h3 {
            color: #e63946;
            font-weight: bold;
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Navigation Bar -->
    <header class="bg-gradient-to-r from-red-400 to-yellow-500 shadow-md">
        <nav class="container mx-auto px-4 py-4 flex justify-between items-center text-white">
            <a href="#" class="text-2xl font-extrabold tracking-wider">Restaurant</a>
            <div class="hidden md:flex space-x-6">
                <a href="#menu" class="hover:underline">Menu</a>
                <a href="#about" class="hover:underline">About</a>
                <a href="#contact" class="hover:underline">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="bg-cover bg-center h-80 flex items-center justify-center text-white" style="background-image: url('https://tse4.mm.bing.net/th?id=OIP.qTEHRnCMgOKY87hkM95NygHaE6&pid=Api');">
        <div class="bg-black bg-opacity-60 p-6 rounded-lg text-center">
            <h1 class="text-4xl md:text-5xl font-extrabold">Discover Our Menu</h1>
            <p class="mt-2 text-lg md:text-xl">Explore a world of flavors and delicious experiences</p>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="container mx-auto px-4 py-10">
        <h2 class="text-3xl font-extrabold text-center text-gray-800 mb-8">Our Menu</h2>
        <div class="space-y-10">
            <!-- Main Course -->
            <div class="menu-section bg-white shadow-md p-4">
                <h3 class="text-xl mb-2">Fel Principal</h3>
                <div class="flex space-x-4">
                    <img src="https://tse4.mm.bing.net/th?id=OIP.mV26GuNqF_Rte3ynISEjsAHaE2&pid=Api" alt="Main Course" class="w-32 h-32 rounded-lg object-cover">
                    <div>
                        <h4 class="font-bold text-lg">Somon mediteranean cu orez</h4>
                        <p class="text-sm text-gray-600">Somon, capere, roșii cherry, lămâie, ulei de măsline...</p>
                        <p class="text-lg font-semibold text-red-500">75,00 Lei</p>
                    </div>
                </div>
            </div>

            <!-- Burgers -->
            <div class="menu-section bg-white shadow-md p-4">
                <h3 class="text-xl mb-2">Burgers</h3>
                <div class="flex space-x-4">
                    <img src="https://tse4.mm.bing.net/th?id=OIP.o77Uq83-UtGePE2GltXipwHaE7&pid=Api" alt="House Burger" class="w-32 h-32 rounded-lg object-cover">
                    <div>
                        <h4 class="font-bold text-lg">House Burger</h4>
                        <p class="text-sm text-gray-600">Chiflă de casă, carne de vită, ceapă la grătar...</p>
                        <p class="text-lg font-semibold text-red-500">59,00 Lei</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gradient-to-r from-gray-800 via-gray-900 to-black text-white py-8">
        <div class="container mx-auto px-4 text-center">
            <p class="text-lg">&copy; 2025 Restaurant. All rights reserved.</p>
            <div class="mt-4 flex justify-center space-x-4">
                <button class="bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded">Cere nota</button>
                <button class="bg-yellow-500 hover:bg-yellow-600 text-white py-2 px-4 rounded">Cheamă ospătarul</button>
            </div>
        </div>
    </footer>
</body>
</html>
