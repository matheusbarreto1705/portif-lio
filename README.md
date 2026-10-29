# portif-lio

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portfólio profissional de desenvolvedor web.">
    <title>teteus portfólio | Desenvolvedor Web</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 90px;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #ffffff;
            color: #222222;
            line-height: 1.6;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        header {
            position: sticky;
            top: 0;
            z-index: 10;
            background: rgba(255, 255, 255, 0.96);
            border-bottom: 1px solid #eeeeee;
        }

        nav {
            max-width: 1100px;
            margin: auto;
            padding: 18px 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }

        .logo {
            font-size: 21px;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            flex-wrap: wrap;
            gap: 22px;
            list-style: none;
        }

        .nav-links a {
            color: #555555;
            font-size: 14px;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: #000000;
        }

        .container {
            width: min(100% - 40px, 1000px);
            margin: auto;
        }

        section {
            padding: 85px 0;
        }

        .hero {
            min-height: 570px;
            display: flex;
            align-items: center;
        }

        .hero-content {
            max-width: 750px;
        }

        .avatar {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            object-position: center;
            border: 4px solid #eeeeee;
            display: block;
            margin-bottom: 28px;
            background: #f4f4f4;
        }

        .eyebrow {
            color: #777777;
            font-size: 14px;
            margin-bottom: 8px;
        }

        h1 {
            font-size: clamp(36px, 6vw, 58px);
            line-height: 1.1;
            letter-spacing: -2px;
            margin-bottom: 20px;
        }

        .hero p {
            max-width: 620px;
            color: #666666;
            font-size: 17px;
            margin-bottom: 28px;
        }

        .button {
            display: inline-block;
            padding: 12px 22px;
            background: #222222;
            color: white;
            border: 1px solid #222222;
            border-radius: 8px;
            transition: 0.2s;
        }

        .button:hover {
            background: #444444;
            transform: translateY(-2px);
        }

        .button-outline {
            background: white;
            color: #222222;
            margin-left: 8px;
        }

        .button-outline:hover {
            background: #f3f3f3;
        }

        .section-title {
            font-size: 32px;
            letter-spacing: -1px;
            margin-bottom: 12px;
        }

        .section-description {
            color: #666666;
            margin-bottom: 32px;
            max-width: 650px;
        }

        .about-box {
            padding: 28px;
            border: 1px solid #eeeeee;
            border-radius: 16px;
            background: #fafafa;
        }

        .about-box p {
            color: #555555;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
        }

        .skill-item {
            padding: 13px 18px;
            border: 1px solid #e5e5e5;
            border-radius: 12px;
            background: #fafafa;
            font-size: 15px;
            transition: transform 0.2s;
        }

        .skill-item:hover {
            transform: translateY(-3px);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 22px;
        }

        .project-card {
            padding: 25px 20px;
            border: 1px solid #e8e8e8;
            border-radius: 16px;
            text-align: center;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.06);
        }

        .project-image {
            width: 125px;
            height: 125px;
            border-radius: 50%;
            object-fit: cover;
            object-position: center;
            display: block;
            margin: 0 auto 20px;
            background: #f0f0f0;
            border: 3px solid #eeeeee;
        }

        .project-card h3 {
            margin-bottom: 10px;
            font-size: 19px;
        }

        .project-card p {
            color: #666666;
            font-size: 14px;
            margin-bottom: 18px;
        }

        .tag {
            display: inline-block;
            font-size: 12px;
            padding: 5px 9px;
            background: #f2f2f2;
            border-radius: 6px;
            margin: 3px;
        }

        .contact-box {
            padding: 28px;
            background: #fafafa;
            border: 1px solid #eeeeee;
            border-radius: 16px;
        }

        .contact-box p {
            color: #555555;
            margin-bottom: 20px;
        }

        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        footer {
            border-top: 1px solid #eeeeee;
            padding: 25px 20px;
            text-align: center;
            color: #777777;
            font-size: 14px;
        }

        @media (max-width: 750px) {
            nav {
                flex-direction: column;
            }

            .nav-links {
                justify-content: center;
                gap: 14px;
            }

            .hero {
                min-height: auto;
                padding: 70px 0;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 28px;
            }

            .avatar {
                width: 155px;
                height: 155px;
            }

            .button {
                margin: 5px 5px 5px 0;
            }
        }
    </style>
</head>

