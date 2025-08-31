# p-bravo
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bravo Clothing - Indian Fashion</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@300;400;700&display=swap');
        
        body {
            font-family: 'Lato', sans-serif;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }
        
        .hero-section {
            background: linear-gradient(135deg, #FF9933 0%, #FFFFFF 50%, #138808 100%);
            min-height: 100vh;
        }
        
        .logo-text {
            font-family: 'Playfair Display', serif;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.3);
        }
        
        .nav-link {
            position: relative;
            transition: all 0.3s ease;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 50%;
            background: #FF9933;
            transition: all 0.3s ease;
            transform: translateX(-50%);
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        .product-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        .page {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }
        
        .page.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .indian-flag {
            background: linear-gradient(to right, #FF9933 33.3%, #FFFFFF 33.3%, #FFFFFF 66.6%, #138808 66.6%);
        }
    </style>
</head>
<body class="min-h-screen">
    <!-- Navigation -->
    <nav class="bg-white shadow-lg fixed w-full top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <div class="text-3xl font-bold text-orange-600 logo-text">BRAVO</div>
                </div>
                <div class="flex space-x-8 items-center">
                    <a href="#" class="nav-link text-gray-700 hover:text-orange-600 font-medium" onclick="showPage('home')">Home</a>
                    <a href="#" class="nav-link text-gray-700 hover:text-orange-600 font-medium" onclick="showPage('contact')">Contact</a>
                    <div class="flex items-center space-x-4">
                        <a href="#" class="text-gray-600 hover:text-orange-600">
                            <i class="fas fa-shopping-bag"></i>
                        </a>
                        <a href="#" class="text-gray-600 hover:text-orange-600">
                            <i class="fas fa-user"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- Home Page -->
    <div id="home-page" class="page active">
        <!-- Hero Section -->
        <section class="hero-section pt-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
                <div class="text-center">
                    <div class="mb-8">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/101a2765-e534-492d-8ce7-5483fc99dce3.png" alt="Bravo Clothing Company Logo - Elegant Indian fashion brand with saffron background and white Devanagari script inspired text" class="mx-auto w-80 h-40 object-contain" onerror="this.style.backgroundColor='#FF9933'; this.style.color='white'; this.textContent='BRAVO INDIA'">
                    </div>
                    <h1 class="text-5xl md:text-7xl font-bold text-white logo-text mb-6">शानदार भारतीय शैली</h1>
                    <p class="text-xl md:text-2xl text-white mb-8 max-w-3xl mx-auto">
                        Discover the authentic Indian style that combines traditional heritage with contemporary elegance
                    </p>
                    <button class="bg-white text-orange-600 px-8 py-4 rounded-full font-semibold text-lg hover:bg-gray-100 transition duration-300 transform hover:scale-105">
                        Explore Collection <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
        </section>

        <!-- Featured Products -->
        <section class="py-20 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-4xl font-bold text-gray-800 mb-4">Featured Collection</h2>
                    <p class="text-xl text-gray-600">Handcrafted with Indian artistry and precision</p>
                    <div class="w-24 h-1 bg-orange-600 mx-auto mt-4"></div>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Product 1 -->
                    <div class="product-card bg-gray-50 rounded-lg overflow-hidden">
                        <div class="relative">
                            <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/69798276-cbf7-4d90-ac78-1fbd70e560d8.png" alt="Elegant Indian traditional outfits including sarees and sherwanis displayed in vibrant colors with intricate embroidery" class="w-full h-80 object-cover" onerror="this.style.backgroundColor='#FF9933'">
                            <div class="absolute top-4 right-4 bg-orange-600 text-white px-3 py-1 rounded-full text-sm">
                                New
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-semibold text-gray-800 mb-2">Delhi Heritage Collection</h3>
                            <p class="text-gray-600 mb-4">Handcrafted with traditional Indian fabrics and embroidery</p>
                            <div class="flex justify-between items-center">
                                <span class="text-2xl font-bold text-orange-600">₹5,999</span>
                                <button class="bg-orange-600 text-white px-4 py-2 rounded hover:bg-orange-700 transition">
                                    Add to Cart
                                </button>
                            </div>
                        </div>
                    </div>

                    <!-- Product 2 -->
                    <div class="product-card bg-gray-50 rounded-lg overflow-hidden">
                        <div class="relative">
                            <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/cf8295d0-6b6e-446e-80df-acb4e51a7edc.png" alt="Traditional Indian jewelry and accessories including bangles, necklaces and turbans in gold and silver tones" class="w-full h-80 object-cover" onerror="this.style.backgroundColor='#FFFFFF'">
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-semibold text-gray-800 mb-2">Jaipur Jewelry Line</h3>
                            <p class="text-gray-600 mb-4">Authentic Indian handcrafted accessories</p>
                            <div class="flex justify-between items-center">
                                <span class="text-2xl font-bold text-orange-600">₹2,499</span>
                                <button class="bg-orange-600 text-white px-4 py-2 rounded hover:bg-orange-700 transition">
                                    Add to Cart
                                </button>
                            </div>
                        </div>
                    </div>

                    <!-- Product 3 -->
                    <div class="product-card bg-gray-50 rounded-lg overflow-hidden">
                        <div class="relative">
                            <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/6ccf08b9-7312-4519-ad2c-196d0d2d5e54.png" alt="Modern Indian fusion wear combining traditional patterns with contemporary silhouettes in earthy tones" class="w-full h-80 object-cover" onerror="this.style.backgroundColor='#138808'">
                            <div class="absolute top-4 left-4 bg-green-600 text-white px-3 py-1 rounded-full text-sm">
                                Sale
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-semibold text-gray-800 mb-2">Mumbai Fusion Line</h3>
                            <p class="text-gray-600 mb-4">Traditional elegance meets modern comfort</p>
                            <div class="flex justify-between items-center">
                                <span class="text-2xl font-bold text-orange-600">₹3,299</span>
                                <button class="bg-orange-600 text-white px-4 py-2 rounded hover:bg-orange-700 transition">
                                    Add to Cart
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Indian Heritage -->
        <section class="py-20 bg-gray-100">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div>
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/bbb7d480-21fc-4d90-87af-489aa10e4486.png" alt="Indian artisans working with traditional handicrafts including block printing, embroidery and weaving techniques" class="rounded-lg shadow-xl w-full" onerror="this.style.backgroundColor='#FF9933'">
                    </div>
                    <div>
                        <h2 class="text-4xl font-bold text-gray-800 mb-6">Authentic Indian Craftsmanship</h2>
                        <p class="text-lg text-gray-600 mb-6">
                            For generations, Bravo Clothing has celebrated Indian artistry. 
                            Our garments are crafted by skilled artisans across India, using traditional 
                            techniques that have been perfected over centuries.
                        </p>
                        <div class="space-y-4">
                            <div class="flex items-center">
                                <div class="w-12 h-12 bg-orange-600 rounded-full flex items-center justify-center mr-4">
                                    <i class="fas fa-award text-white text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold text-gray-800">Premium Materials</h4>
                                    <p class="text-gray-600">Finest Indian fabrics and textiles</p>
                                </div>
                            </div>
                            <div class="flex items-center">
                                <div class="w-12 h-12 bg-green-600 rounded-full flex items-center justify-center mr-4">
                                    <i class="fas fa-hands text-white text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold text-gray-800">Handcrafted Quality</h4>
                                    <p class="text-gray-600">Every piece tells a story of tradition</p>
                                </div>
                            </div>
                            <div class="flex items-center">
                                <div class="w-12 h-12 bg-white rounded-full flex items-center justify-center mr-4 border-2 border-orange-600">
                                    <i class="fas fa-globe-asia text-orange-600 text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold text-gray-800">Worldwide Shipping</h4>
                                    <p class="text-gray-600">Bringing India to your doorstep</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Newsletter -->
        <section class="py-16 indian-flag">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Join the Bravo Family</h2>
                <p class="text-lg text-gray-600 mb-8">Get exclusive offers and style inspirations from India</p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <input type="email" placeholder="Your email address" class="px-6 py-3 rounded-full border-0 focus:ring-2 focus:ring-orange-600 w-full sm:w-96">
                    <button class="bg-orange-600 text-white px-8 py-3 rounded-full font-semibold hover:bg-orange-700 transition">
                        Subscribe
                    </button>
                </div>
            </div>
        </section>
    </div>

    <!-- Contact Page -->
    <div id="contact-page" class="page">
        <div class="pt-20 pb-16">
            <div class="max-w-7xl mx-auto px-极 sm:px-6 lg:px-8">
                <!-- Header -->
                <极 class="text-center mb-16">
                    <h1 class="text-4xl font-bold text-gray-800 mb-4">Contact Bravo Clothing</h1>
                    <p class="text-xl text-gray-600">We'd love to hear from you! Get in touch with our team.</p>
                    <div class="w-24 h-1 bg-orange-600 mx-auto mt-4"></div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                    <!-- Contact Form -->
                    <div class="bg-white rounded-lg shadow-lg p-8">
                        <h2 class="text-2极 font-bold text-gray-800 mb-6">Send us a Message</h2>
                        <form class="space-y-6">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label class="block text-sm font-medium text-gray-700 mb-2">First Name</label>
                                    <input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent">
                                </div>
                                <div>
                                    <label class="block text-sm font-medium text-gray-700极-2">Last Name</label>
                                    <input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent">
                                </div>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
                                <input type="email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Subject</label>
                                <input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Message</label>
                                <textarea rows="5" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent"></textarea>
                            </极>
                            <button type="submit" class="w-full bg-orange-600 text-white py-3 px-6 rounded-lg font-semibold hover:bg-orange-700 transition">
                                Send Message <i class="fas fa-paper-plane ml-2"></i>
                            </button>
                        </form>
                    </div>

                    <!-- Contact Info -->
                    <div class="space-y-8">
                        <div class="bg-white rounded-lg shadow-lg p-8">
                            <h2 class="text-2xl font-bold text-gray-800 mb-6">Contact Information</h2>
                            <div class="space-y-4">
                                <div class="flex items-center">
                                    <div class="w-12 h-12 bg-orange-600 rounded-full flex items-center justify-center mr-4">
                                        <i class="fas fa-map-marker-alt text-white"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-semibold text-gray-800">Headquarters</h4>
                                        <p class="text-gray-600">Connaught Place, New Delhi, India 110001</p>
                                    </div>
                                </div>
                                <div class="flex items-center">
                                    <div class="w-12 h-12 bg-green-600 rounded-full flex items-center justify-center mr-4">
                                        <i class="fas fa-phone text-white"></极>
                                    </div>
                                    <div>
                                        <h4 class="font-semibold text-gray-800">Phone</h4>
                                        <p class="text-gray-600">+91 11 2345 6789</p>
                                    </div>
                                </div>
                                <div class="flex items-center">
                                    <div class="w-12 h-12 bg-gray-600 rounded-full flex items-center justify-center mr-4">
                                        <i class="fas fa-envelope text-white"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-semibold text-gray-800">Email</h4>
                                        <p class="text-gray-600">info@bravoclothing.in</p>
                                    </div>
                                </div>
                                <div class="flex items-center">
                                    <div class="w-12 h-12 bg-blue-600 rounded-full flex items-center justify-center mr-4">
                                        极 class="fas fa-clock text-white"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-semibold text-gray-800">Business Hours</h4>
                                        <p class="text-gray-600">Mon-Sat: 10:00 AM - 8:00 PM IST</p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Social Media -->
                        <div class="bg-white rounded-lg shadow-lg p-8">
                            <h2 class="text-2xl font-bold text-gray-800 mb-6">Follow Us</h2>
                            <div class="flex space-x-4">
                                <a href="#" class="w-12 h-12 bg-gray-800 rounded-full flex items-center justify-center hover:bg-orange-600 transition">
                                    <i class="fab fa-facebook-f text-white"></i>
                                </a>
                                <a href="#" class="w-12 h-12 bg-gray-800 rounded-full flex items-center justify-center hover:bg-orange-600 transition">
                                    <i class="fab fa-instagram text-white"></i>
                                </a>
                                <a href="#" class="w-12 h-12 bg-gray-800 rounded-full flex items-center justify-center hover:bg-orange-600 transition">
                                    <i class="fab fa-twitter text-white"></i>
                                </a>
                                <a href="#" class="w-12 h-12 bg-gray-800 rounded-full flex items-center justify-center hover:bg-orange-600 transition">
                                    <i class="fab fa-youtube text-white"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="text-3xl font-bold text-orange-600 logo-text mb-4">BRAVO</div>
                    <p class="text-gray-400 mb-4">Authentic Indian fashion since 1950</p>
                    <div class="flex space极-4">
                        <i class="fab fa-cc-visa text-2xl text-gray-400"></i>
                        <i class="fab fa-cc-mastercard text-2xl text-gray-400"></i>
                        <i class="fab fa-cc-amex text-2xl text-gray-400"></i>
                        <i class="fab fa-cc-paypal text-2xl text-gray-400"></i>
                    </div>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Shop</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Men's Collection</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Women's Collection</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Accessories</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">New Arrivals</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semib极 mb-4">Company</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">About Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Our Story</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Sustainability</a></li>
                        <li><a href="#" class="text-gray-极- hover:text-white">Careers</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Support</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white">Contact Us</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Shipping Info</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Returns</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white">Size Guide</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-8 pt-8 text-center">
                <p class="text-gray-400">© 2024 Bravo Clothing. All rights reserved. Authentic Indian fashion.</p>
            </div>
        </div>
    </footer>

    <script>
        function showPage(pageId) {
            // Hide all pages
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            
            // Show the selected page
            document.getElementById(pageId + '-page').classList.add('active');
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        // Initialize page
        document.addEventListener('DOMContentLoaded', function() {
            showPage('home');
        });
    </script>
</body>
</html>

``` Login to continue using
