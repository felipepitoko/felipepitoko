<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Felipe Sousa da Costa | GitHub Profile</title>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* Light gray background */
            color: #374151; /* Dark gray text */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 1rem; /* p-4 */
        }

        .container {
            background-color: #fff;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); /* shadow-xl */
            border-radius: 0.75rem; /* rounded-xl */
            padding: 1.5rem; /* p-6 */
            max-width: 48rem; /* max-w-4xl */
            width: 100%;
            margin-left: auto;
            margin-right: auto;
            border: 1px solid #e5e7eb; /* border border-gray-200 */
        }

        @media (min-width: 640px) { /* sm breakpoint */
            body {
                padding: 1.5rem; /* sm:p-6 */
            }
            .container {
                padding: 2rem; /* sm:p-8 */
            }
        }

        @media (min-width: 768px) { /* md breakpoint */
            body {
                padding: 2rem; /* md:p-8 */
            }
            .container {
                padding: 2.5rem; /* md:p-10 */
            }
            .skills-grid {
                grid-template-columns: repeat(2, minmax(0, 1fr)); /* md:grid-cols-2 */
            }
        }

        @media (min-width: 1024px) { /* lg breakpoint */
            .container {
                padding: 3rem; /* lg:p-12 */
            }
        }

        /* Header Section */
        .header {
            text-align: center;
            margin-bottom: 2rem; /* mb-8 */
        }

        .header h1 {
            font-size: 2.25rem; /* text-4xl */
            font-weight: 800; /* font-extrabold */
            color: #1d4ed8; /* text-blue-700 */
            margin-bottom: 0.5rem; /* mb-2 */
        }

        .header h2 {
            font-size: 1.25rem; /* text-xl */
            font-weight: 600; /* font-semibold */
            color: #4b5563; /* text-gray-700 */
        }

        .header hr {
            margin-top: 1.5rem; /* my-6 */
            margin-bottom: 1.5rem;
            border-top: 2px solid #bfdbfe; /* border-t-2 border-blue-200 */
            width: 6rem; /* w-24 */
            margin-left: auto;
            margin-right: auto;
            border-radius: 9999px; /* rounded-full */
        }

        @media (min-width: 640px) { /* sm breakpoint */
            .header h1 {
                font-size: 3rem; /* sm:text-5xl */
            }
            .header h2 {
                font-size: 1.5rem; /* sm:text-2xl */
            }
        }

        /* Section Headings */
        .section-heading {
            font-size: 1.5rem; /* text-2xl */
            font-weight: 700; /* font-bold */
            color: #1f2937; /* text-gray-800 */
            margin-bottom: 1rem; /* mb-4 */
        }

        @media (min-width: 640px) { /* sm breakpoint */
            .section-heading {
                font-size: 1.875rem; /* sm:text-3xl */
            }
        }

        /* Paragraphs */
        .section-paragraph {
            color: #4b5563; /* text-gray-700 */
            line-height: 1.625; /* leading-relaxed */
            margin-bottom: 1rem; /* mb-4 */
        }

        .section-paragraph strong {
            color: #2563eb; /* text-blue-600 */
        }

        /* My Skills Section */
        .skills-list {
            display: grid;
            grid-template-columns: 1fr; /* grid-cols-1 */
            gap: 1rem; /* gap-4 */
            color: #4b5563; /* text-gray-700 */
        }

        .skills-list li {
            display: flex;
            align-items: flex-start; /* items-start */
        }

        .skills-list li span {
            color: #3b82f6; /* text-blue-500 */
            margin-right: 0.5rem; /* mr-2 */
            font-size: 1.25rem; /* text-xl */
        }

        .skills-list li p strong {
            font-weight: 600; /* font-semibold */
        }

        /* Technologies & Tools Section */
        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem; /* gap-3 */
        }

        .tech-tags span {
            background-color: #dbeafe; /* bg-blue-100 */
            color: #1e40af; /* text-blue-800 */
            font-size: 0.875rem; /* text-sm */
            font-weight: 500; /* font-medium */
            padding: 0.25rem 0.75rem; /* px-3 py-1 */
            border-radius: 9999px; /* rounded-full */
            box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05); /* shadow-sm */
        }

        /* Explore My Work Section */
        .explore-list {
            list-style-type: disc;
            list-style-position: inside;
            color: #4b5563; /* text-gray-700 */
            line-height: 1.625; /* leading-relaxed */
        }

        .explore-list li {
            margin-bottom: 0.5rem; /* space-y-2 */
        }

        /* Let's Connect Section */
        .connect-section {
            text-align: center;
        }

        .connect-section .connect-links {
            display: flex;
            flex-direction: column; /* flex-col */
            justify-content: center;
            gap: 1rem; /* gap-4 */
        }

        @media (min-width: 640px) { /* sm breakpoint */
            .connect-section .connect-links {
                flex-direction: row; /* sm:flex-row */
            }
        }

        .connect-button {
            background-color: #2563eb; /* bg-blue-600 */
            color: #fff;
            font-weight: 700; /* font-bold */
            padding: 0.75rem 1.5rem; /* py-3 px-6 */
            border-radius: 0.5rem; /* rounded-lg */
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06); /* shadow-md */
            transition: all 0.3s ease-in-out; /* transition duration-300 ease-in-out */
            text-decoration: none;
            display: inline-block; /* Ensure padding works */
        }

        .connect-button:hover {
            background-color: #1d4ed8; /* hover:bg-blue-700 */
            transform: scale(1.05); /* hover:scale-105 */
        }

        .connect-button.email {
            background-color: #374151; /* bg-gray-700 */
        }

        .connect-button.email:hover {
            background-color: #1f2937; /* hover:bg-gray-800 */
        }
    </style>