<body>

    <!-- CABEÇALHO -->
    <header>
        <nav>
            <a href="#inicio" class="logo">Meu Portfólio.</a>

            <ul class="nav-links">
                <li><a href="#inicio">Início</a></li>
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#habilidades">Habilidades</a></li>
                <li><a href="#projetos">Projetos</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>

        <!-- INÍCIO -->
        <section class="hero container" id="inicio">
            <div class="hero-content">

                <img
                    src="img1"
                    alt="Minha foto de perfil"
                    class="avatar">

                <div class="eyebrow">DESENVOLVEDOR EM FORMAÇÃO</div>

                <h1>Olá! Eu sou <span>Matheus Barreto</span>.</h1>

                <p>
                    Estou aprendendo desenvolvimento web e criando projetos
                    com HTML, CSS e JavaScript. Meu objetivo é crescer na
                    área de tecnologia e conquistar uma oportunidade de estágio.
                </p>

                <a href="#projetos" class="button">Ver meus projetos</a>
                <a href="#contato" class="button button-outline">Fale comigo</a>

            </div>
        </section>

        <!-- SOBRE MIM -->
        <section id="sobre">
            <div class="container">
                <h2 class="section-title">Sobre mim</h2>

                <p class="section-description">
                    Conheça um pouco sobre mim e meus objetivos profissionais.
                </p>

                <div class="about-box">
                    <p>
                        Sou estudante de tecnologia e tenho interesse em
                        programação e desenvolvimento de sites. Estou
                        desenvolvendo minhas habilidades por meio de estudos
                        e projetos práticos. Busco aprender novas tecnologias,
                        melhorar meus conhecimentos e adquirir experiência
                        profissional na área.
                    </p>
                </div>
            </div>
        </section>

        <!-- HABILIDADES -->
        <section id="habilidades">
            <div class="container">
                <h2 class="section-title">Minhas habilidades</h2>

                <p class="section-description">
                    Tecnologias e conhecimentos que estou desenvolvendo.
                </p>

                <div class="skills-list">
                    <div class="skill-item">🌐 HTML</div>
                    <div class="skill-item">🎨 CSS</div>
                    <div class="skill-item">⚡ JavaScript</div>
                    <div class="skill-item">🛠️ Git e GitHub</div>
                </div>
            </div>
        </section>

        <!-- PROJETOS -->
        <section id="projetos">
            <div class="container">
                <h2 class="section-title">Meus projetos</h2>

                <p class="section-description">
                    Alguns exemplos de projetos que posso desenvolver
                    durante meus estudos.
                </p>

                <div class="projects-grid">

                    <article class="project-card">
                        <img
                            src="img2.jpg"
                            alt="Imagem do projeto de loja virtual"
                            class="project-image">

                        <h3>🛍️ Site de loja</h3>

                        <p>
                            Página para apresentar produtos de uma loja,
                            com organização visual e navegação simples.
                        </p>

                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                    </article>

                    <article class="project-card">
                        <img
                            src="img4.jpg"
                            alt="Imagem de projeto com JavaScript"
                            class="project-image">

                        <h3>💻 Projeto interativo</h3>

                        <p>
                            Página com funcionalidades interativas
                            desenvolvidas para praticar JavaScript.
                        </p>

                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">JavaScript</span>
                    </article>

                    <article class="project-card">
                        <img
                            src="img5.jpg"
                            alt="Imagem do projeto de portfólio"
                            class="project-image">

                        <h3>🚀 Meu portfólio</h3>

                        <p>
                            Site pessoal para apresentar minhas habilidades,
                            meus projetos e minhas informações de contato.
                        </p>

                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">JavaScript</span>
                    </article>

                </div>
            </div>
        </section>

        <!-- CONTATO -->
        <section id="contato">
            <div class="container">
                <h2 class="section-title">Vamos conversar?</h2>

                <p class="section-description">
                    Estou aberto a oportunidades de estágio e a novos
                    projetos para continuar aprendendo.
                </p>

                <div class="contact-box">
                    <p>
                        Entre em contato comigo pelos canais abaixo.
                    </p>

                    <div class="contact-links">
                        <a
                            href="mailto:seuemail@exemplo.com"
                            class="button">
                            ✉️ Enviar e-mail
                        </a>

                        <a
                            href="https://github.com/matheusbarreto1705"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="button button-outline">
                            💻 GitHub
                        </a>

                        <a
                            href="https://www.linkedin.com/"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="button button-outline">
                            🔗 LinkedIn
                        </a>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- RODAPÉ -->
    <footer>
        <p>
            © <span id="ano"></span> Seu Nome.
            Desenvolvido com HTML e CSS.
        </p>
    </footer>

    <script>
        document.getElementById("ano").textContent =
            new Date().getFullYear();
    </script>

