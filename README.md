<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta content="width=device-width, initial-scale=1.0" name="viewport">
    <title>Profil Pengguna</title>
    <link href="assets/vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">
    <link href="assets/vendor/bootstrap-icons/bootstrap-icons.css" rel="stylesheet">
    <link href="assets/css/style.css" rel="stylesheet">
</head>

<body>
    <header id="header" class="header fixed-top d-flex align-items-center">
        <div class="d-flex align-items-center justify-content-between">
            <a href="index.html" class="logo d-flex align-items-center"> 
                <span class="d-none d-lg-block">TUGAS UTS</span>
            </a>
            <i class="bi bi-list toggle-sidebar-btn" id="toggleSidebar"></i>
        </div>
        <nav class="header-nav ms-auto">
            <ul class="d-flex align-items-center">
                <li class="nav-item dropdown">
                    <a class="nav-link nav-profile d-flex align-items-center pe-0" href="#" data-bs-toggle="dropdown">
                        <img src="assets/img/profile-img.jpg" alt="Profile" class="rounded-circle">
                        <span class="d-none d-md-block dropdown-toggle ps-2">K. Anderson</span>
                    </a>
                    <ul class="dropdown-menu dropdown-menu-end dropdown-menu-arrow profile">
                        <li class="dropdown-header">
                            <h6>Muhamad Alfiansyah</h6>
                        </li>
                        <li><hr class="dropdown-divider"></li>
                        <li>
                            <a class="dropdown-item d-flex align-items-center" href="usersS-profile.html">
                                <i class="bi bi-person"></i>
                                <span>My Profile</span>
                            </a>
                        </li>
                        <li><hr class="dropdown-divider"></li>
                        <li>
                            <a class="dropdown-item d-flex align-items-center" href="pages-faq.html">
                                <i class="bi bi-question-circle"></i>
                                <span>Need Help?</span>
                            </a>
                        </li>
                        <li><hr class="dropdown-divider"></li>
                        <li>
                            <a class="dropdown-item d-flex align-items-center" href="#">
                                <i class="bi bi-box-arrow-right"></i>
                                <span>Sign Out</span>
                            </a>
                        </li>
                    </ul>
                </li>
            </ul>
        </nav>
    </header>

    <aside id="sidebar" class="sidebar">
        <ul class="sidebar-nav" id="sidebar-nav">
            <li class="nav-item">
                <a class="nav-link" href="index.html">
                    <i class="bi bi-grid"></i>
                    <span>Dashboard</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="data-karyawan.html">
                    <i class="bi bi-person-lines-fill"></i>
                    <span>Data Karyawan</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="jabatan.html">
                    <i class="bi bi-briefcase"></i>
                    <span>Jabatan</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="divisi.html">
                    <i class="bi bi-diagram-3"></i>
                    <span>Divisi</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="absensi.html">
                    <i class="bi bi-calendar-check"></i>
                    <span>Absensi</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="izin.html">
                    <i class="bi bi-calendar-minus"></i>
                    <span>Izin</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="lembur.html">
                    <i class="bi bi-clock-history"></i>
                    <span>Lembur</span>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="slip-gaji.html">
                    <i class="bi bi-receipt"></i>
                    <span>Slip Gaji</span>
                </a>
            </li>
        </ul>
    </aside>

    <main id="main" class="main">
        <div class="pagetitle">
            <h1>Profil Pengguna</h1>
        </div>

        <section class="section profile">
            <div class="card">
                <div class="card-body">
                    <h5 class="card-title">Informasi Akun</h5>
                    <div class="row mb-3">
                        <label for="inputName" class="col-sm-2 col-form-label">Nama</label>
                        <div class="col-sm-10">
                            <input type="text" class="form-control" id="inputName" value="Muhamad Alfiansyah" disabled>
                        </div>
                    </div>
                    <div class="row mb-3">
                        <label for="inputEmail" class="col-sm-2 col-form-label">Email</label>
                        <div class="col-sm-10">
                            <input type="email" class="form-control" id="inputEmail" value="Alfiansyah@example.com" disabled>
                        </div>
                    </div>
                    <div class="row mb-3">
                        <label for="inputPhone" class="col-sm-2 col-form-label">Nomor Telepon</label>
                        <div class="col-sm-10">
                            <input type="text" class="form-control" id="inputPhone" value="08123456789" disabled>
                        </div>
                    </div>
                    <div class="row mb-3">
                        <label for="inputPosition" class="col-sm-2 col-form-label">Jabatan</label>
                        <div class="col-sm-10">
                            <input type="text" class="form-control" id="inputPosition" value="Software Engineer" disabled>
                        </div>
                    </div>
                    <div class="row mb-3">
                        <label for="inputDepartment" class="col-sm-2 col-form-label">Divisi</label>
                        <div class="col-sm-10">
                            <input type="text" class="form-control" id="inputDepartment" value="IT Department" disabled>
                        </div>
                    </div>
                    <button class="btn btn-primary" onclick="toggleEdit()">Edit Profil</button>
                    <button class="btn btn-secondary" onclick="togglePassword()">Ubah Password</button>
                </div>
            </div>
        </section>

        <section class="section" id="passwordSection" style="display: none;">
            <div class="card">
                <div class="card-body">
                    <h5 class="card-title">Ubah Password</h5>
                    <form id="passwordForm">
                        <div class="row mb-3">
                            <label for="inputCurrentPassword" class="col-sm-4 col-form-label">Password Saat Ini</label>
                            <div class="col-sm-8">
                                <input type="password" class="form-control" id="inputCurrentPassword" required>
                            </div>
                        </div>
                        <div class="row mb-3">
                            <label for="inputNewPassword" class="col-sm-4 col-form-label">Password Baru</label>
                            <div class="col-sm-8">
                                <input type="password" class="form-control" id="inputNewPassword" required>
                            </div>
                        </div>
                        <div class="row mb-3">
                            <label for="inputConfirmPassword" class="col-sm-4 col-form-label">Konfirmasi Password</label>
                            <div class="col-sm-8">
                                <input type="password" class="form-control" id="inputConfirmPassword" required>
                            </div>
                        </div>
                        <button type="submit" class="btn btn-success">Ubah Password</button>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <footer class="footer">
        <div class="container">
            <span class="text-muted">© 2024 TUGAS UTS. All Rights Reserved.</span>
        </div>
    </footer>

    <script src="assets/vendor/bootstrap/js/bootstrap.bundle.min.js"></script>
    <script>
        // Function to toggle edit mode for the profile
        function toggleEdit() {
            const inputs = document.querySelectorAll('.form-control');
            inputs.forEach(input => {
                input.disabled = !input.disabled;
            });
            const button = document.querySelector('.btn-primary');
            button.textContent = button.textContent === 'Edit Profil' ? 'Simpan' : 'Edit Profil';
        }

        // Function to toggle password change section
        // function togglePassword()