</head>
<body>
    <div class="container">

        <!-- Header Section -->
        <header class="header">
            <h1>Olá, sou Felipe Sousa da Costa 👋</h1>
            <h2>Engenheiro de Software Focado em Soluções | Tech Lead | Especialista em Python e Nuvem</h2>
            <hr>
        </header>

        <!-- About Me Section -->
        <section class="section-about-me">
            <h3 class="section-heading">Sobre Mim</h3>
            <p class="section-paragraph">
                Sou um Engenheiro de Software apaixonado, com mais de 4 anos de experiência no desenvolvimento <strong>Back-End</strong> e na construção de soluções de software robustas e escaláveis. Como um <strong>"Solutions Builder"</strong>, tenho expertise em transformar desafios complexos em arquiteturas técnicas eficientes e de alta performance, utilizando <strong>Python</strong> com frameworks como Django, Flask e FastAPI.
            </p>
            <p class="section-paragraph">
                Minha atuação inclui o desenvolvimento de <strong>microsserviços</strong> e a integração de sistemas diversos. Possuo forte experiência em plataformas de nuvem, especialmente <strong>AWS</strong>, e trabalho com <strong>bancos de dados relacionais e não-relacionais</strong>. Minha experiência como Tech Lead me permitiu liderar equipes, colaborar ativamente e interagir com clientes para entregar transformações digitais impactantes.
            </p>
        </section>

        <!-- My Skills Section -->
        <section class="section-skills">
            <h3 class="section-heading">Minhas Habilidades</h3>
            <ul class="skills-list">
                <li>
                    <span>&#10003;</span>
                    <p><strong>Desenvolvimento Back-End:</strong> Experiência sólida com Python e frameworks web modernos (Django, Flask, FastAPI).</p>
                </li>
                <li>
                    <span>&#10003;</span>
                    <p><strong>Microsserviços:</strong> Habilidade em projetar, desenvolver e implantar arquiteturas de microsserviços.</p>
                </li>
                <li>
                    <span>&#10003;</span>
                    <p><strong>Cloud (AWS):</strong> Proficiência em implantação e gestão de aplicações na nuvem AWS (EC2, Lambda, S3, RDS, SQS, SNS, CloudWatch, EKS).</p>
                </li>
                <li>
                    <span>&#10003;</span>
                    <p><strong>Integração de Sistemas:</strong> Especialista na conexão de sistemas via APIs RESTful e pipelines de dados (ETL).</p>
                </li>
                <li>
                    <span>&#10003;</span>
                    <p><strong>Bancos de Dados:</strong> Experiência com SQL (PostgreSQL, MySQL) e NoSQL (DynamoDB).</p>
                </li>
                <li>
                    <span>&#10003;</span>
                    <p><strong>Liderança e Agile:</strong> Habilidades em liderança de equipes e aplicação de metodologias ágeis (Scrum/Kanban).</p>
                </li>
                <li>
                    <span>&#10003;</span>
                    <p><strong>Comunicação:</strong> Fluência em Português e Inglês profissional para comunicação global.</p>
                </li>
            </ul>
        </section>

        <!-- Technologies & Tools Section -->
        <section class="section-tech-tools">
            <h3 class="section-heading">Tecnologias & Ferramentas</h3>
            <div class="tech-tags">
                <span>Python</span>
                <span>SQL</span>
                <span>Django</span>
                <span>Flask</span>
                <span>FastAPI</span>
                <span>AWS</span>
                <span>PostgreSQL</span>
                <span>MySQL</span>
                <span>DynamoDB</span>
                <span>Microsserviços</span>
                <span>RESTful APIs</span>
                <span>ETL</span>
                <span>Git</span>
                <span>Agile (Scrum/Kanban)</span>
                <span>Linux</span>
                <span>CloudWatch</span>
                <span>Testes Unitários</span>
            </div>
        </section>

        <!-- Explore My Work Section -->
        <section class="section-explore-work">
            <h3 class="section-heading">Explore Meu Trabalho</h3>
            <p class="section-paragraph">
                Confira meus repositórios para ver exemplos de:
            </p>
            <ul class="explore-list">
                <li>Serviços Back-End Escaláveis e Desenvolvimento de API</li>
                <li>Implantações em Nuvem e Infraestrutura como Código</li>
                <li>Soluções de Processamento de Dados e ETL</li>
                <li>Implementações de Microsserviços</li>
                <li>Projetos de Integração de Sistemas</li>
            </ul>
        </section>

        <!-- Let's Connect Section -->
        <section class="connect-section">
            <h3 class="section-heading">Conecte-se Comigo!</h3>
            <p class="section-paragraph" style="margin-bottom: 1.5rem;">
                Estou sempre aberto a novas oportunidades, colaborações em projetos interessantes ou troca de conhecimentos sobre desenvolvimento de software.
            </p>
            <div class="connect-links">
                <a href="[Seu URL do Perfil do LinkedIn, ex: https://www.linkedin.com/in/felipe-costa-engineer/]" target="_blank" class="connect-button">
                    LinkedIn
                </a>
                <a href="mailto:lip-sousa@hotmail.com" class="connect-button email">
                    Email
                </a>
            </div>
        </section>

    </div>
</body>
</html>