</body>
</html>




/* CONFIGURAÇÕES GERAIS */

:root {
    --fundo: #ffffff;
    --fundo-cinza: #f7f7f7;
    --texto: #171717;
    --texto-secundario: #666666;
    --borda: #e5e5e5;
    --botao: #171717;
    --botao-texto: #ffffff;
}

:root.escuro {
    --fundo: #171717;
    --fundo-cinza: #202020;
    --texto: #f5f5f5;
    --texto-secundario: #bbbbbb;
    --borda: #393939;
    --botao: #ffffff;
    --botao-texto: #171717;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: var(--fundo);
    color: var(--texto);
    line-height: 1.7;
    transition: background 0.2s, color 0.2s;
}

a {
    color: inherit;
    text-decoration: none;
}

button,
input,
textarea {
    font: inherit;
}

button,
a,
input,
textarea {
    -webkit-tap-highlight-color: transparent;
}

a:focus-visible,
button:focus-visible,
input:focus-visible,
textarea:focus-visible {
    outline: 2px solid var(--texto);
    outline-offset: 4px;
}

.container {
    width: 90%;
    max-width: 1050px;
    margin: 0 auto;
}

.secao {
    padding: 90px 0;
}

.fundo-cinza {
    background: var(--fundo-cinza);
}

/* ACESSIBILIDADE */

.pular-conteudo {
    position: absolute;
    top: -100px;
    left: 15px;
    padding: 10px;
    background: var(--fundo);
    z-index: 100;
}

.pular-conteudo:focus {
    top: 10px;
}

/* CABEÇALHO */

header {
    background: var(--fundo);
    border-bottom: 1px solid var(--borda);
    position: sticky;
    top: 0;
    z-index: 10;
}

.navegacao {
    min-height: 75px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.logo {
    font-size: 22px;
    font-weight: bold;
    letter-spacing: -1px;
}

.menu {
    display: flex;
    list-style: none;
    gap: 25px;
}

.menu a {
    font-size: 14px;
    color: var(--texto-secundario);
    transition: color 0.2s;
}

.menu a:hover {
    color: var(--texto);
}

.menu-toggle,
.tema-toggle {
    background: transparent;
    color: var(--texto);
    border: 1px solid var(--borda);
    border-radius: 6px;
    padding: 7px 10px;
    cursor: pointer;
}

.menu-toggle {
    display: none;
}

.tema-toggle {
    font-size: 18px;
}

/* INÍCIO */

.inicio {
    min-height: 570px;
    padding-top: 100px;
    padding-bottom: 100px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
}

.avatar {
    width: 65px;
    height: 65px;
    border: 1px solid var(--borda);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    margin-bottom: 25px;
}

.saudacao {
    color: var(--texto-secundario);
    margin-bottom: 8px;
}

h1,
h2,
h3 {
    line-height: 1.25;
    letter-spacing: -0.7px;
}

h1 {
    max-width: 750px;
    font-size: clamp(32px, 5vw, 52px);
    margin-bottom: 20px;
}

h1 span {
    color: var(--texto-secundario);
}

.descricao {
    max-width: 620px;
    color: var(--texto-secundario);
    font-size: 17px;
}

.botoes {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 28px;
}

.botao {
    display: inline-block;
    padding: 11px 19px;
    border: 1px solid var(--borda);
    border-radius: 5px;
    background: var(--fundo);
    color: var(--texto);
    cursor: pointer;
    font-size: 14px;
    text-align: center;
    transition: opacity 0.2s;
}

.botao:hover {
    opacity: 0.75;
}

.botao.principal {
    background: var(--botao);
    color: var(--botao-texto);
    border-color: var(--botao);
}

.disponibilidade {
    margin-top: 25px;
    color: var(--texto-secundario);
    font-size: 13px;
}

/* TÍTULOS DAS SEÇÕES */

.subtitulo {
    color: var(--texto-secundario);
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 12px;
}

h2 {
    font-size: clamp(27px, 4vw, 36px);
    margin-bottom: 22px;
}

.texto-intro {
    color: var(--texto-secundario);
    margin-bottom: 30px;
}

/* SOBRE MIM */

.texto-sobre {
    max-width: 750px;
    color: var(--texto-secundario);
}

.texto-sobre p {
    margin-bottom: 16px;
}

/* HABILIDADES */

.habilidades-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
}

