# bpr201internettabanliprogramlama_zeynepozsaglam
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BABYROO  </title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

        <style>
        /* --- 1. PEMBE TEMA VE GÜZELLEŞTİRMELER --- */
        :root {
            --pembe-ana: #EC407A;
            --pembe-acik: #FFB6C1; 
            --krem-arkaplan: #FFF0F5; 
            --yazi-koyu: #333333;
        }

        body {
            background-color: var(--krem-arkaplan);
            color: var(--yazi-koyu);
        }

        /* Navbar (Üst Menü) */
        .navbar {
            background-color: var(--pembe-ana) !important;
        }

        .navbar-brand, .nav-link {
            color: white !important;
            font-weight: bold;
        }

        .navbar-brand:hover, .nav-link:hover {
            color: var(--pembe-acik) !important;
        }

        /* Ana Buton Stili  */
        .btn-pembe-ana {
            background-color: var(--pembe-ana);
            border-color: var(--pembe-ana);
            color: white;
            transition: background-color 0.3s ease;
        }

        .btn-pembe-ana:hover {
            background-color: #D81B60; 
            border-color: #D81B60;
        }

        /* Ürün Kartları */
        .card {
            border: 1px solid var(--pembe-acik);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }

        .card-img-top {
            height: 200px;
            object-fit: cover;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
        }
        
        .urun-fiyati {
            color: var(--pembe-ana);
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        /* Üye Giriş Alanı  */
        .login-card {
            max-width: 400px;
            margin: 50px auto;
            padding: 30px;
            border: 1px solid var(--pembe-acik);
            border-radius: 15px;
            background-color: white;
            box-shadow: 0 0 15px rgba(236, 64, 122, 0.1);
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg sticky-top">
        <div class="container-fluid container-lg">
            <a class="navbar-brand" href="#">
                <i class="fas fa-baby"></i> BABYROO
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Ana Sayfa</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Giyim</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Oyuncaklar</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Oda & Aksesuar</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#uye-giris">
                            <i class="fas fa-user"></i> Üye Girişi
                        </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#sepet">
                            <i class="fas fa-shopping-bag"></i> Sepet (0)
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container my-5">
        
        <header class="text-center mb-5 p-4 rounded" style="background-color: white; border: 1px solid var(--pembe-acik);">
            <h1 class="display-4" style="color: var(--pembe-ana);">Yeni Sezon Ürünleri</h1>
            <p class="lead">En tatlı ve en güvenli ürünler şimdi pembe dokunuşlarla!</p>
        </header>

        <h2 class="mb-4">Öne Çıkan Aktüel Ürünler</h2>
        <div class="row g-4 mb-5">
            
            <div class="col-lg-3 col-md-6">
                <div class="card h-100">
                    <img src="pembebulutoyuncak.jpg" class="card-img-top" alt="Ürün Resmi">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title">Pembe Bulut Oyuncak</h5>
                        <p class="card-text flex-grow-1">Yumuşak dokulu, güvenli ve eğitici oyuncak.</p>
                        <p class="urun-fiyati">499.99 TL</p>
                        
                        <button class="btn btn-pembe-ana mt-2" data-bs-toggle="modal" data-bs-target="#sepetModal">
                            <i class="fas fa-shopping-cart me-2"></i> Sepete Ekle
                        </button>
                    </div>
                </div>
            </div>

            <div class="col-lg-3 col-md-6">
                <div class="card h-100">
                    <img src="organikpembetulum.jpg" class="card-img-top" alt="Ürün Resmi">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title">Organik Pembe Tulum</h5>
                        <p class="card-text flex-grow-1">%100 organik pamuktan üretilmiştir. Hassas ciltler için.</p>
                        <p class="urun-fiyati">799.99 TL</p>
                        <button class="btn btn-pembe-ana mt-2">
                            <i class="fas fa-shopping-cart me-2"></i> Sepete Ekle
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="col-lg-3 col-md-6">
                <div class="card h-100">
                    <img src="stitchveliloluçifttaraflınevresimtakımı.jpg" class="card-img-top" alt="Ürün Resmi">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title">Lilo ve Stitch Çift Taraflı Uyku Seti</h5>
                        <p class="card-text flex-grow-1">Bebeğinizin odasına şıklık katacak set.</p>
                        <p class="urun-fiyati">1099.99 TL</p>
                        <button class="btn btn-pembe-ana mt-2">
                            <i class="fas fa-shopping-cart me-2"></i> Sepete Ekle
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="col-lg-3 col-md-6">
                <div class="card h-100">
                    <img src="çocukkitapseti.jpg" class="card-img-top" alt="Ürün Resmi">
                    <div class="card-body d-flex flex-column">
                        <h5 class="card-title">Çocuk Kitap Seti</h5>
                        <p class="card-text flex-grow-1">Partiler ve özel günler için harika aksesuarlar.</p>
                        <p class="urun-fiyati">299.99 TL</p>
                        <button class="btn btn-pembe-ana mt-2">
                            <i class="fas fa-shopping-cart me-2"></i> Sepete Ekle
                        </button>
                    </div>
                </div>
            </div>
        </div>
        
        <section id="uye-giris" class="mb-5">
            <h2 class="text-center mb-4" style="color: var(--pembe-ana);">Hesabınıza Giriş Yapın</h2>
            <div class="login-card">
                <form>
                    <div class="mb-3">
                        <label for="email" class="form-label">E-posta Adresiniz</label>
                        <input type="email" class="form-control" id="email" required>
                    </div>
                    <div class="mb-3">
                        <label for="password" class="form-label">Şifreniz</label>
                        <input type="password" class="form-control" id="password" required>
                    </div>
                    <div class="mb-3 form-check">
                        <input type="checkbox" class="form-check-input" id="remember">
                        <label class="form-check-label" for="remember">Beni Hatırla</label>
                    </div>
                    <button type="submit" class="btn btn-pembe-ana w-100">Giriş Yap</button>
                </form>
                <div class="mt-3 text-center small">
                    <a href="#" class="text-decoration-none" style="color: var(--pembe-ana);">Şifremi Unuttum</a> | 
                    <a href="#" class="text-decoration-none" style="color: var(--pembe-ana);">Yeni Üye Ol</a>
                </div>
            </div>
        </section>

    </div>
    <div class="modal fade" id="sepetModal" tabindex="-1" aria-labelledby="sepetModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header" style="background-color: var(--pembe-ana); color: white;">
                    <h5 class="modal-title" id="sepetModalLabel"><i class="fas fa-shopping-cart"></i> Sepetim</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <p>Ürün sepetinize eklendi. (Bu sadece bir göstermeliktir, gerçek sepet işlemleri için JS/Backend gereklidir.)</p>
                    <table class="table table-hover">
                        <thead>
                            <tr>
                                <th>Ürün</th>
                                <th>Adet</th>
                                <th>Fiyat</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Pembe Bulut Oyuncak</td>
                                <td>1</td>
                                <td>299.99TL</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
               
            </div>
        </div>
    </div>

    <footer class="bg-white mt-5 border-top pt-4 pb-3">
        <div class="container text-center text-muted small">
            <p>&copy; 2024 Minik Prenses. Tüm Hakları Saklıdır. Pembe Temalı E-Ticaret Şablonu.</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
