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
        }
    </style>
</head>
<body class="bg-neutral font-sans">
    <!-- 导航栏 -->
    <nav class="bg-primary text-white shadow-md">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center">
                <<i class="fa fa-camera-retro text-2xl mr-2"></</i>
                <h1 class="text-xl font-bold">城市与海岸摄影集</h1>
            </div>
            <div class="hidden md:flex space-x-6">
                <a href=" " class="hover:text-secondary transition-colors">城市建筑</a >
                <a href="#coast" class="hover:text-secondary transition-colors">海岸风情</a >
                <a href="#about" class="hover:text-secondary transition-colors">关于作者</a >
            </div>
            <div class="md:hidden">
                <button class="text-white focus:outline-none">
                    <<i class="fa fa-bars text-xl"></</i>
                </button>
            </div>
        </div>
    </nav>

    <!-- 英雄区域 -->
    <header class="relative h-96 flex items-center justify-center overflow-hidden">
        < img src="https://picsum.photos/id/1033/1600/900" alt="城市天际线" class="w-full h-full object-cover">
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
                    < img src="https://i.imgur.com/your-image1.jpg" alt="城市建筑群" class="w-full h-64 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">现代建筑峡谷</h3>
                        <p class="text-gray-600 text-sm">玻璃幕墙与钢铁森林的碰撞</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://i.imgur.com/your-image2.jpg" alt="建筑细节" class="w-full h-64 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">建筑线条</h3>
                        <p class="text-gray-600 text-sm">几何美学与现代设计的融合</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://i.imgur.com/your-image3.jpg" alt="城市日落" class="w-full h-64 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">日落都市</h3>
                        <p class="text-gray-600 text-sm">夕阳为建筑披上金色外衣</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://i.imgur.com/your-image4.jpg" alt="城市黄昏" class="w-full h-64 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">黄昏天际线</h3>
                        <p class="text-gray-600 text-sm">蓝调时刻的城市轮廓</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://i.imgur.com/your-image5.jpg" alt="城市夜景" class="w-full h-64 object-cover">
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
                    < img src="https://i.imgur.com/your-image6.jpg" alt="海岸日落" class="w-full h-64 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">粉蓝海岸</h3>
                        <p class="text-gray-600 text-sm">晚霞渲染的海岸风光</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://i.imgur.com/your-image7.jpg" alt="夜间渔船" class="w-full h-64 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg">夜海渔舟</h3>
                        <p class="text-gray-600 text-sm">夜色中海上的点点灯火</p >
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md image-hover">
                    < img src="https://i.imgur.com/your-image8.jpg" alt="红日海岸" class="w-full h-64 object-cover">
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
                < img src="https://picsum.photos/id/64/200/200" alt="作者头像" class="w-32 h-32 rounded-full object-cover mb-4 md:mb-0 md:mr-6">
                <div>
                    <h3 class="text-xl font-bold mb-2">阿克dui</h3>
                    <p class="text-gray-600 mb-4">一位热爱摄影的创作者，专注于捕捉城市建筑的独特线条与海岸自然的绝美光影。用镜头记录下城市的繁华与海岸的宁静，展现不同场景下的视觉魅力。</p >
                    <div class="flex space-x-4">
                        <a href="#" class="text-primary hover:text-secondary transition-colors"><<i class="fa fa-instagram text-xl"></</i></a >
                        <a href="#" class="text-primary hover:text-secondary transition-colors"><<i class="fa fa-weibo text-xl"></</i></a >
                        <a href="#" class="text-primary hover:text-secondary transition-colors"><<i class="fa fa-behance text-xl"></</i></a >
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer class="bg-primary text-white py-6">
        <div class="container mx-auto px-4 text-center">
            <p>&copy; 2025 城市与海岸摄影集. 保留所有权利.</p >
            <p class="mt-2 text-sm opacity-80">设计与开发：为摄影作品打造的展示平台</p >
        </div>
    </footer>

    <script>
        // 简单的图片点击放大功能（可根据需求扩展为模态框）
        document.querySelectorAll('.image-grid img').forEach(img => {
            img.addEventListener('click', function() {
                alert('点击查看大图功能可在此处扩展');
            });
        });
    </script>
</body>
</html>
