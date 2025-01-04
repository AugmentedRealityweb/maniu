<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Menu</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
    <style>
        body {
            scroll-behavior: smooth;
            background-color: #f8f9fa;
        }
        .menu-header {
            background: linear-gradient(90deg, rgba(255,94,87,1) 0%, rgba(255,195,113,1) 100%);
            color: white;
        }
        .menu-card {
            border: none;
            border-radius: 12px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .menu-card:hover {
            transform: scale(1.05);
        }
        .menu-footer {
            background: #343a40;
            color: white;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="menu-header py-4">
        <div class="container d-flex justify-content-between align-items-center">
            <h1 class="fw-bold">Smart Menu</h1>
            <div>
                <button class="btn btn-light fw-bold me-2">RO</button>
                <button class="btn btn-light fw-bold">EN</button>
            </div>
        </div>
    </header>

    <!-- Menu Section -->
    <section class="container my-5">
        <h2 class="text-center fw-bold mb-4">Our Menu</h2>
        <div class="row g-4">
            <!-- Brunch -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Brunch</h5>
                        <button class="btn btn-danger mt-3">View</button>
                    </div>
                </div>
            </div>
            <!-- Gustari si Salate -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Gustari Si Salate</h5>
                        <button class="btn btn-danger mt-3">View</button>
                    </div>
                </div>
            </div>
            <!-- Supe si Ciorbe -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Supe Si Ciorbe</h5>
                        <button class="btn btn-danger mt-3">View</button>
                    </div>
                </div>
            </div>
            <!-- Paste -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Paste</h5>
                        <button class="btn btn-danger mt-3">View</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Food Detail Section -->
    <section class="container my-5">
        <div class="card menu-card">
            <div class="row g-0">
                <div class="col-md-4">
                    <img src="https://via.placeholder.com/300" class="img-fluid rounded-start" alt="Burger de vita">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title fw-bold">Burger de vita</h5>
                        <p class="card-text">1 pastila carne vita (170 g), 1 chifla cu susan (86 g), 30 g ketchup...</p>
                        <p class="card-text text-danger fw-bold">37,00 Lei</p>
                        <h6 class="fw-bold">Informatii nutritionale:</h6>
                        <ul>
                            <li>Valoare energetica: 1234 kcal</li>
                            <li>Grasimi: 58 g</li>
                            <li>Proteine: 58 g</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="menu-footer py-4">
        <div class="container text-center">
            <div class="mb-3">
                <button class="btn btn-danger me-2">Cere nota</button>
                <button class="btn btn-warning">Cheama ospatarul</button>
            </div>
            <p class="mb-0">&copy; 2025 Smart Menu. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
