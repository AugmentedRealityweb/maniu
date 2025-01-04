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
                    <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Brunch">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Brunch</h5>
                        <ul class="list-unstyled">
                            <li><strong>Avocado Toast:</strong> Toast, avocado, cherry tomatoes, olive oil.</li>
                            <li><strong>Pancakes:</strong> Fluffy pancakes, maple syrup, fresh fruits.</li>
                            <li><strong>Egg Benedict:</strong> Poached eggs, hollandaise sauce, ham.</li>
                            <li><strong>Bagel & Cream Cheese:</strong> Fresh bagel, cream cheese, smoked salmon.</li>
                            <li><strong>Breakfast Bowl:</strong> Yogurt, granola, berries, honey.</li>
                        </ul>
                    </div>
                </div>
            </div>
            <!-- Gustari si Salate -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Gustari si Salate">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Gustari Si Salate</h5>
                        <ul class="list-unstyled">
                            <li><strong>Caesar Salad:</strong> Romaine lettuce, croutons, parmesan, caesar dressing.</li>
                            <li><strong>Greek Salad:</strong> Tomatoes, cucumbers, olives, feta cheese.</li>
                            <li><strong>Bruschetta:</strong> Grilled bread, tomatoes, garlic, basil.</li>
                            <li><strong>Caprese Salad:</strong> Mozzarella, tomatoes, basil, balsamic glaze.</li>
                            <li><strong>Stuffed Mushrooms:</strong> Mushrooms, cheese, breadcrumbs, herbs.</li>
                        </ul>
                    </div>
                </div>
            </div>
            <!-- Supe si Ciorbe -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Supe si Ciorbe">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Supe Si Ciorbe</h5>
                        <ul class="list-unstyled">
                            <li><strong>Chicken Soup:</strong> Chicken, vegetables, noodles.</li>
                            <li><strong>Minestrone:</strong> Mixed vegetables, pasta, tomato broth.</li>
                            <li><strong>Tomato Soup:</strong> Fresh tomatoes, cream, basil.</li>
                            <li><strong>Beef Broth:</strong> Beef, carrots, celery, parsley.</li>
                            <li><strong>Vegetable Cream Soup:</strong> Assorted vegetables, cream, croutons.</li>
                        </ul>
                    </div>
                </div>
            </div>
            <!-- Paste -->
            <div class="col-md-6 col-lg-4">
                <div class="card menu-card">
                    <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Paste">
                    <div class="card-body text-center">
                        <h5 class="card-title fw-bold">Paste</h5>
                        <ul class="list-unstyled">
                            <li><strong>Spaghetti Carbonara:</strong> Pasta, eggs, pancetta, parmesan.</li>
                            <li><strong>Fettuccine Alfredo:</strong> Pasta, cream, butter, parmesan.</li>
                            <li><strong>Lasagna:</strong> Layers of pasta, meat, ricotta, marinara sauce.</li>
                            <li><strong>Penne Arrabiata:</strong> Pasta, spicy tomato sauce, garlic.</li>
                            <li><strong>Pesto Pasta:</strong> Pasta, basil pesto, parmesan.</li>
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
