<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LINK VIPZEXNET</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2980b9;
            --light-bg: #f8f9fa;
            --dark-bg: #1a1a2e;
            --light-text: #f8f9fa;
            --dark-text: #2c3e50;
            --card-light: #ffffff;
            --card-dark: #2d2d44;
            --gradient: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
        }

        body {
            font-family: 'Vazir', sans-serif;
            background-color: var(--light-bg);
            color: var(--dark-text);
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }

        .login-container {
            max-width: 400px;
            margin: 100px auto;
            padding: 25px;
            border-radius: 15px;
            background-color: white;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .chat-background {
            background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), 
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="50%" y="50%" font-family="Arial" font-size="12" fill="%233498db" text-anchor="middle" dominant-baseline="middle">یک دنیای متفاوت از لینک‌ها\nLINK VIPZEXNET</text></svg>');
            background-size: 300px;
            background-attachment: fixed;
            min-height: 100vh;
        }

        .navbar {
            background: var(--gradient);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .card {
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border: none;
            margin-bottom: 20px;
        }

        .card-header {
            border-radius: 12px 12px 0 0 !important;
            background: var(--gradient);
            color: white;
        }

        .btn-primary {
            background: var(--gradient);
            border: none;
        }

        .btn-primary:hover {
            background: linear-gradient(135deg, var(--secondary-color) 0%, var(--primary-color) 100%);
        }

        .banner-card {
            transition: transform 0.3s;
            border-radius: 12px;
            overflow: hidden;
            cursor: pointer;
        }

        .banner-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .banner-image {
            height: 160px;
            object-fit: cover;
        }

        .message {
            padding: 12px 15px;
            margin: 8px 0;
            border-radius: 18px;
            max-width: 80%;
            position: relative;
        }

        .user-message {
            background-color: #e3f2fd;
            margin-left: auto;
        }

        .admin-message {
            background-color: #fce4ec;
            margin-right: auto;
        }

        .chat-container {
            height: 400px;
            overflow-y: auto;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 15px;
            background-color: rgba(255, 255, 255, 0.8);
        }

        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            object-fit: cover;
        }

        .profile-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary-color);
        }

        .notification-badge {
            position: absolute;
            top: -5px;
            right: -5px;
            background-color: #e74c3c;
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18px;
            font-size: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .verified-badge {
            color: #3498db;
            font-size: 16px;
        }

        .online-status {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: #2ecc71;
            position: absolute;
            bottom: 0;
            right: 0;
            border: 2px solid white;
        }

        .typing-animation {
            overflow: hidden;
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: .15em;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
            text-align: center;
            margin-bottom: 30px;
            color: #3498db;
            font-weight: bold;
            font-size: 1.5rem;
        }

        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #3498db; }
        }

        .banner-status {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10;
        }
        
        .status-blue {
            background-color: #3498db;
            border: 2px solid white;
            color: white;
        }
        
        .status-yellow {
            background-color: #f39c12;
            border: 2px solid white;
            color: white;
        }

        .category-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            z-index: 10;
        }

        .banner-description {
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-top: 8px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .banner-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 10px;
            font-size: 0.85rem;
        }

        .form-control, .form-select {
            border-radius: 10px;
            padding: 12px 15px;
        }

        .form-control:focus, .form-select:focus {
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
            border-color: #3498db;
        }

        .nav-tabs .nav-link {
            border-radius: 10px 10px 0 0;
        }

        .support-link {
            color: #3498db;
            text-decoration: none;
        }

        .support-link:hover {
            text-decoration: underline;
        }
        
        .modal-banner-img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 15px;
        }
    </style>
