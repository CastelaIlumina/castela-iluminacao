<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Castela Iluminação - Iluminando seus eventos</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .tab-content {
            display: none;
        }
        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }
        .gallery-overlay {
            transition: opacity 0.3s ease;
        }
    </style>
</head>
<body class="min-h-screen bg-gray-100">
    <!-- Header -->
    <header class="bg-yellow-600 text-white shadow-lg">
        <div class="container mx-auto px-4 py-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h1 class="text-3xl font-bold">Castela Iluminação</h1>
                    <p class="text-yellow-100">Iluminando seus eventos</p>
                </div>
                <nav class="flex flex-wrap justify-center gap-2 md:gap-4">
                    <button 
                        onclick="showTab('home')" 
                        class="px-3 py-2 rounded-lg flex items-center bg-yellow-700"
                    >
                        <i class="fas fa-home mr-2"></i> Início
                    </button>
                    <button 
                        onclick="showTab('about')" 
                        class="px-3 py-2 rounded-lg flex items-center hover:bg-yellow-500"
                    >
                        <i class="fas fa-info-circle mr-2"></i> Quem Somos
                    </button>
                    <button 
                        onclick="showTab('gallery')" 
                        class="px-3 py-2 rounded-lg flex items-center hover:bg-yellow-500"
                    >
                        <i class="fas fa-images mr-2"></i> Eventos
                    </button>
                    <button 
                        onclick="showTab('contact')" 
                        class="px-3 py-2 rounded-lg flex items-center hover:bg-yellow-500"
                    >
                        <i class="fas fa-envelope mr-2"></i> Contato
                    </button>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-12">
        <!-- Home Tab -->
        <section id="home" class="tab-content active">
            <div class="bg-white rounded-xl shadow-md overflow-hidden mb-16">
                <div class="md:flex">
                    <div class="md:w-1/2">
                        <img 
                            src="https://images.unsplash.com/photo-1511795409834-ef04bbd61622?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Show com iluminação espetacular" 
                            class="w-full h-full object-cover"
                            loading="lazy"
                        />
                    </div>
                    <div class="p-8 md:w-1/2">
                        <h2 class="text-2xl font-bold text-gray-800 mb-4">Transformando eventos com luz</h2>
                        <p class="text-gray-600 mb-6">
                            A Castela Iluminação traz magia e atmosfera única para seus eventos através de soluções 
                            personalizadas em iluminação cênica. Desde casamentos até grandes shows, criamos a 
                            ambiência perfeita para cada ocasião.
                        </p>
                        <button 
                            onclick="showTab('about')"
                            class="bg-yellow-600 hover:bg-yellow-700 text-white px-6 py-3 rounded-lg transition-colors"
                        >
                            Conheça nossa história
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- About Tab -->
        <section id="about" class="tab-content">
            <div class="bg-white rounded-xl shadow-md p-8 mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-6">Quem Somos</h2>
                <div class="prose max-w-none text-gray-700">
                    <p class="mb-4">
                        Fundada em 2010, a <strong>Castela Iluminação</strong> nasceu da paixão por transformar espaços 
                        através da luz. Somos especialistas em iluminação cênica para eventos dos mais variados tipos.
                    </p>
                    <p class="mb-4">
                        Nossa equipe é composta por profissionais experientes que combinam conhecimento técnico 
                        com sensibilidade artística para criar ambientes únicos e memoráveis.
                    </p>
                    <h3 class="text-xl font-semibold text-gray-800 mt-8 mb-4">Nossa Missão</h3>
                    <p class="mb-4">
                        Iluminar e transformar eventos em experiências visuais inesquecíveis, superando as 
                        expectativas de nossos clientes com soluções criativas e técnicas inovadoras.
                    </p>
                    <h3 class="text-xl font-semibold text-gray-800 mt-8 mb-4">Nossos Valores</h3>
                    <ul class="list-disc pl-5 space-y-2">
                        <li>Excelência técnica e artística</li>
                        <li>Compromisso com a satisfação do cliente</li>
                        <li>Inovação constante em equipamentos e técnicas</li>
                        <li>Sustentabilidade ambiental</li>
                        <li>Segurança em todos os projetos</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Gallery Tab -->
        <section id="gallery" class="tab-content">
            <div class="bg-white rounded-xl shadow-md p-8 mb-16">
                <div class="flex justify-between items-center mb-8">
                    <h2 class="text-3xl font-bold text-gray-800">Nossos Eventos</h2>
                    <button 
                        onclick="alert('Funcionalidade de upload seria implementada com integração a um serviço de armazenamento')"
                        class="bg-yellow-600 hover:bg-yellow-700 text-white px-4 py-2 rounded-lg transition-colors"
                    >
                        Adicionar Fotos
                    </button>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div class="group relative overflow-hidden rounded-lg shadow-md hover:shadow-xl transition-shadow">
                        <img 
                            src="https://images.unsplash.com/photo-1514525253161-7a46d19cd819?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Evento de casamento com iluminação elegante" 
                            class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
                            loading="lazy"
                        />
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4 gallery-overlay">
                            <p class="text-white">Casamento com iluminação elegante</p>
                        </div>
                    </div>
                    
                    <div class="group relative overflow-hidden rounded-lg shadow-md hover:shadow-xl transition-shadow">
                        <img 
                            src="https://images.unsplash.com/photo-1492684223066-81342ee5ff30?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Show com efeitos de luz coloridos" 
                            class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
                            loading="lazy"
                        />
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4 gallery-overlay">
                            <p class="text-white">Show com efeitos de luz</p>
                        </div>
                    </div>
                    
                    <div class="group relative overflow-hidden rounded-lg shadow-md hover:shadow-xl transition-shadow">
                        <img 
                            src="https://images.unsplash.com/photo-1519671482749-fd09be7ccebf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Evento corporativo com iluminação moderna" 
                            class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
                            loading="lazy"
                        />
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4 gallery-overlay">
                            <p class="text-white">Evento corporativo</p>
                        </div>
                    </div>
                    
                    <div class="group relative overflow-hidden rounded-lg shadow-md hover:shadow-xl transition-shadow">
                        <img 
                            src="https://images.unsplash.com/photo-1496337589254-7f1e249be1b5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Festa temática com efeitos especiais" 
                            class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
                            loading="lazy"
                        />
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4 gallery-overlay">
                            <p class="text-white">Festa temática</p>
                        </div>
                    </div>
                    
                    <div class="group relative overflow-hidden rounded-lg shadow-md hover:shadow-xl transition-shadow">
                        <img 
                            src="https://images.unsplash.com/photo-1540575467063-178a50c2df87?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Palco com iluminação profissional" 
                            class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
                            loading="lazy"
                        />
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4 gallery-overlay">
                            <p class="text-white">Palco profissional</p>
                        </div>
                    </div>
                    
                    <div class="group relative overflow-hidden rounded-lg shadow-md hover:shadow-xl transition-shadow">
                        <img 
                            src="https://images.unsplash.com/photo-1511578314322-379afb476865?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                            alt="Evento social com atmosfera iluminada" 
                            class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-105"
                            loading="lazy"
                        />
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end p-4 gallery-overlay">
                            <p class="text-white">Evento social</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Tab -->
        <section id="contact" class="tab-content">
            <div class="bg-white rounded-xl shadow-md overflow-hidden mb-16">
                <div class="md:flex">
                    <div class="md:w-1/2 p-8">
                        <h2 class="text-3xl font-bold text-gray-800 mb-6">Entre em Contato</h2>
                        <form class="space-y-4">
                            <div>
                                <label for="name" class="block text-gray-700 mb-2">Nome</label>
                                <input 
                                    type="text" 
                                    id="name" 
                                    class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500"
                                    placeholder="Seu nome completo"
                                />
                            </div>
                            <div>
                                <label for="email" class="block text-gray-700 mb-2">E-mail</label>
                                <input 
                                    type="email" 
                                    id="email" 
                                    class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500"
                                    placeholder="seu@email.com"
                                />
                            </div>
                            <div>
                                <label for="message" class="block text-gray-700 mb-2">Mensagem</label>
                                <textarea 
                                    id="message" 
                                    rows="4" 
                                    class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-yellow-500 focus:border-yellow-500"
                                    placeholder="Descreva seu evento e necessidades de iluminação"
                                ></textarea>
                            </div>
                            <button 
                                type="button" 
                                onclick="alert('Mensagem enviada com sucesso! (em produção isso enviaria para o servidor)')"
                                class="bg-yellow-600 hover:bg-yellow-700 text-white px-6 py-3 rounded-lg transition-colors w-full"
                            >
                                Enviar Mensagem
                            </button>
                        </form>
                    </div>
                    <div class="md:w-1/2 bg-gray-50 p-8">
                        <h3 class="text-xl font-semibold text-gray-800 mb-4">Informações de Contato</h3>
                        <div class="space-y-4">
                            <div class="flex items-start">
                                <i class="fas fa-phone text-yellow-600 mt-1 mr-3"></i>
                                <div>
                                    <p class="font-medium text-gray-800">Telefone</p>
                                    <p class="text-gray-600">(XX) XXXX-XXXX</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fas fa-envelope text-yellow-600 mt-1 mr-3"></i>
                                <div>
                                    <p class="font-medium text-gray-800">E-mail</p>
                                    <p class="text-gray-600">contato@castelailuminacao.com.br</p>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <i class="fas fa-map-marker-alt text-yellow-600 mt-1 mr-3"></i>
                                <div>
                                    <p class="font-medium text-gray-800">Endereço</p>
                                    <p class="text-gray-600">Rua Exemplo, 123 - Centro, Cidade/UF</p>
                                </div>
                            </div>
                        </div>
                        
                        <h3 class="text-xl font-semibold text-gray-800 mt-8 mb-4">Redes Sociais</h3>
                        <div class="flex space-x-4">
                            <a href="#" class="text-gray-700 hover:text-yellow-600 transition-colors">
                                <i class="fab fa-instagram text-2xl"></i>
                            </a>
                            <a href="#" class="text-gray-700 hover:text-yellow-600 transition-colors">
                                <i class="fab fa-facebook text-2xl"></i>
                            </a>
                        </div>
                        
                        <div class="mt-8">
                            <iframe 
                                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3657.0754267452926!2d-46.6534265844076!3d-23.565734367638952!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce59c8da0aa315%3A0xd59f9431f2c9776a!2sAv.%20Paulista%2C%20S%C3%A3o%20Paulo%20-%20SP!5e0!3m2!1spt-BR!2sbr!4v1629830000000!5m2!1spt-BR!2sbr" 
                                width="100%" 
                                height="250" 
                                style="border:0;" 
                                allowfullscreen="" 
                                loading="lazy"
                                class="rounded-lg shadow-sm"
                            ></iframe>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-800 text-white py-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h3 class="text-xl font-bold mb-2">Castela Iluminação</h3>
                    <p class="text-gray-400">Iluminando seus eventos desde 2010</p>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">
                        <i class="fab fa-instagram text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">
                        <i class="fab fa-facebook text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">
                        <i class="fas fa-envelope text-xl"></i>
                    </a>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-6 pt-6 text-center text-gray-400">
                <p>&copy; <script>document.write(new Date().getFullYear())</script> Castela Iluminação. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        function showTab(tabId) {
            // Esconde todas as abas
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Mostra a aba selecionada
            document.getElementById(tabId).classList.add('active');
            
            // Atualiza o botão ativo
            document.querySelectorAll('nav button').forEach(button => {
                button.classList.remove('bg-yellow-700');
                button.classList.add('hover:bg-yellow-500');
            });
            
            event.currentTarget.classList.add('bg-yellow-700');
            event.currentTarget.classList.remove('hover:bg-yellow-500');
        }
        
        function handleImageUpload() {
            // Em produção, isso seria substituído por upload real
            alert('Funcionalidade de upload seria implementada com integração a um serviço de armazenamento');
        }
    </script>
</body>
</html>