.habilidade {
    padding: 25px;
    border: 1px solid var(--borda);
    border-radius: 6px;
}

.habilidade h3 {
    font-size: 18px;
    margin-bottom: 10px;
}

.habilidade p {
    color: var(--texto-secundario);
    font-size: 14px;
}

/* PROJETOS */

.projetos-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
}

.projeto {
    padding: 25px;
    background: var(--fundo);
    border: 1px solid var(--borda);
    border-radius: 6px;
}

.numero {
    display: block;
    color: var(--texto-secundario);
    font-size: 13px;
    margin-bottom: 25px;
}

.projeto h3 {
    font-size: 18px;
    margin-bottom: 12px;
}

.projeto p {
    color: var(--texto-secundario);
    font-size: 14px;
}

.projeto .tecnologias {
    border-top: 1px solid var(--borda);
    padding-top: 12px;
    margin-top: 20px;
    font-size: 12px;
}

.aviso-projetos {
    color: var(--texto-secundario);
    font-size: 13px;
    margin-top: 22px;
}

/* FORMULÁRIO DE CONTATO */

form {
    max-width: 650px;
}

.campo {
    margin-bottom: 20px;
}

.campo label {
    display: block;
    margin-bottom: 7px;
    font-weight: bold;
    font-size: 14px;
}

.campo input,
.campo textarea {
    display: block;
    width: 100%;
    padding: 12px;
    color: var(--texto);
    background: var(--fundo);
    border: 1px solid var(--borda);
    border-radius: 5px;
}

.campo textarea {
    resize: vertical;
}

.campo input:focus,
.campo textarea:focus {
    outline: 2px solid var(--texto);
    outline-offset: 1px;
}

.campo [aria-invalid="true"] {
    border-color: #c62828;
}

.consentimento {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    margin-bottom: 8px;
    color: var(--texto-secundario);
    font-size: 13px;
}

.consentimento input {
    margin-top: 6px;
    accent-color: var(--texto);
}

.erro {
    display: block;
    min-height: 20px;
    color: #c62828;
    font-size: 12px;
}

#status-form {
    margin-top: 15px;
    font-size: 14px;
    color: var(--texto-secundario);
}

/* RODAPÉ */

footer {
    border-top: 1px solid var(--borda);
    padding: 25px 0;
}

.rodape {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
    font-size: 13px;
    color: var(--texto-secundario);
}

.rodape a {
    color: var(--texto);
}

.rodape a:hover {
    text-decoration: underline;
}

/* RESPONSIVIDADE */

@media (max-width: 750px) {
    .menu-toggle {
        display: block;
        margin-left: auto;
    }

    .menu {
        display: none;
        position: absolute;
        top: 75px;
        left: 0;
        width: 100%;
        padding: 15px 5%;
        background: var(--fundo);
        border-bottom: 1px solid var(--borda);
        flex-direction: column;
        gap: 0;
    }

    .menu.aberto {
        display: flex;
    }

    .menu a {
        display: block;
        padding: 10px 0;
    }

    .inicio {
        min-height: auto;
        padding-top: 80px;
        padding-bottom: 80px;
    }

    .projetos-grid {
        grid-template-columns: 1fr;
    }

    .secao {
        padding: 65px 0;
    }
}

@media (max-width: 480px) {
    .habilidades-grid {
        grid-template-columns: 1fr;
    }

    .rodape {
        flex-direction: column;
        align-items: flex-start;
    }

    h1 {
        font-size: 34px;
    }

    .descricao {
        font-size: 15px;
    }

    .botoes {
        width: 100%;
    }

    .botoes .botao {
        flex: 1;
    }
}

@media (prefers-reduced-motion: reduce) {
    html {
        scroll-behavior: auto;
    }

    *,
    *::before,
    *::after {
        transition: none !important;
    }
}


/* SAUDAÇÃO DINÂMICA */

const saudacao = document.getElementById("saudacao");
const hora = new Date().getHours();

if (hora < 12) {
    saudacao.textContent = "Bom dia!";
} else if (hora < 18) {
    saudacao.textContent = "Boa tarde!";
} else {
    saudacao.textContent = "Boa noite!";
}

