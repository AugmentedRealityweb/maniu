<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Restaurant Menu</title>
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css"
    rel="stylesheet"
  />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css"
  />
  <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"
  ></script>
  <style>
    body {
      scroll-behavior: smooth;
      background-color: #f8f9fa;
    }

    .menu-header {
      background: linear-gradient(
        90deg,
        rgba(255, 94, 87, 1) 0%,
        rgba(255, 195, 113, 1) 100%
      );
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
      <!-- Brunch Category Card -->
      <div class="col-md-6 col-lg-4">
        <div class="card menu-card text-center">
          <img
            src="https://via.placeholder.com/300x200"
            class="card-img-top"
            alt="Brunch Category"
          />
          <div class="card-body">
            <h5 class="card-title fw-bold">Brunch</h5>
            <button
              class="btn btn-danger mt-3"
              data-bs-toggle="collapse"
              data-bs-target="#brunchMenu"
            >
              View
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Collapsible Brunch Items (Name + Image) -->
    <div class="collapse mt-4" id="brunchMenu">
      <div class="row g-3">
        <!-- Item 1 -->
        <div class="col-sm-6 col-md-4 col-lg-3">
          <div
            class="card h-100"
            data-bs-toggle="modal"
            data-bs-target="#brunchModal1"
            style="cursor: pointer;"
          >
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="Avocado Toast"
            />
            <div class="card-body text-center">
              <h6 class="card-title mb-0">Avocado Toast</h6>
            </div>
          </div>
        </div>

        <!-- Item 2 -->
        <div class="col-sm-6 col-md-4 col-lg-3">
          <div
            class="card h-100"
            data-bs-toggle="modal"
            data-bs-target="#brunchModal2"
            style="cursor: pointer;"
          >
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="Pancakes"
            />
            <div class="card-body text-center">
              <h6 class="card-title mb-0">Pancakes</h6>
            </div>
          </div>
        </div>

        <!-- Item 3 -->
        <div class="col-sm-6 col-md-4 col-lg-3">
          <div
            class="card h-100"
            data-bs-toggle="modal"
            data-bs-target="#brunchModal3"
            style="cursor: pointer;"
          >
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="Egg Benedict"
            />
            <div class="card-body text-center">
              <h6 class="card-title mb-0">Egg Benedict</h6>
            </div>
          </div>
        </div>

        <!-- Item 4 -->
        <div class="col-sm-6 col-md-4 col-lg-3">
          <div
            class="card h-100"
            data-bs-toggle="modal"
            data-bs-target="#brunchModal4"
            style="cursor: pointer;"
          >
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="Bagel & Cream Cheese"
            />
            <div class="card-body text-center">
              <h6 class="card-title mb-0">Bagel & Cream Cheese</h6>
            </div>
          </div>
        </div>

        <!-- Item 5 -->
        <div class="col-sm-6 col-md-4 col-lg-3">
          <div
            class="card h-100"
            data-bs-toggle="modal"
            data-bs-target="#brunchModal5"
            style="cursor: pointer;"
          >
            <img
              src="https://via.placeholder.com/300x200"
              class="card-img-top"
              alt="Breakfast Bowl"
            />
            <div class="card-body text-center">
              <h6 class="card-title mb-0">Breakfast Bowl</h6>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Modals Brunch Items: Poza, Descriere, Ingrediente -->
    <!-- Modal 1 -->
    <div
      class="modal fade"
      id="brunchModal1"
      tabindex="-1"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Avocado Toast</h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <img
              src="https://via.placeholder.com/300x200"
              class="img-fluid mb-3"
              alt="Avocado Toast"
            />
            <p><strong>Descriere:</strong> Toast crocant cu pastă de avocado, topping de roșii cherry și un strop de ulei de măsline.</p>
            <p><strong>Ingrediente:</strong> pâine, avocado, roșii cherry, ulei de măsline, sare, piper.</p>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-bs-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Modal 2 -->
    <div
      class="modal fade"
      id="brunchModal2"
      tabindex="-1"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Pancakes</h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <img
              src="https://via.placeholder.com/300x200"
              class="img-fluid mb-3"
              alt="Pancakes"
            />
            <p><strong>Descriere:</strong> Clătite pufoase servite cu sirop de arțar și fructe de sezon.</p>
            <p><strong>Ingrediente:</strong> făină, ouă, lapte, zahăr, sirop de arțar, fructe.</p>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-bs-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Modal 3 -->
    <div
      class="modal fade"
      id="brunchModal3"
      tabindex="-1"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Egg Benedict</h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <img
              src="https://via.placeholder.com/300x200"
              class="img-fluid mb-3"
              alt="Egg Benedict"
            />
            <p><strong>Descriere:</strong> Ou poșat servit pe un english muffin, cu șuncă și sos Hollandaise cremos.</p>
            <p><strong>Ingrediente:</strong> ouă, bacon sau șuncă, muffin englezesc, sos Hollandaise.</p>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-bs-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Modal 4 -->
    <div
      class="modal fade"
      id="brunchModal4"
      tabindex="-1"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Bagel &amp; Cream Cheese</h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <img
              src="https://via.placeholder.com/300x200"
              class="img-fluid mb-3"
              alt="Bagel & Cream Cheese"
            />
            <p><strong>Descriere:</strong> Bagel proaspăt copt, uns cu cremă de brânză și opțional somon afumat.</p>
            <p><strong>Ingrediente:</strong> bagel, cremă de brânză, somon (opțional), ceapă roșie, capere.</p>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-bs-dismiss="modal"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Modal 5 -->
    <div
      class="modal fade"
      id="brunchModal5"
      tabindex="-1"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Breakfast Bowl</h5>
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body">
            <img
              src="https://via.placeholder.com/300x200"
              class="img-fluid mb-3"
              alt="Breakfast Bowl"
            />
            <p><strong>Descriere:</strong> Bol consistent cu ouă, legume proaspete și semințe, perfect pentru un început de zi sănătos.</p>
            <p><strong>Ingrediente:</strong> ouă, salată verde, roșii, avocado, semințe de dovleac, dressing.</p>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-bs-dismiss="modal"
            >
              Close
            </button>
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
        <button class="btn btn-warning">Cheamă ospătarul</button>
      </div>
      <p class="mb-0">&copy; 2025 Smart Menu. All rights reserved.</p>
    </div>
  </footer>
</body>
</html>
