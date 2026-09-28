# :checkered_flag: ELOREPX

Elorepx é uma plataforma web que incentiva e prepara estudantes do ensino fundamental e médio para olimpíadas científicas. Ela reúne informações sobre as principais olimpíadas, relatos de alunos olímpicos, biografias de cientistas e um calendário de provas. Oferece também quizzes preparatórios por nível de dificuldade, com correção determinística e explicações complementares geradas por Inteligência Artificial. Uma camada de gamificação (XP, níveis, medalhas e missões) acompanha o progresso individual do estudante.

## :technologist: Membros da equipe

554563 - Daniel Lucas Ulisses Magalhães - Engenharia de Software

## :bulb: Objetivo Geral
Desenvolver uma plataforma web que incentive e prepare estudantes para olimpíadas científicas, combinando conteúdo motivacional, quizzes preparatórios, gamificação e IA de escopo controlado, a fim de reduzir barreiras de informação, motivação e acesso a material de qualidade em português.

## :eyes: Público-Alvo
- Estudantes do ensino fundamental e médio, principalmente de escolas públicas, que acessam o sistema muitas vezes pelo celular pessoal.
- Professores de ciências que desejam usar a plataforma como apoio metodológico para motivar os alunos e discutir olimpíadas em sala.

## :star2: Impacto Esperado
- **Divulgação:** dar visibilidade às olimpíadas científicas, seus prêmios, bolsas e oportunidades, já que a falta de divulgação foi apontada nas entrevistas como um dos obstáculos à participação.
- **Motivação:** aproximar o estudante da ciência por meio de relatos reais de alunos olímpicos, biografias, conteúdo visual e gamificação simples, sem ranking comparativo, para não desestimular quem está em contexto de vulnerabilidade.
- **Preparação:** oferecer treino gratuito, acessível pelo celular e com feedback imediato
- **Apoio ao professor:** disponibilizar um recurso metodológico que integra teoria, prática visual e conteúdo do cotidiano.

## :people_holding_hands: Papéis ou tipos de usuário da aplicação

| **Visitante (não logado)** | Navega pelo conteúdo público da plataforma sem criar conta. |
| **Estudante (logado)** | Usuário cadastrado que resolve quizzes com progresso registrado e acompanha sua evolução. |
| **Administrador** | Responsável por gerenciar o conteúdo da plataforma e moderar os feedbacks. |

## :triangular_flag_on_post:	 Principais funcionalidades da aplicação

**Acessíveis a todos (visitante, estudante e administrador):**
- Informações sobre as principais olimpíadas (descrição, sites e redes sociais oficiais);
- Importância das olimpíadas: prêmios, bolsas e oportunidades;
- Relatos de alunos olímpicos (texto, foto e vídeo);
- Biografias de cientistas;
- Calendário de olimpíadas (inscrições, provas e resultados);
- Seção "Ciência e cotidiano" e curiosidades científicas;
- Conteúdo dinâmico de ciência via API externa (ex.: NASA);
- Canais e recursos de estudo curados, com prioridade para conteúdo em português;
- Cadastro e login.

**Restritas a estudantes logados:**
- Quizzes preparatórios com escolha de nível de dificuldade e correção imediata;
- Explicação complementar gerada por IA após cada questão, com limite diário de uso;
- Perfil com XP, nível e barra de progresso;
- Medalhas, conquistas e missões;
- Envio de feedback sobre a plataforma.

**Restritas ao administrador:**
- CRUD de olimpíadas, eventos do calendário, questões, relatos, biografias e recursos de estudo;
- Consulta e moderação dos feedbacks recebidos;
- Gerenciamento de medalhas e missões.

## :spiral_calendar: Entidades ou tabelas do sistema

- **Usuario** (id, email, senha, apelido, papel, XP, nível)
- **Olimpiada** (nome, descrição, site, redes sociais)
- **EventoCalendario** (olimpíada, tipo: inscrição/prova/resultado, data)
- **Assunto** (área do conhecimento)
- **Questao** (enunciado, gabarito, dificuldade, olimpíada, assunto)
- **AlternativaQuestao**
- **Quiz** (agrupamento de questões por olimpíada e nível)
- **TentativaQuiz** e **RespostaUsuario** (histórico de respostas)
- **ExplicacaoIA** (explicação gerada, associada à questão)
- **UsoIA** (contagem diária de chamadas por usuário)
- **Curiosidade** (conteúdo de cotidiano/IA)
- **RelatoOlimpico** (texto, mídia, autor do relato)
- **Cientista** (biografia e descobertas)
- **RecursoEstudo** (canais, sites, jogos; idioma)
- **NivelProgressao** (faixas de XP e nomes dos níveis)
- **Medalha** e **UsuarioMedalha**
- **Missao** e **UsuarioMissao**
- **Feedback** (mensagem, tipo, usuário, status)
