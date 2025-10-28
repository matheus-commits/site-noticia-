# site-noticia- <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notícias do Dia</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #1e90ff;
            color: white;
            text-align: center;
            padding: 20px 0;
        }
        nav {
            background-color: #333;
            color: white;
            display: flex;
            justify-content: center;
            gap: 15px;
            padding: 10px;
        }
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            text-decoration: underline;
        }
        main {
            padding: 20px;
            max-width: 900px;
            margin: auto;
        }
        .noticia {
            background: white;
            margin-bottom: 20px;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .noticia img {
            width: 100%;
            border-radius: 8px;
        }
        .noticia h2 {
            color: #1e90ff;
        }
        footer {
            background-color: #1e90ff;
            color: white;
            text-align: center;
            padding: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Notícias do Dia</h1>
        <p>As principais manchetes em um só lugar</p>
    </header>

    <nav>
        <a href="#">Início</a>
        <a href="#">Política</a>
        <a href="#">Esportes</a>
        <a href="#">Tecnologia</a>
        <a href="#">Contato</a>
    </nav>

    <main id="conteudo">
        <!-- Notícias serão inseridas via JavaScript -->
    </main>

    <footer>
        &copy; 2025 Notícias do Dia - Todos os direitos reservados.
    </footer>

    <script>
        const noticias = [
            {
                titulo: "Eleições 2025: Novas regras entram em vigor",
                imagem: "https://picsum.photos/900/400?random=1",
                texto: "As mudanças na legislação eleitoral prometem impactar o cenário político nacional."
            },
            {
                titulo: "Novo celular dobrável é lançado no Brasil",
                imagem: "https://picsum.photos/900/400?random=2",
                texto: "A tecnologia de telas flexíveis continua evoluindo, com novos modelos chegando ao mercado."
            },
            {
                titulo: "Brasil vence campeonato mundial de futebol",
                imagem: "https://picsum.photos/900/400?random=3",
                texto: "Em uma partida emocionante, o Brasil conquista o título mundial após 20 anos."
            }
        ];

        const conteudo = document.getElementById("conteudo");

        noticias.forEach(noticia => {
            const div = document.createElement("div");
            div.className = "noticia";
            div.innerHTML = `
                <img src="${noticia.imagem}" alt="${noticia.titulo}">
                <h2>${noticia.titulo
