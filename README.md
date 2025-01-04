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
                        <button class="btn btn-danger mt-3" data-bs-toggle="collapse" data-bs-target="#brunchMenu">View</button>
                    </div>
                </div>
            </div>
            <!-- Brunch Items -->
            <div class="collapse mt-4" id="brunchMenu">
                <div class="list-group">
                    <a href="#brunchItem1" class="list-group-item list-group-item-action" data-bs-toggle="modal" data-bs-target="#brunchModal1">Avocado Toast</a>
                    <a href="#brunchItem2" class="list-group-item list-group-item-action" data-bs-toggle="modal" data-bs-target="#brunchModal2">Pancakes</a>
                    <a href="#brunchItem3" class="list-group-item list-group-item-action" data-bs-toggle="modal" data-bs-target="#brunchModal3">Egg Benedict</a>
                    <a href="#brunchItem4" class="list-group-item list-group-item-action" data-bs-toggle="modal" data-bs-target="#brunchModal4">Bagel & Cream Cheese</a>
                    <a href="#brunchItem5" class="list-group-item list-group-item-action" data-bs-toggle="modal" data-bs-target="#brunchModal5">Breakfast Bowl</a>
                </div>
            </div>

            <!-- Brunch Modals -->
            <div class="modal fade" id="brunchModal1" tabindex="-1">
                <div class="modal-dialog modal-dialog-centered">
                    <div class="modal-content">
                        <div class="modal-header">
                            <h5 class="modal-title">Avocado Toast</h5>
                            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
                        </div>
                        <div class="modal-body">
                            <img src="https://via.placeholder.com/300x200" class="img-fluid mb-3" alt="Avocado Toast">
                            <p>Toast, avocado, cherry tomatoes, olive oil.</p>
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="modal fade" id="brunchModal2" tabindex="-1">
                <div class="modal-dialog modal-dialog-centered">
                    <div class="modal-content">
                        <div class="modal-header">
                            <h5 class="modal-title">Pancakes</h5>
                            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
                        </div>
                        <div class="modal-body">
                            <img src="https://via.placeholder.com/300x200" class="img-fluid mb-3" alt="Pancakes">
                            <p>Fluffy pancakes, maple syrup, fresh fruits.</p>
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Repeat similar structure for other Brunch items and categories -->
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