/* MENU HAMBÚRGUER */

const menuToggle = document.querySelector(".menu-toggle");
const menu = document.getElementById("menu");

menuToggle.addEventListener("click", function () {
    const aberto = menu.classList.toggle("aberto");

    menuToggle.setAttribute("aria-expanded", aberto);
    menuToggle.setAttribute(
        "aria-label",
        aberto ? "Fechar menu" : "Abrir menu"
    );

    menuToggle.textContent = aberto ? "✕" : "☰";
});

// Fecha o menu quando um link é selecionado.
menu.querySelectorAll("a").forEach(function (link) {
    link.addEventListener("click", function () {
        menu.classList.remove("aberto");

        menuToggle.setAttribute("aria-expanded", "false");
        menuToggle.setAttribute("aria-label", "Abrir menu");
        menuToggle.textContent = "☰";
    });
});

/* MODO CLARO E ESCURO */

const temaToggle = document.querySelector(".tema-toggle");

temaToggle.addEventListener("click", function () {
    const escuro = document.documentElement.classList.toggle("escuro");

    temaToggle.setAttribute(
        "aria-label",
        escuro ? "Ativar modo claro" : "Ativar modo escuro"
    );

    temaToggle.setAttribute(
        "title",
        escuro ? "Ativar modo claro" : "Ativar modo escuro"
    );

    temaToggle.textContent = escuro ? "☀" : "◐";
});

/* ANO AUTOMÁTICO */

document.getElementById("ano").textContent =
    new Date().getFullYear();

/* VALIDAÇÃO DO FORMULÁRIO */

const formulario = document.getElementById("form-contato");

const nome = document.getElementById("nome");
const email = document.getElementById("email");
const mensagem = document.getElementById("mensagem");
const consentimento = document.getElementById("consentimento");

const statusForm = document.getElementById("status-form");

const campos = {
    nome: nome,
    email: email,
    mensagem: mensagem,
    consentimento: consentimento
};

const erros = {
    nome: document.getElementById("erro-nome"),
    email: document.getElementById("erro-email"),
    mensagem: document.getElementById("erro-mensagem"),
    consentimento: document.getElementById("erro-consentimento")
};

function mostrarErro(campo, texto) {
    erros[campo].textContent = texto;

    if (campo !== "consentimento") {
        campos[campo].setAttribute(
            "aria-invalid",
            texto ? "true" : "false"
        );
    }
}

formulario.addEventListener("submit", function (evento) {
    evento.preventDefault();

    statusForm.textContent = "";

    const nomeValor = nome.value.trim();
    const emailValor = email.value.trim();
    const mensagemValor = mensagem.value.trim();

    const validacoes = {
        nome: nomeValor.length >= 2
            ? ""
            : "Digite seu nome com pelo menos 2 caracteres.",

        email: /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(emailValor)
            ? ""
            : "Digite um endereço de e-mail válido.",

        mensagem: mensagemValor.length >= 10
            ? ""
            : "Escreva uma mensagem com pelo menos 10 caracteres.",

        consentimento: consentimento.checked
            ? ""
            : "É necessário aceitar o consentimento."
    };

    let formularioValido = true;
    let primeiroCampoComErro = null;

    Object.keys(validacoes).forEach(function (campo) {
        const erro = validacoes[campo];

        mostrarErro(campo, erro);

        if (erro) {
            formularioValido = false;

            if (!primeiroCampoComErro) {
                primeiroCampoComErro = campos[campo];
            }
        }
    });

    if (!formularioValido) {
        statusForm.textContent =
            "Confira os campos destacados e tente novamente.";

        primeiroCampoComErro.focus();
        return;
    }

    statusForm.textContent =
        "Formulário validado com sucesso! " +
        "Este modelo não envia mensagens. " +
        "É necessário conectar um serviço para receber os contatos.";

    formulario.reset();

    Object.keys(erros).forEach(function (campo) {
        mostrarErro(campo, "");
    });
});


<img width="547" height="365" alt="image" src="https://github.com/user-attachments/assets/8feba655-13ba-47f1-9aeb-6c7044800070" />
<img width="612" height="344" alt="image" src="https://github.com/user-attachments/assets/ea4de0c3-275f-4c6f-9f58-e5930f0041bf" />
<img width="660" height="440" alt="image" src="https://github.com/user-attachments/assets/06ea97b3-d75a-4292-a91e-fe5fff41912f" />