</head>
<body class="chat-background">
    <!-- صفحه ورود -->
    <div id="login-page">
        <div class="login-container">
            <div class="text-center mb-4">
                <h3 class="typing-animation">یک دنیای متفاوت از لینک‌ها<br>LINK VIPZEXNET</h3>
            </div>
            <ul class="nav nav-tabs mb-3" id="loginTabs" role="tablist">
                <li class="nav-item" role="presentation">
                    <button class="nav-link active" id="login-tab" data-bs-toggle="tab" data-bs-target="#login" type="button" role="tab">ورود</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="register-tab" data-bs-toggle="tab" data-bs-target="#register" type="button" role="tab">ثبت نام</button>
                </li>
            </ul>
            <div class="tab-content" id="loginTabContent">
                <div class="tab-pane fade show active" id="login" role="tabpanel">
                    <form id="login-form">
                        <div class="mb-3">
                            <label for="login-username" class="form-label">نام کاربری</label>
                            <input type="text" class="form-control" id="login-username" required>
                        </div>
                        <div class="mb-3">
                            <label for="login-password" class="form-label">رمز عبور</label>
                            <input type="password" class="form-control" id="login-password" required>
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="remember-login">
                            <label class="form-check-label" for="remember-login">مرا به خاطر بسپار</label>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">ورود</button>
                    </form>
                </div>
                <div class="tab-pane fade" id="register" role="tabpanel">
                    <form id="register-form">
                        <div class="mb-3">
                            <label for="register-username" class="form-label">نام کاربری</label>
                            <input type="text" class="form-control" id="register-username" required>
                        </div>
                        <div class="mb-3">
                            <label for="register-email" class="form-label">ایمیل</label>
                            <input type="email" class="form-control" id="register-email" required>
                        </div>
                        <div class="mb-3">
                            <label for="register-password" class="form-label">رمز عبور</label>
                            <input type="password" class="form-control" id="register-password" required>
                        </div>
                        <div class="mb-3">
                            <label for="register-confirm-password" class="form-label">تکرار رمز عبور</label>
                            <input type="password" class="form-control" id="register-confirm-password" required>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">ثبت نام</button>
                    </form>
                </div>
            </div>
            <div class="text-center mt-3">
                <p>پشتیبانی: 
                    <a href="https://rubika.ir/Mahdi_shami89" target="_blank" class="support-link">@Mahdi_shami89</a>
                </p>
            </div>
        </div>
    </div>

    <!-- نوار ناوبری -->
    <nav class="navbar navbar-expand-lg navbar-dark" style="display: none;" id="main-navbar">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="bi bi-link-45deg"></i> LINK VIPZEXNET
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="#" onclick="showPage('home')">
                            <i class="bi bi-house"></i> صفحه اصلی
                        </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showPage('banner-register')">
                            <i class="bi bi-plus-square"></i> ثبت بنر
                        </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showPage('chat-room')">
                            <i class="bi bi-chat-dots"></i> چت روم
                            <span class="notification-badge" id="chat-notification">0</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showPage('message-inbox')">
                            <i class="bi bi-inbox"></i> صندوق پیام
                            <span class="notification-badge" id="message-notification">0</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" onclick="showPage('profile')">
                            <i class="bi bi-person"></i> پروفایل
                        </a>
                    </li>
                </ul>
                <div class="d-flex">
                    <div id="admin-nav-item">
                        <button class="btn btn-outline-light me-2" onclick="showPage('admin-login')">
                            <i class="bi bi-shield-lock"></i> ورود ادمین
                        </button>
                    </div>
                    <button class="btn btn-outline-light" onclick="logout()">
                        <i class="bi bi-box-arrow-right"></i> خروج
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <div class="container mt-4" id="main-container" style="display: none;">
        <!-- صفحه اصلی -->
        <div id="home-page" class="page">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-house"></i> صفحه اصلی</h5>
                </div>
                <div class="card-body">
                    <div class="d-flex justify-content-between align-items-center mb-3">
                        <h4>بنرهای کاربران</h4>
                        <div class="d-flex">
                            <button class="btn btn-outline-primary me-2" onclick="sortBanners('newest')">
                                <i class="bi bi-sort-down"></i> جدیدترین
                            </button>
                            <button class="btn btn-outline-primary" onclick="sortBanners('popular')">
                                <i class="bi bi-hand-thumbs-up"></i> محبوب‌ترین
                            </button>
                        </div>
                    </div>
                    
                    <div id="banners-container" class="row">
                        <!-- بنرها اینجا نمایش داده می شوند -->
                    </div>
                </div>
            </div>
        </div>

        <!-- صفحه ثبت بنر -->
        <div id="banner-register-page" class="page" style="display: none;">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-plus-square"></i> ثبت بنر جدید</h5>
                </div>
                <div class="card-body">
                    <form id="banner-form">
                        <div class="row">
                            <div class="col-md-8">
                                <div class="mb-3">
                                    <label for="banner-title" class="form-label">عنوان بنر *</label>
                                    <input type="text" class="form-control" id="banner-title" placeholder="عنوان بنر را وارد کنید" required>
                                </div>
                                
                                <div class="mb-3">
                                    <label for="banner-description" class="form-label">توضیحات</label>
                                    <textarea class="form-control" id="banner-description" rows="3" placeholder="توضیحات مربوط به بنر را وارد کنید"></textarea>
                                </div>
                                
                                <div class="mb-3">
                                    <label for="banner-url" class="form-label">لینک بنر</label>
                                    <input type="url" class="form-control" id="banner-url" placeholder="https://example.com">
                                </div>
                                
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label for="banner-category" class="form-label">دسته‌بندی</label>
                                            <select class="form-select" id="banner-category">
                                                <option value="عمومی">عمومی</option>
                                                <option value="فروشگاه">فروشگاه</option>
                                                <option value="خدمات">خدمات</option>
                                                <option value="آموزشی">آموزشی</option>
                                                <option value="سرگرمی">سرگرمی</option>
                                            </select>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label for="banner-tags" class="form-label">تگ‌ها (با کاما جدا کنید)</label>
                                            <input type="text" class="form-control" id="banner-tags" placeholder="تگ۱, تگ۲, تگ۳">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="col-md-4">
                                <div class="mb-3">
                                    <label for="banner-image-upload" class="form-label">تصویر بنر *</label>
                                    <div class="border rounded p-3 text-center">
                                        <i class="bi bi-cloud-upload display-4 text-muted"></i>
                                        <p class="mb-0 mt-2">برای آپلود کلیک کنید</p>
                                        <small class="text-muted">فرمت‌های مجاز: JPG, PNG</small>
                                        <input type="file" id="banner-image-upload" class="d-none" accept="image/*" required>
                                        <button type="button" class="btn btn-sm btn-outline-primary mt-2" onclick="document.getElementById('banner-image-upload').click()">
                                            انتخاب تصویر
                                        </button>
                                    </div>
                                    <div id="banner-image-preview" class="mt-3 text-center" style="display: none;">
                                        <img id="banner-preview" class="img-fluid rounded" style="max-height: 200px;">
                                        <button type="button" class="btn btn-sm btn-danger mt-2" onclick="removeBannerImage()">
                                            <i class="bi bi-trash"></i> حذف تصویر
                                        </button>
                                    </div>
                                </div>
                                
                                <div class="mb-3 form-check">
                                    <input type="checkbox" class="form-check-input" id="banner-terms" required>
                                    <label class="form-check-label" for="banner-terms">با شرایط و قوانین موافقم</label>
                                </div>
                                
                                <button type="submit" class="btn btn-primary w-100">
                                    <i class="bi bi-check-circle"></i> ثبت بنر
                                </button>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>

        <!-- صفحه چت روم -->
        <div id="chat-room-page" class="page" style="display: none;">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-chat-dots"></i> چت روم کاربران</h5>
                </div>
                <div class="card-body">
                    <div id="admin-indicator" class="alert alert-info" style="display: none;">
                        <i class="bi bi-patch-check-fill"></i>
                        <span>شما به عنوان ادمین در حال چت هستید</span>
                    </div>
                    <div class="row">
                        <div class="col-md-4">
                            <h6>کاربران آنلاین</h6>
                            <div class="user-list">
                                <div id="admin-user-item" class="d-flex align-items-center p-2 mb-2 rounded" onclick="selectUser('admin')" style="display: none; background: #f8f9fa;">
                                    <div class="position-relative">
                                        <img src="https://ui-avatars.com/api/?name=ادمین&background=3498db&color=fff" class="user-avatar">
                                        <span class="online-status"></span>
                                    </div>
                                    <div class="me-2">
                                        <div>مدیر سیستم <i class="bi bi-patch-check-fill verified-badge"></i></div>
                                        <small class="text-muted">آنلاین</small>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-8">
                            <div id="chat-with" class="p-2 mb-3 rounded text-center" style="background: #f8f9fa;">
                                <small>با <strong id="selected-user">همه کاربران</strong> در حال گفتگو هستید</small>
                            </div>
                            <div id="chat-messages" class="chat-container">
                                <!-- پیام های چت در اینجا نمایش داده می شوند -->
                            </div>
                            <div class="input-group mt-2">
                                <input type="text" id="chat-input" class="form-control" placeholder="پیام خود را بنویسید...">
                                <button class="btn btn-primary" onclick="sendMessage()">
                                    <i class="bi bi-send"></i> ارسال
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- صفحه صندوق پیام -->
        <div id="message-inbox-page" class="page" style="display: none;">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-inbox"></i> صندوق پیام ها</h5>
                </div>
                <div class="card-body">
                    <div class="d-flex mb-3">
                        <button class="btn btn-outline-primary me-2 active">همه</button>
                        <button class="btn btn-outline-primary me-2">خوانده نشده</button>
                        <button class="btn btn-outline-primary">مهم</button>
                    </div>
                    <div id="messages-container">
                        <!-- پیام ها اینجا نمایش داده می شوند -->
                    </div>
                </div>
            </div>
        </div>

        <!-- صفحه پروفایل -->
        <div id="profile-page" class="page" style="display: none;">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-person"></i> پروفایل کاربری</h5>
                </div>
                <div class="card-body">
                    <div id="profile-view">
                        <div class="row">
                            <div class="col-md-4 text-center">
                                <img src="https://ui-avatars.com/api/?name=کاربر+لینکدونی&size=100&background=3498db&color=fff" class="profile-avatar mb-3" id="profile-avatar">
                                <h4 id="profile-name">کاربر لینکدونی</h4>
                                <p class="text-muted" id="profile-join-date">عضو since 1402</p>
                                <div class="d-grid gap-2">
                                    <button class="btn btn-outline-primary" onclick="toggleEditProfile()">
                                        <i class="bi bi-pencil"></i> ویرایش پروفایل
                                    </button>
                                </div>
                            </div>
                            <div class="col-md-8">
                                <div class="row mb-3">
                                    <div class="col-md-6">
                                        <div class="card bg-light">
                                            <div class="card-body text-center">
                                                <h6>بنرهای ثبت شده</h6>
                                                <h3 id="profile-banners-count">0</h3>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="card bg-light">
                                            <div class="card-body text-center">
                                                <h6>پیام های ارسال شده</h6>
                                                <h3 id="profile-messages-count">0</h3>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                
                                <h5>اطلاعات کاربری</h5>
                                <table class="table">
                                    <tr>
                                        <th>نام کاربری:</th>
                                        <td id="profile-username">user123</td>
                                    </tr>
                                    <tr>
                                        <th>ایمیل:</th>
                                        <td id="profile-email">user@linkoni.ir</td>
                                    </tr>
                                    <tr>
                                        <th>تاریخ عضویت:</th>
                                        <td id="profile-join-date">1402/05/01</td>
                                    </tr>
                                </table>
                                
                                <h5>آخرین فعالیت‌ها</h5>
                                <div id="user-activities">
                                    <div class="text-center py-4 text-muted">
                                        <i class="bi bi-clock-history display-4"></i>
                                        <p>هیچ فعالیتی ثبت نشده است</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div id="profile-edit-form" class="profile-edit-form mt-4" style="display: none;">
                        <h5>ویرایش پروفایل</h5>
                        <form id="edit-profile-form">
                            <div class="row">
                                <div class="col-md-6">
                                    <div class="mb-3">
                                        <label for="edit-username" class="form-label">نام کاربری</label>
                                        <input type="text" class="form-control" id="edit-username" value="user123" readonly>
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="mb-3">
                                        <label for="edit-email" class="form-label">ایمیل</label>
                                        <input type="email" class="form-control" id="edit-email" value="user@linkoni.ir">
                                    </div>
                                </div>
                            </div>
                            <div class="mb-3">
                                <label for="avatar-upload" class="form-label">تصویر پروفایل</label>
                                <input type="file" class="form-control" id="avatar-upload" accept="image/*">
                            </div>
                            <div class="mb-3">
                                <label for="edit-bio" class="form-label">بیوگرافی</label>
                                <textarea class="form-control" id="edit-bio" rows="3">من یک کاربر فعال در لینکدونی هستم</textarea>
                            </div>
                            <button type="submit" class="btn btn-primary">ذخیره تغییرات</button>
                            <button type="button" class="btn btn-secondary" onclick="toggleEditProfile()">انصراف</button>
                        </form>
                    </div>
                </div>
            </div>
        </div>

        <!-- صفحه ورود ادمین -->
        <div id="admin-login-page" class="page" style="display: none;">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-shield-lock"></i> ورود ادمین</h5>
                </div>
                <div class="card-body">
                    <form id="admin-login-form">
                        <div class="mb-3">
                            <label for="admin-username" class="form-label">نام کاربری</label>
                            <input type="text" class="form-control" id="admin-username" required>
                        </div>
                        <div class="mb-3">
                            <label for="admin-password" class="form-label">رمز عبور</label>
                            <input type="password" class="form-control" id="admin-password" required>
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="remember-me">
                            <label class="form-check-label" for="remember-me">مرا به خاطر بسپار</label>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">ورود</button>
                    </form>
                </div>
            </div>
        </div>

        <!-- پنل ادمین -->
        <div id="admin-panel-page" class="page" style="display: none;">
            <div class="card">
                <div class="card-header">
                    <h5 class="mb-0"><i class="bi bi-speedometer2"></i> پنل مدیریت ادمین</h5>
                </div>
                <div class="card-body">
                    <div class="d-flex justify-content-between align-items-center mb-4">
                        <h4>مدیریت سیستم</h4>
                        <button class="btn btn-danger" onclick="adminLogout()">
                            <i class="bi bi-box-arrow-right"></i> خروج
                        </button>
                    </div>
                    
                    <ul class="nav nav-tabs" id="adminTabs" role="tablist">
                        <li class="nav-item" role="presentation">
                            <button class="nav-link active" id="messages-tab" data-bs-toggle="tab" data-bs-target="#messages" type="button" role="tab">ارسال پیام</button>
                        </li>
                        <li class="nav-item" role="presentation">
                            <button class="nav-link" id="banners-tab" data-bs-toggle="tab" data-bs-target="#banners" type="button" role="tab">مدیریت بنرها</button>
                        </li>
                    </ul>
                    
                    <div class="tab-content mt-3" id="adminTabContent">
                        <div class="tab-pane fade show active" id="messages" role="tabpanel">
                            <div class="card mb-4">
                                <div class="card-header">
                                    <h5 class="mb-0"><i class="bi bi-megaphone"></i> ارسال پیام به همه کاربران</h5>
                                </div>
                                <div class="card-body">
                                    <form id="admin-message-form">
                                        <div class="mb-3">
                                            <label for="admin-message" class="form-label">متن پیام</label>
                                            <textarea class="form-control" id="admin-message" rows="3" required></textarea>
                                        </div>
                                        <div class="mb-3">
                                            <label class="form-label">اولویت پیام</label>
                                            <div class="form-check">
                                                <input class="form-check-input" type="radio" name="priority" id="priority-low" value="low" checked>
                                                <label class="form-check-label" for="priority-low">کم</label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="radio" name="priority" id="priority-medium" value="medium">
                                                <label class="form-check-label" for="priority-medium">متوسط</label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="radio" name="priority" id="priority-high" value="high">
                                                <label class="form-check-label" for="priority-high">بالا</label>
                                            </div>
                                        </div>
                                        <button type="submit" class="btn btn-primary">
                                            <i class="bi bi-send"></i> ارسال پیام
                                        </button>
                                    </form>
                                </div>
                            </div>
                        </div>
                        
                        <div class="tab-pane fade" id="banners" role="tabpanel">
                            <div class="card">
                                <div class="card-header">
                                    <h5 class="mb-0"><i class="bi bi-images"></i> مدیریت بنرها</h5>
                                </div>
                                <div class="card-body">
                                    <div class="input-group mb-3">
                                        <input type="text" class="form-control" placeholder="جستجوی بنر...">
                                        <button class="btn btn-outline-secondary" type="button">
                                            <i class="bi bi-search"></i>
                                        </button>
                                    </div>
                                    <div id="admin-banners-container">
                                        <!-- بنرهای مدیریتی اینجا نمایش داده می شوند -->
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- مودال نمایش توضیحات بنر -->
    <div class="modal fade" id="bannerModal" tabindex="-1" aria-labelledby="bannerModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="bannerModalLabel">عنوان بنر</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <img id="modalBannerImage" src="" class="modal-banner-img" alt="بنر">
                    <div id="modalBannerContent">
                        <!-- محتوای بنر اینجا نمایش داده می شود -->
                    </div>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">بستن</button>
                    <a id="modalBannerLink" href="#" target="_blank" class="btn btn-primary">مشاهده لینک</a>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // داده های نمونه
        let banners = [
            {
                id: 1,
                title: "لبنگ مکس",
                description: "دریافت بروزترین اطلاعیه ها و اخبار",
                image: "https://via.placeholder.com/300x150/3498db/ffffff?text=لبنگ+مکس",
                url: "#",
                category: "عمومی",
                likes: 24,
                approved: true,
                status: "blue",
                tags: ["اخبار", "اطلاعیه"],
                date: "1402/05/15"
            },
            {
                id: 2,
                title: "جبای، دستیار هوش مصنوعی",
                description: "جبای، دستیار هوشمند برای پاسخگویی به سوالات شما",
                image: "https://via.placeholder.com/300x150/2ecc71/ffffff?text=جبای+هوش+مصنوعی",
                url: "#",
                category: "خدمات",
                likes: 18,
                approved: true,
                status: "blue",
                tags: ["هوش مصنوعی", "دستیار"],
                date: "1402/05/10"
            },
            {
                id: 3,
                title: "ربات چت ناشناس چتوگرام",
                description: "⚠️چتوگرام ⚠️چبه ⚠️دی......",
                image: "https://via.placeholder.com/300x150/e74c3c/ffffff?text=چتوگرام",
                url: "#",
                category: "سرگرمی",
                likes: 32,
                approved: true,
                status: "yellow",
                tags: ["چت بات", "ربات"],
                date: "1402/05/05"
            },
            {
                id: 4,
                title: "خبر فوری",
                description: "⚠️سفارش تبلیغ خبرفوری و اطلاع رسانی",
                image: "https://via.placeholder.com/300x150/f39c12/ffffff?text=خبر+فوری",
                url: "#",
                category: "اخبار",
                likes: 15,
                approved: true,
                status: "blue",
                tags: ["خبر", "تبلیغات"],
                date: "1402/05/01"
            }
        ];
        
        let adminMessages = [];
        let chatMessages = [];
        let isAdminLoggedIn = false;
        let currentUser = null;
        let adminCredentials = { username: "admin", password: "admin123" };
        let userProfile = {
            username: "user123",
            name: "کاربر لینکدونی",
            email: "user@linkoni.ir",
            avatar: "https://ui-avatars.com/api/?name=کاربر+لینکدونی&size=100&background=3498db&color=fff",
            joinDate: "1402/05/01",
            bannersCount: 0,
            messagesCount: 0,
            bio: "من یک کاربر فعال در لینکدونی هستم"
        };

        // مدیریت کاربران
        let users = [
            { username: "user123", password: "pass123", email: "user@linkoni.ir" }
        ];

        // ذخیره داده‌ها در localStorage
        function saveData() {
            localStorage.setItem('banners', JSON.stringify(banners));
            localStorage.setItem('adminMessages', JSON.stringify(adminMessages));
            localStorage.setItem('chatMessages', JSON.stringify(chatMessages));
            localStorage.setItem('userProfile', JSON.stringify(userProfile));
            localStorage.setItem('users', JSON.stringify(users));
        }

        // بارگذاری داده‌ها از localStorage
        function loadData() {
            const savedBanners = localStorage.getItem('banners');
            const savedAdminMessages = localStorage.getItem('adminMessages');
            const savedChatMessages = localStorage.getItem('chatMessages');
            const savedUserProfile = localStorage.getItem('userProfile');
            const savedUsers = localStorage.getItem('users');
            
            if (savedBanners) banners = JSON.parse(savedBanners);
            if (savedAdminMessages) adminMessages = JSON.parse(savedAdminMessages);
            if (savedChatMessages) chatMessages = JSON.parse(savedChatMessages);
            if (savedUserProfile) userProfile = JSON.parse(savedUserProfile);
            if (savedUsers) users = JSON.parse(savedUsers);
        }

        // نمایش صفحه مورد نظر و مخفی کردن بقیه
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => {
                page.style.display = 'none';
            });
            
            document.getElementById(pageId + '-page').style.display = 'block';
            
            if (pageId === 'home') {
                loadBanners();
            } else if (pageId === 'chat-room') {
                loadChatMessages();
                updateAdminIndicator();
            } else if (pageId === 'message-inbox') {
                loadAdminMessages();
            } else if (pageId === 'profile') {
                loadProfile();
            } else if (pageId === 'admin-panel' && isAdminLoggedIn) {
                loadAdminBanners();
            }
        }

        // بارگذاری بنرها در صفحه اصلی
        function loadBanners() {
            const bannersContainer = document.getElementById('banners-container');
            
            if (banners.length === 0) {
                bannersContainer.innerHTML = `
                    <div class="col-12">
                        <div class="text-center py-5 text-muted">
                            <i class="bi bi-images display-4"></i>
                            <h5 class="mt-3">هنوز بنری ثبت نشده است</h5>
                            <p>اولین نفری باشید که بنر خود را ثبت می‌کند</p>
                        </div>
                    </div>
                `;
            } else {
                bannersContainer.innerHTML = '';
                banners.filter(banner => banner.approved).forEach(banner => {
                    const statusIcon = banner.status === "blue" 
                        ? '<span class="banner-status status-blue"><i class="bi bi-patch-check-fill"></i></span>' 
                        : banner.status === "yellow" 
                            ? '<span class="banner-status status-yellow"><i class="bi bi-exclamation-circle-fill"></i></span>' 
                            : '';
                    
                    const bannerElement = `
                        <div class="col-12 mb-4">
                            <div class="card banner-card h-100" onclick="showBannerDetails(${banner.id})">
                                <div class="row g-0">
                                    <div class="col-md-4">
                                        <img src="${banner.image}" class="img-fluid rounded-start h-100 w-100" style="object-fit: cover;" alt="${banner.title}">
                                    </div>
                                    <div class="col-md-8">
                                        <div class="card-body">
                                            <div class="d-flex justify-content-between align-items-start">
                                                <h5 class="card-title">${banner.title}</h5>
                                                ${banner.status === "blue" ? '<span class="badge bg-primary"><i class="bi bi-patch-check-fill"></i> تایید شده</span>' : ''}
                                                ${banner.status === "yellow" ? '<span class="badge bg-warning"><i class="bi bi-exclamation-circle-fill"></i> هشدار</span>' : ''}
                                            </div>
                                            <p class="card-text">${banner.description}</p>
                                            <div class="d-flex justify-content-between align-items-center">
                                                <div>
                                                    <span class="badge bg-secondary">${banner.category}</span>
                                                    <span class="text-muted me-2"><i class="bi bi-heart-fill text-danger"></i> ${banner.likes}</span>
                                                    <span class="text-muted"><i class="bi bi-calendar"></i> ${banner.date}</span>
                                                </div>
                                                <button class="btn btn-outline-primary btn-sm" onclick="event.stopPropagation(); likeBanner(${banner.id})">
                                                    <i class="bi bi-hand-thumbs-up"></i> لایک
                                                </button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    `;
                    bannersContainer.innerHTML += bannerElement;
                });
            }
        }

        // نمایش جزئیات بنر در مودال
        function showBannerDetails(bannerId) {
            const banner = banners.find(b => b.id === bannerId);
            if (banner) {
                document.getElementById('bannerModalLabel').textContent = banner.title;
                document.getElementById('modalBannerImage').src = banner.image;
                
                let modalContent = `
                    <p><strong>دسته‌بندی:</strong> ${banner.category}</p>
                    <p><strong>تگ‌ها:</strong> ${banner.tags.join(', ')}</p>
                    <p><strong>تاریخ ثبت:</strong> ${banner.date}</p>
                    <p><strong>لایک‌ها:</strong> ${banner.likes}</p>
                    <hr>
                    <h6>توضیحات کامل:</h6>
                    <p>${banner.description}</p>
                `;
                
                document.getElementById('modalBannerContent').innerHTML = modalContent;
                
                if (banner.url) {
                    document.getElementById('modalBannerLink').href = banner.url;
                    document.getElementById('modalBannerLink').style.display = 'inline-block';
                } else {
                    document.getElementById('modalBannerLink').style.display = 'none';
                }
                
                // نمایش مودال
                const bannerModal = new bootstrap.Modal(document.getElementById('bannerModal'));
                bannerModal.show();
            }
        }

        // تنظیم وضعیت بنر توسط ادمین
        function setBannerStatus(bannerId, status) {
            const banner = banners.find(b => b.id === bannerId);
            if (banner) {
                banner.status = status;
                loadBanners();
                saveData();
                showNotification(`وضعیت بنر تغییر کرد`, 'success');
            }
        }

        // لایک کردن بنر
        function likeBanner(bannerId) {
            const banner = banners.find(b => b.id === bannerId);
            if (banner) {
                banner.likes++;
                loadBanners();
                saveData();
                showNotification(`بنر "${banner.title}" لایک شد!`, 'success');
            }
        }

        // مدیریت فرم ثبت بنر
        document.getElementById('banner-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const title = document.getElementById('banner-title').value;
            const description = document.getElementById('banner-description').value;
            const url = document.getElementById('banner-url').value;
            const category = document.getElementById('banner-category').value;
            const tags = document.getElementById('banner-tags').value.split(',').map(tag => tag.trim());
            const terms = document.getElementById('banner-terms').checked;
            const imageInput = document.getElementById('banner-image-upload');
            
            if (!terms) {
                showNotification('لطفا با شرایط و قوانین موافقت کنید', 'error');
                return;
            }
            
            if (imageInput.files.length === 0) {
                showNotification('لطفا یک تصویر برای بنر انتخاب کنید', 'error');
                return;
            }
            
            const reader = new FileReader();
            reader.onload = function(e) {
                const now = new Date();
                const date = `${now.getFullYear()}/${now.getMonth() + 1}/${now.getDate()}`;
                
                const newBanner = {
                    id: banners.length + 1,
                    title: title,
                    description: description,
                    url: url,
                    image: e.target.result,
                    category: category,
                    tags: tags,
                    approved: false,
                    likes: 0,
                    status: null,
                    date: date
                };
                
                banners.push(newBanner);
                
                // افزایش شمارنده بنرهای کاربر
                userProfile.bannersCount++;
                document.getElementById('profile-banners-count').textContent = userProfile.bannersCount;
                
                // اضافه کردن به تاریخچه فعالیت
                const activitiesContainer = document.getElementById('user-activities');
                
                activitiesContainer.innerHTML = `
                    <div class="activity-item">
                        <div>ثبت بنر جدید "${title}"</div>
                        <small class="text-muted">همین الان</small>
                    </div>
                ` + (activitiesContainer.innerHTML || '');
                
                showNotification('بنر شما با موفقیت ثبت شد و پس از تایید ادمین نمایش داده خواهد شد.', 'success');
                document.getElementById('banner-form').reset();
                document.getElementById('banner-image-preview').style.display = 'none';
                saveData();
                showPage('home');
            };
            reader.readAsDataURL(imageInput.files[0]);
        });

        // پیش‌نمایش تصویر بنر
        document.getElementById('banner-image-upload').addEventListener('change', function(e) {
            if (this.files && this.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    document.getElementById('banner-preview').src = e.target.result;
                    document.getElementById('banner-image-preview').style.display = 'block';
                };
                reader.readAsDataURL(this.files[0]);
            }
        });

        // حذف تصویر بنر
        function removeBannerImage() {
            document.getElementById('banner-image-upload').value = '';
            document.getElementById('banner-image-preview').style.display = 'none';
        }

        // مدیریت فرم ورود کاربر
        document.getElementById('login-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('login-username').value;
            const password = document.getElementById('login-password').value;
            
            const user = users.find(u => u.username === username && u.password === password);
            
            if (user) {
                currentUser = user;
                userProfile.username = user.username;
                userProfile.email = user.email;
                
                document.getElementById('login-page').style.display = 'none';
                document.getElementById('main-navbar').style.display = 'flex';
                document.getElementById('main-container').style.display = 'block';
                showPage('home');
                showNotification(`خوش آمدید ${username}`, 'success');
            } else {
                showNotification('نام کاربری یا رمز عبور اشتباه است.', 'error');
            }
        });

        // مدیریت فرم ثبت نام کاربر
        document.getElementById('register-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('register-username').value;
            const email = document.getElementById('register-email').value;
            const password = document.getElementById('register-password').value;
            const confirmPassword = document.getElementById('register-confirm-password').value;
            
            if (password !== confirmPassword) {
                showNotification('رمز عبور و تکرار آن مطابقت ندارند.', 'error');
                return;
            }
            
            if (users.find(u => u.username === username)) {
                showNotification('این نام کاربری قبلا ثبت شده است.', 'error');
                return;
            }
            
            users.push({ username, password, email });
            currentUser = { username, password, email };
            userProfile.username = username;
            userProfile.email = email;
            
            document.getElementById('login-page').style.display = 'none';
            document.getElementById('main-navbar').style.display = 'flex';
            document.getElementById('main-container').style.display = 'block';
            showPage('home');
            saveData();
            showNotification('ثبت نام با موفقیت انجام شد.', 'success');
        });

        // مدیریت فرم ورود ادمین
        document.getElementById('admin-login-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('admin-username').value;
            const password = document.getElementById('admin-password').value;
            
            if (username === adminCredentials.username && password === adminCredentials.password) {
                isAdminLoggedIn = true;
                showNotification('با موفقیت وارد پنل مدیریت شدید', 'success');
                updateNavbar();
                showPage('admin-panel');
            } else {
                showNotification('نام کاربری یا رمز عبور اشتباه است.', 'error');
            }
        });

        // بروزرسانی نوار ناوبری بر اساس وضعیت ورود
        function updateNavbar() {
            const adminNavItem = document.getElementById('admin-nav-item');
            
            if (isAdminLoggedIn) {
                adminNavItem.innerHTML = `
                    <div class="d-flex align-items-center me-3 text-light">
                        <i class="bi bi-patch-check-fill me-1"></i>
                        <span>مدیر سیستم</span>
                    </div>
                `;
            } else {
                adminNavItem.innerHTML = `
                    <button class="btn btn-outline-light me-2" onclick="showPage('admin-login')">
                        <i class="bi bi-shield-lock"></i> ورود ادمین
                    </button>
                `;
            }
        }

        // بارگذاری پروفایل کاربر
        function loadProfile() {
            document.getElementById('profile-name').textContent = userProfile.name;
            document.getElementById('profile-username').textContent = userProfile.username;
            document.getElementById('profile-email').textContent = userProfile.email;
            document.getElementById('profile-avatar').src = userProfile.avatar;
            document.getElementById('profile-join-date').textContent = `عضو since ${userProfile.joinDate}`;
            document.getElementById('profile-banners-count').textContent = userProfile.bannersCount;
            document.getElementById('profile-messages-count').textContent = userProfile.messagesCount;
            
            // مقداردهی فرم ویرایش
            document.getElementById('edit-username').value = userProfile.username;
            document.getElementById('edit-email').value = userProfile.email;
            document.getElementById('edit-bio').value = userProfile.bio;
        }

        // نمایش/پنهان کردن فرم ویرایش پروفایل
        function toggleEditProfile() {
            const profileView = document.getElementById('profile-view');
            const profileEditForm = document.getElementById('profile-edit-form');
            
            if (profileEditForm.style.display === 'block') {
                profileEditForm.style.display = 'none';
                profileView.style.display = 'block';
            } else {
                profileView.style.display = 'none';
                profileEditForm.style.display = 'block';
            }
        }

        // مدیریت فرم ویرایش پروفایل
        document.getElementById('edit-profile-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            userProfile.email = document.getElementById('edit-email').value;
            userProfile.bio = document.getElementById('edit-bio').value;
            
            loadProfile();
            toggleEditProfile();
            saveData();
            showNotification('پروفایل شما با موفقیت به روز شد.', 'success');
        });

        // پیش‌نمایش تصویر پروفایل
        document.getElementById('avatar-upload').addEventListener('change', function(e) {
            if (this.files && this.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    userProfile.avatar = e.target.result;
                    document.getElementById('profile-avatar').src = e.target.result;
                    saveData();
                };
                reader.readAsDataURL(this.files[0]);
            }
        });

        // بارگذاری پیام های چت
        function loadChatMessages() {
            const chatContainer = document.getElementById('chat-messages');
            
            if (chatMessages.length === 0) {
                chatContainer.innerHTML = `
                    <div class="text-center py-5 text-muted">
                        <i class="bi bi-chat-dots display-4"></i>
                        <h5 class="mt-3">هنوز پیامی ارسال نشده است</h5>
                        <p>اولین نفری باشید که پیام ارسال می‌کند</p>
                    </div>
                `;
            } else {
                chatContainer.innerHTML = '';
                
                chatMessages.forEach(msg => {
                    const messageElement = `
                        <div class="message ${msg.isAdmin ? 'admin-message' : 'user-message'}">
                            <div class="d-flex align-items-center">
                                <img src="${msg.avatar}" class="user-avatar">
                                <strong>${msg.user} ${msg.isAdmin ? '<i class="bi bi-patch-check-fill verified-badge"></i>' : ''}</strong>
                            </div>
                            <div class="mt-1">${msg.message}</div>
                            <div class="d-flex justify-content-between mt-2">
                                <div class="text-muted small">${msg.time}</div>
                                <button class="btn btn-sm p-0 text-primary" onclick="likeMessage(this)">
                                    <i class="bi bi-hand-thumbs-up"></i> ${msg.likes}
                                </button>
                            </div>
                        </div>
                    `;
                    chatContainer.innerHTML += messageElement;
                });
                
                // اسکرول به پایین
                chatContainer.scrollTop = chatContainer.scrollHeight;
            }
        }

        // ارسال پیام در چت
        function sendMessage() {
            const input = document.getElementById('chat-input');
            const message = input.value.trim();
            
            if (message) {
                const now = new Date();
                const time = `${now.getHours()}:${now.getMinutes()}`;
                
                chatMessages.push({
                    user: isAdminLoggedIn ? "مدیر سیستم" : "شما",
                    message: message,
                    time: time,
                    avatar: isAdminLoggedIn ? "https://ui-avatars.com/api/?name=ادمین&background=3498db&color=fff" : userProfile.avatar,
                    likes: 0,
                    isAdmin: isAdminLoggedIn
                });
                
                loadChatMessages();
                input.value = '';
                saveData();
                
                // افزایش شمارنده پیام‌های کاربر
                userProfile.messagesCount++;
                document.getElementById('profile-messages-count').textContent = userProfile.messagesCount;
            }
        }

        // لایک کردن پیام
        function likeMessage(btn) {
            const likes = parseInt(btn.innerHTML.match(/\d+/)[0]);
            btn.innerHTML = `<i class="bi bi-hand-thumbs-up"></i> ${likes + 1}`;
            btn.classList.add('text-danger');
        }

        // بروزرسانی نشانگر وضعیت ادمین
        function updateAdminIndicator() {
            const adminIndicator = document.getElementById('admin-indicator');
            const adminUserItem = document.getElementById('admin-user-item');
            
            if (isAdminLoggedIn) {
                adminIndicator.style.display = 'block';
                adminUserItem.style.display = 'flex';
            } else {
                adminIndicator.style.display = 'none';
                adminUserItem.style.display = 'none';
            }
        }

        // انتخاب کاربر برای چت
        function selectUser(userId) {
            selectedChatUser = userId;
            
            const users = {
                "admin": "مدیر سیستم",
                "all": "همه کاربران"
            };
            
            document.getElementById('selected-user').textContent = users[userId];
        }

        // بارگذاری پیام های ادمین
        function loadAdminMessages() {
            const messagesContainer = document.getElementById('messages-container');
            
            if (adminMessages.length === 0) {
                messagesContainer.innerHTML = `
                    <div class="text-center py-5 text-muted">
                        <i class="bi bi-inbox display-4"></i>
                        <h5 class="mt-3">صندوق پیام خالی است</h5>
                        <p>هیچ پیامی دریافت نکرده‌اید</p>
                    </div>
                `;
            } else {
                messagesContainer.innerHTML = '';
                adminMessages.forEach(msg => {
                    const priorityClass = msg.priority === 'high' ? 'danger' : (msg.priority === 'medium' ? 'warning' : 'info');
                    
                    const messageElement = `
                        <div class="card mb-3">
                            <div class="card-header d-flex justify-content-between">
                                <span>پیام مدیریت</span>
                                <span class="badge bg-${priorityClass}">${msg.priority === 'high' ? 'بالا' : (msg.priority === 'medium' ? 'متوسط' : 'کم')}</span>
                            </div>
                            <div class="card-body">
                                <p class="card-text">${msg.content}</p>
                                <small class="text-muted">تاریخ: ${msg.date}</small>
                            </div>
                        </div>
                    `;
                    messagesContainer.innerHTML += messageElement;
                });
            }
        }

        // مدیریت فرم ارسال پیام توسط ادمین
        document.getElementById('admin-message-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const message = document.getElementById('admin-message').value;
            const priority = document.querySelector('input[name="priority"]:checked').value;
            const now = new Date();
            const date = `${now.getFullYear()}/${now.getMonth() + 1}/${now.getDate()}`;
            
            adminMessages.unshift({
                id: adminMessages.length + 1,
                content: message,
                date: date,
                priority: priority,
                read: false
            });
            
            showNotification('پیام شما با موفقیت برای همه کاربران ارسال شد.', 'success');
            
            // افزایش شمارنده نوتیفیکیشن
            const notificationBadge = document.getElementById('message-notification');
            notificationBadge.textContent = parseInt(notificationBadge.textContent || 0) + 1;
            
            this.reset();
            saveData();
        });

        // بارگذاری بنرها در پنل ادمین
        function loadAdminBanners() {
            const adminBannersContainer = document.getElementById('admin-banners-container');
            
            if (banners.length === 0) {
                adminBannersContainer.innerHTML = `
                    <div class="text-center py-5 text-muted">
                        <i class="bi bi-images display-4"></i>
                        <h5 class="mt-3">هنوز بنری برای مدیریت وجود ندارد</h5>
                        <p>هیچ کاربری تاکنون بنری ثبت نکرده است</p>
                    </div>
                `;
            } else {
                adminBannersContainer.innerHTML = '';
                banners.forEach(banner => {
                    const statusBadge = banner.approved ? 
                        '<span class="badge bg-success">تایید شده</span>' : 
                        '<span class="badge bg-warning">در انتظار تایید</span>';
                    
                    const bannerElement = `
                        <div class="card mb-2">
                            <div class="card-body">
                                <div class="d-flex justify-content-between align-items-center">
                                    <h6 class="card-title mb-0">${banner.title}</h6>
                                    ${statusBadge}
                                </div>
                                <p class="mb-1 mt-2">دسته: ${banner.category}</p>
                                <p class="mb-2">لایک: ${banner.likes}</p>
                                <div class="btn-group btn-group-sm">
                                    <button class="btn btn-outline-success" onclick="approveBanner(${banner.id})">تایید</button>
                                    <button class="btn btn-outline-danger" onclick="deleteBanner(${banner.id})">حذف</button>
                                </div>
                            </div>
                        </div>
                    `;
                    adminBannersContainer.innerHTML += bannerElement;
                });
            }
        }

        // تایید بنر توسط ادمین
        function approveBanner(bannerId) {
            const banner = banners.find(b => b.id === bannerId);
            if (banner) {
                banner.approved = true;
                loadAdminBanners();
                loadBanners();
                saveData();
                showNotification('بنر تایید شد.', 'success');
            }
        }

        // حذف بنر توسط ادمین
        function deleteBanner(bannerId) {
            if (confirm('آیا از حذف این بنر اطمینان دارید؟')) {
                banners = banners.filter(b => b.id !== bannerId);
                loadAdminBanners();
                loadBanners();
                saveData();
                showNotification('بنر حذف شد.', 'success');
            }
        }

        // خروج ادمین
        function adminLogout() {
            isAdminLoggedIn = false;
            showNotification('از پنل مدیریت خارج شدید.', 'info');
            updateNavbar();
            showPage('home');
        }

        // خروج کاربر
        function logout() {
            currentUser = null;
            isAdminLoggedIn = false;
            
            document.getElementById('main-navbar').style.display = 'none';
            document.getElementById('main-container').style.display = 'none';
            document.getElementById('login-page').style.display = 'block';
            
            showNotification('با موفقیت خارج شدید.', 'info');
        }

        // نمایش نوتیفیکیشن
        function showNotification(message, type) {
            // ایجاد المان نوتیفیکیشن
            const notification = document.createElement('div');
            notification.className = `alert alert-${type === 'success' ? 'success' : type === 'error' ? 'danger' : 'info'} alert-dismissible fade show position-fixed`;
            notification.style.cssText = 'top: 20px; right: 20px; z-index: 1050; min-width: 300px;';
            notification.innerHTML = `
                ${message}
                <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
            `;
            
            document.body.appendChild(notification);
            
            // حذف خودکار پس از 3 ثانیه
            setTimeout(() => {
                if (notification.parentNode) {
                    notification.parentNode.removeChild(notification);
                }
            }, 3000);
        }

        // مرتب‌سازی بنرها
        function sortBanners(method) {
            if (method === 'newest') {
                banners.sort((a, b) => b.id - a.id);
            } else if (method === 'popular') {
                banners.sort((a, b) => b.likes - a.likes);
            }
            
            loadBanners();
            showNotification(`بنرها بر اساس ${method === 'newest' ? 'جدیدترین' : 'محبوب‌ترین'} مرتب شدند.`, 'success');
        }

        // مقداردهی اولیه
        document.addEventListener('DOMContentLoaded', function() {
            loadData();
            updateNavbar();
            
            // نمایش صفحه ورود به عنوان پیش فرض
            document.getElementById('login-page').style.display = 'block';
            
            // بارگذاری بنرها
            loadBanners();
        });
    </script>
</body>
</html>
