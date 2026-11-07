# Gi-Papelaria1
Papelaria e designers em geral
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GI Papelaria | Qualidade e Personalização</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            font-weight: bold;
        }

        :root {
            --cor-principal: #D4AF37;
            --cor-secundaria: #000000;
            --cor-fundo: #F5F0E1;
            --cor-card: #FFFFFF;
            --cor-destaque: #C9A227;
        }

        body {
            background-color: var(--cor-fundo);
            color: var(--cor-secundaria);
            line-height: 1.6;
        }

        header {
            background: linear-gradient(135deg, #000000 0%, #1a1a1a 50%, #000000 100%);
            color: #FFFFFF;
            padding: 2.5rem 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.1) 0%, transparent 70%);
            animation: brilho 8s infinite linear;
        }

        @keyframes brilho {
            0% { transform: translate(0, 0); }
            50% { transform: translate(20%, 20%); }
            100% { transform: translate(0, 0); }
        }

        .logo {
            width: 160px;
            height: 160px;
            background: radial-gradient(circle, #D4AF37 0%, #B8860B 50%, #8B6914 100%);
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border: 4px solid #FFFFFF;
            box-shadow: 0 0 25px rgba(212, 175, 55, 0.6), 0 0 50px rgba(212, 175, 55, 0.3);
            margin: 0 auto 1rem;
            position: relative;
            z-index: 1;
        }

        .logo-texto {
            font-size: 2.2rem;
            color: #000000;
            letter-spacing: 3px;
            text-shadow: 1px 1px 3px rgba(255, 255, 255, 0.3);
        }

        .logo-sub {
            font-size: 0.75rem;
            color: #FFFFFF;
            margin-top: 4px;
            letter-spacing: 2px;
        }

        h1 {
            font-size: 2.8rem;
            text-shadow: 3px 3px 8px rgba(212, 175, 55, 0.5);
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
        }

        .slogan {
            font-size: 1.2rem;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }

        nav {
            background-color: #FFFFFF;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            padding: 1rem;
        }

        nav ul li {
            margin: 0.5rem 1.2rem;
        }

        nav ul li a {
            text-decoration: none;
            color: #000000;
            font-weight: bold;
            transition: all 0.3s;
            position: relative;
        }

        nav ul li a::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--cor-principal);
            transition: width 0.3s;
        }

        nav ul li a:hover {
            color: var(--cor-principal);
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        section {
            padding: 3.5rem 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 2.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 3px solid var(--cor-principal);
            display: inline-block;
            width: 100%;
        }

        .hero {
            background: linear-gradient(135deg, #000000 0%, #1a1a1a 100%);
            color: #FFFFFF;
            padding: 4rem 2rem;
            border-radius: 20px;
            margin-bottom: 3rem;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 30% 50%, rgba(212, 175, 55, 0.2) 0%, transparent 50%);
        }

        .hero-conteudo {
            position: relative;
            z-index: 1;
            text-align: center;
        }

        .hero h2 {
            font-size: 2.2rem;
            margin-bottom: 1rem;
            color: var(--cor-principal);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            opacity: 0.9;
        }

        .servicos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .servico-card {
            background-color: var(--cor-card);
            border-radius: 15px;
            padding: 2rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            border-top: 5px solid var(--cor-principal);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .servico-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.05) 0%, transparent 100%);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .servico-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.15);
        }

        .servico-card:hover::before {
            opacity: 1;
        }

        .servico-card h3 {
            margin-bottom: 1rem;
            font-size: 1.3rem;
            color: var(--cor-principal);
        }

        .processo-passos {
            display: flex;
            flex-direction: column;
            gap: 2rem;
            margin-top: 2rem;
        }

        .passo {
            display: flex;
            gap: 1.5rem;
            align-items: flex-start;
            background-color: var(--cor-card);
            padding: 1.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: all 0.3s;
        }

        .passo:hover {
            transform: translateX(5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .passo-numero {
            background: linear-gradient(135deg, var(--cor-principal) 0%, var(--cor-destaque) 100%);
            color: #000000;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            font-size: 1.3rem;
            box-shadow: 0 4px 10px rgba(212, 175, 55, 0.4);
        }

        .passo-conteudo h4 {
            margin-bottom: 0.5rem;
            color: var(--cor-principal);
        }

        .contato {
            text-align: center;
        }

        .endereco-box {
            background: linear-gradient(135deg, #E8E0CC 0%, #F5F0E1 100%);
            padding: 2.5rem;
            border-radius: 15px;
            border-left: 5px solid var(--cor-principal);
            max-width: 600px;
            margin: 0 auto;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .whatsapp-btn {
            display: inline-block;
            background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
            color: #FFFFFF;
            padding: 15px 30px;
            border-radius: 10px;
            text-decoration: none;
            margin-top: 1.5rem;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3);
        }

        .whatsapp-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.4);
        }

        footer {
            background-color: #000000;
            color: #FFFFFF;
            text-align: center;
            padding: 2.5rem;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            .passo {
                flex-direction: column;
                text-align: center;
            }

            .hero h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <span class="logo-texto">GI</span>
            <span class="logo-sub">PAPELARIA</span>
        </div>
        <h1>GI PAPELARIA</h1>
        <p class="slogan">Papelaria • Personalização • Lembrancinhas — Tudo com carinho e qualidade!</p>
    </header>

    <nav>
        <ul>
            <li><a href="#inicio">Início</a></li>
            <li><a href="#sobre">Sobre Nós</a></li>
            <li><a href="#servicos">Nossos Serviços</a></li>
            <li><a href="#processo">Como Funciona</a></li>
            <li><a href="#contato">Onde Estamos</a></li>
        </ul>
    </nav>

    <section id="inicio">
        <div class="hero">
            <div class="hero-conteudo">
                <h2>Bem-vindo à GI Papelaria!</h2>
                <p>Somos a solução completa para tudo que você precisa em papelaria e personalização. Reunimos em um só lugar qualidade, dedicação e aquele atendimento especial que você merece!</p>
            </div>
        </div>
    </section>

    <section id="sobre">
        <h2 class="section-title">Sobre a GI Papelaria</h2>
        <div style="max-width: 800px; margin: 0 auto; text-align: center;">
            <p>
                A GI Papelaria nasceu para oferecer muito mais do que produtos — oferecemos soluções criativas 
                e feitas com atenção aos detalhes. Tudo o que você precisa está aqui: papelaria completa, 
                plastificação, encadernação personalizada, adesivos à prova d'água, estampas em canecas 
                e lembrancinhas para todos os momentos!
            </p>
            <br>
            <p>
                Trabalhamos com materiais selecionados e todo o carinho que seu pedido merece. 
                Do primeiro atendimento à entrega, cada etapa é pensada para você ficar satisfeito!
            </p>
        </div>
    </section>

    <section id="servicos">
        <h2 class="section-title">Nossos Serviços</h2>
        <div class="servicos-grid">
            <div class="servico-card">
                <h3>📝 Papelaria em Geral</h3>
                <p>Variedade completa para escola, escritório e uso pessoal. Cadernos, canetas, papéis, pastas e muito mais com qualidade garantida!</p>
            </div>

            <div class="servico-card">
                <h3>📄 Plastificação</h3>
                <p>Proteja seus documentos, cartões, trabalhos e lembranças. Deixe tudo conservado, limpo e durável por muito mais tempo!</p>
            </div>

            <div class="servico-card">
                <h3>📓 Encadernação Personalizada</h3>
                <p>Cadernos, agendas, apostilas e blocos com a sua cara! Escolha capa, cores e acabamentos — fazemos do jeitinho que você quer!</p>
            </div>

            <div class="servico-card">
                <h3>💧 Adesivos à Prova d'Água</h3>
                <p>Resistentes à água, sol e umidade! Ideais para produtos, lembrancinhas, embalagens e decoração. Não desbotam e duram muito!</p>
            </div>

            <div class="servico-card">
                <h3>☕ Estampa Estilizada de Canecas</h3>
                <p>Sua arte, frase, foto ou desenho aplicada com qualidade. Presente especial que acompanha você no dia a dia!</p>
            </div>

            <div class="servico-card">
                <h3>🎁 Lembrancinhas em Geral</h3>
                <p>Para festas, eventos, casamentos, aniversários e qualquer ocasião! Peças únicas e cheias de carinho para surpreender!</p>
            </div>
        </div>
    </section>

    <section id="processo">
        <h2 class="section-title">Nosso Processo — Passo a Passo</h2>
        <p style="text-align: center; margin-bottom: 1rem;">Veja como é simples ter um produto especial feito para você:</p>
        
        <div class="processo-passos">
            <div class="passo">
                <div class="passo-numero">1</div>
                <div class="passo-conteudo">
                    <h4>Conversa e Ideias</h4>
                    <p>Você nos conta o que precisa! Ouvimos com atenção suas ideias, preferências, cores, textos, quantidades e todos os detalhes. Tiramos todas as suas dúvidas!</p>
                </div>
            </div>

            <div class="passo">
                <div class="passo-numero">2</div>
                <div class="passo-conteudo">
                    <h4>Criação e Aprovação</h4>
                    <p>Preparamos o projeto e apresentamos para você. Ajustamos quantas vezes forem necessárias. Só começamos a produção quando você aprovar — é assim que garantimos que ficará perfeito!</p>
                </div>
            </div>

            <div class="passo">
                <div class="passo-numero">3</div>
                <div class="passo-conteudo">
                    <h4>Produção com Cuidado</h4>
                    <p>Colocamos a mão na massa! Selecionamos os melhores materiais e produzimos cada peça com atenção. Plastificação, encadernação, impressão, estampas — tudo feito com carinho e qualidade!</p>
                </div>
            </div>

            <div class="passo">
                <div class="passo-numero">4</div>
                <div class="passo-conteudo">
                    <h4>Conferência e Entrega</h4>
                    <p>Antes de te chamar, conferimos cada detalhe. Acabamento, limpeza e qualidade garantidos! Tudo certo? É só você vir retirar e levar seus produtos com um sorriso! 😊</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contato" class="contato">
        <h2 class="section-title">Onde Estamos</h2>
        <p style="margin-bottom: 1.5rem; font-size: 1.1rem;">Venha nos conhecer! Estamos esperando por você!</p>
        
  <div class="endereco-box">
            <p>📍 GI PAPELARIA</p>
            <p style="font-size: 1.2rem; margin: 1rem 0;">
                Rua Santo Ângelo N°65<br>
                Recreio Boa Vista/SJC-SP
            </p>
            <p>📞 Telefone e WhatsApp:</p>
            <p style="font-size: 1.3rem; margin: 0.5rem 0;">12 996590844</p>
            
            <a href="https://wa.me/5512996590844" target="_blank" class="whatsapp-btn">💬 Falar pelo WhatsApp</a>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <p>© 2026 GI Papelaria — Todos os direitos reservados</p>
        <p style="margin-top: 0.5rem; font-size: 0.9rem; opacity: 0.8;">
            Rua Santo Ângelo N°65, Recreio Boa Vista/SJC-SP | Tel: 12 996590844
        </p>
    </footer>
</body>
</html>
