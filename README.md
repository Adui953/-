<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>城市与海岸摄影集</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#1a237e',
                        secondary: '#ff6d00',
                        neutral: '#f5f5f5',
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .image-grid {
                display: grid;
                grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
                gap: 1rem;
            }
            .image-hover {
                transition: transform 0.3s ease, box-shadow 0.3s ease;
            }
            .image-hover:hover {
                transform: scale(1.02);
                box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
            }
            /* 模态框样式 */
            .modal {
                display: none;
                position: fixed;
                z-index: 100;
                left: 0;
                top: 0;
                width: 100%;
                height: 100%;
                overflow: auto;
                background-color: rgba(0,0,0,0.9);
            }
            .modal-content {
                margin: auto;
                display: block;
                width: 80%;
                max-width: 1000px;
                max-height: 80vh;
                object-fit: contain;
                margin-top: 5vh;
            }
            .close {
                position: absolute;
                top: 15px;
                right: 35px;
                color: #f1f1f1;
                font-size: 40px;
                font-weight: bold;
                cursor: pointer;
            }
            .modal-caption {
                margin: auto;
                display: block;
                width: 80%;
                max-width: 1000px;
                text-align: center;
                color: #ccc;
                padding: 10px 0;
            }
        }
    </style>
</head>
<body class="bg-neutral font-sans">
    <!-- 导航栏 -->
    <nav class="bg-primary text-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center">
                <i class="fa fa-camera-retro text-2xl mr-2"></i>
                <h1 class="text-xl font-bold">城市与海岸摄影集</h1>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href=" " class="hover:text-secondary transition-colors">城市建筑</a >
                <a href="#coast" class="hover:text-secondary transition-colors">海岸风情</a >
                <a href="#about" class="hover:text-secondary transition-colors">关于作者</a >
            </div>
            <div class="md:hidden">
                <button class="text-white focus:outline-none" id="mobile-menu-button">
                    <i class="fa fa-bars text-xl"></i>
                </button>
            </div>
        </div>
        <!-- 移动端菜单 -->
        <div class="hidden md:hidden bg-primary-dark px-4 py-2" id="mobile-menu">
            <a href="#city" class="block py-2 hover:text-secondary transition-colors">城市建筑</a >
            <a href="#coast" class="block py-2 hover:text-secondary transition-colors">海岸风情</a >
            <a href="#about" class="block py-2 hover:text-secondary transition-colors">关于作者</a >
        </div>
    </nav>

    <!-- 英雄区域 -->
    <header class="relative h-96 flex items-center justify-center overflow-hidden">
        < img src="https://images.unsplash.com/photo-1477959858617-67f85cf4f1df?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="城市天际线" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-black bg-opacity-40 flex items-center justify-center">
            <div class="text-center text-white px-4">
                <h2 class="text-4xl md:text-5xl font-bold mb-3">镜头下的城市与海岸</h2>
                <p class="text-xl md:text-2xl">记录建筑的线条与自然的光影</p >
            </div>
        </div>
    </header>

    <!-- 图片分类区域 -->
    <main class="container mx-auto px-4 py-8">
        <!-- 城市建筑部分 -->
        <section id="city" class="mb-12">
            <h2 class="text-3xl font-bold mb-6 text-primary border-b-2 border-secondary pb-2">城市建筑</h2>
            <div class="image-grid">
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1449824913935-59a10b8d2000?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="城市建筑群" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">现代建筑峡谷</h3>
                        <p class="text-gray-600 text-sm">玻璃幕墙与钢铁森林的碰撞</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1487958449943-2429e8be8625?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="建筑细节" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">建筑线条</h3>
                        <p class="text-gray-600 text-sm">几何美学与现代设计的融合</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1496568816309-51d7c20e3b21?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1738&q=80" alt="城市日落" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">日落都市</h3>
                        <p class="text-gray-600 text-sm">夕阳为建筑披上金色外衣</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1479030160180-b1860951d696?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="城市黄昏" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">黄昏天际线</h3>
                        <p class="text-gray-600 text-sm">蓝调时刻的城市轮廓</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1464822759849-e0e100921dae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="城市夜景" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">都市霓虹</h3>
                        <p class="text-gray-600 text-sm">夜晚的建筑灯光秀</p >
                    </div>
                </div>
            </div>
        </section>

        <!-- 海岸风情部分 -->
        <section id="coast" class="mb-12">
            <h2 class="text-3xl font-bold mb-6 text-primary border-b-2 border-secondary pb-2">海岸风情</h2>
            <div class="image-grid">
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1746&q=80" alt="海岸日落" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">粉蓝海岸</h3>
                        <p class="text-gray-600 text-sm">晚霞渲染的海岸风光</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1506929562872-bb421503ef21?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1725&q=80" alt="夜间渔船" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">夜海渔舟</h3>
                        <p class="text-gray-600 text-sm">夜色中海上的点点灯火</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://images.unsplash.com/photo-1505852679233-d9fd70aff56d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="红日海岸" class="w-full h-64 object-cover cursor-pointer">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">红日映海</h3>
                        <p class="text-gray-600 text-sm">壮丽的海上日出景象</p >
                    </div>
                </div>
            </div>
        </section>

        <!-- 关于作者部分 -->
        <section id="about" class="bg-white rounded-lg shadow-md p-6 md:p-8">
            <h2 class="text-3xl font-bold mb-6 text-primary border-b-2 border-secondary pb-2">关于作者</h2>
            <div class="flex flex-col md:flex-row items-center">
                < img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=774&q=80" alt="作者头像" class="w-32 h-32 rounded-full object-cover mb-4 md:mb-0 md:mr-6">
                <div>
                    <h3 class="text-xl font-bold mb-2">阿克dui</h3>
                    <p class="text-gray-600 mb-4">一位热爱摄影的创作者，专注于捕捉城市建筑的独特线条与海岸自然的绝美光影。用镜头记录下城市的繁华与海岸的宁静，展现不同场景下的视觉魅力。</p >
                    <div class="flex space-x-4">
                        <a href="#" class="text-primary hover:text-secondary transition-colors"><i class="fa fa-instagram text-xl"></i></a >
                        <a href="#" class="text-primary hover:text-secondary transition-colors"><i class="fa fa-weibo text-xl"></i></a >
                        <a href="#" class="text-primary hover:text-secondary transition-colors"><i class="fa fa-behance text-xl"></i></a >
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- 图片模态框 -->
    <div id="image-modal" class="modal">
        <span class="close" id="close-modal">&times;</span>
        < img class="modal-content" id="modal-image">
        <div id="modal-caption" class="modal-caption"></div>
    </div>

    <!-- 页脚 -->
    <footer class="bg-primary text-white py-6">
        <div class="container mx-auto px-4 text-center">
            <p>&copy; 2025 城市与海岸摄影集. 保留所有权利.</p >
            <p class="mt-2 text-sm opacity-80">设计与开发：为摄影作品打造的展示平台</p >
        </div>
    </footer>

    <script>
        // 移动端菜单功能
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // 图片模态框功能
        const modal = document.getElementById('image-modal');
        const modalImg = document.getElementById('modal-image');
        const captionText = document.getElementById('modal-caption');
        const closeModal = document.getElementById('close-modal');

        // 为所有图片添加点击事件
        document.querySelectorAll('.image-grid img').forEach(img => {
            img.addEventListener('click', function() {
                modal.style.display = 'block';
                modalImg.src = this.src;
                captionText.innerHTML = this.alt;
            });
        });

        // 关闭模态框
        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        // 点击模态框外部也关闭
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.style.display = 'none';
            }
        });

        // 添加键盘支持
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && modal.style.display === 'block') {
                modal.style.display = 'none';
            }
        });

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                    
                    // 如果是移动端菜单，点击后隐藏菜单
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                }
            });
        });
    </script>
</body>
</html>
