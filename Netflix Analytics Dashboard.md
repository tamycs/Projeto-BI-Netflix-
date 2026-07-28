# Netflix Analytics Dashboard!

Maio 2026 • Power Bi

Este projeto teve como objetivo a construção de um dashboard no Power BI a partir de um dataset de títulos da Netflix, com foco na preparação, modelagem e estruturação dos dados.

A base original continha informações como título, tipo (filme ou série), ano de lançamento, duração, gêneros, países de produção e métricas externas como IMDb. Durante a exploração inicial, foram identificadas algumas características comuns em bases reais, como dados em formato não estruturado, presença de valores nulos e campos multivalorados.

A etapa de preparação foi iniciada no Excel, com verificações de consistência, incluindo validação de possíveis duplicidades. Para isso, foi criada uma chave composta utilizando múltiplos atributos, garantindo que títulos com nomes iguais, mas características distintas, não fossem tratados incorretamente como duplicados.

Em seguida, os dados foram carregados no Power BI, onde o tratamento foi aprofundado utilizando o Power Query. Colunas como gêneros e países, que estavam originalmente em formato de lista (com colchetes e aspas), foram normalizadas. Esse processo incluiu a remoção de caracteres indesejados e a transformação dessas colunas em múltiplas linhas, permitindo uma análise mais adequada.

Para evitar distorções nas métricas, foi adotada uma modelagem com tabelas separadas:

- uma tabela principal contendo os títulos
- uma tabela auxiliar para gêneros
- uma tabela auxiliar para países

Essas tabelas foram relacionadas por meio de um identificador único, formando uma estrutura relacional simples. Essa abordagem evita duplicidade de contagem e melhora a performance e a confiabilidade das análises.

Durante a modelagem, também foram realizados ajustes nas métricas, como a definição de agregações apropriadas (ex.: média para avaliações, contagem distinta para títulos) e tratamento de valores nulos quando necessário.

O resultado final é um dashboard estruturado, com dados tratados e modelados de forma consistente, permitindo análises confiáveis e com boa performance.

Este projeto demonstra não apenas a construção visual, mas principalmente o processo de preparação e organização de dados, etapa essencial em projetos de Business Intelligence.

### 📊 Página 1 — Visão Geral do Catálogo

O primeiro painel apresenta os principais indicadores do catálogo Netflix. Com **5.850 títulos** catalogados, a plataforma conta com produções de **110 países**, refletindo seu alcance global e **20 gêneros** identificados, sendo **19 gêneros válidos** após exclusão de registros sem classificação

A distribuição por tipo revela uma predominância clara de filmes: **64% do catálogo são filmes (Movie)** contra **36% de séries (Show)**, totalizando aproximadamente 3,74 mil títulos em filme e 2,11 mil em séries.

Geograficamente, os **Estados Unidos lideram com absoluta dominância**, com mais de 2.000 títulos — quase o triplo do segundo colocado, a Índia (IN). Reino Unido (GB), França (FR) e Canadá (CA) completam o TOP 5, com volumes bem menores, evidenciando a forte concentração de produção no mercado americano.

---

### 🎭 Página 2 — Análise de Conteúdo por Gênero

Com filtros por **ano de lançamento (1945–2022)**, **país** e **tipo**, esta página permite uma análise dinâmica da composição do catálogo por gênero.

O gênero **Drama domina com 2.967 títulos**, seguido de **Comédia** (Comedy -2.323) e Suspense (**Thriller - 1.228)**. Ação (Action) e Romance (Romance) também aparecem com volumes expressivos (1.157 e 971 respectivamente), enquanto Documentário (Documentation) fecha o TOP 6 com 952 títulos.

Esse perfil reforça a preferência da plataforma por conteúdos dramáticos e de comédia, gêneros de amplo apelo popular e alta retenção de audiência.

---

### ⭐ Página 3 — Gêneros Acima da Média IMDb

Com média geral de **6,51 no IMDb Score**, esta página destaca os gêneros que superam esse benchmark de qualidade percebida pelo público.

Os destaques são:

- **Sem dados: 7,25** — títulos sem classificação de gênero tendem a ter scores elevados, possivelmente por serem obras de nicho com audiência fiel
- **História (History): 7,13** — conteúdo histórico é bem avaliado, sugerindo um público exigente e engajado
- **Guerra (War): 7,07** — filmes de guerra costumam ter produções robustas e roteiros densos
- **Documentário (Documentation): 7,01** — documentários mantêm média alta, reflexo de produções criteriosas

Na outra ponta, **Comedy (6,39)**, **Romance (6,38)** e **Thriller (6,37)** ficam abaixo da média geral, indicando que apesar do alto volume de títulos nesses gêneros, a qualidade percebida é menor.

**Insight:** existe uma relação inversa entre volume e qualidade ; os gêneros com mais títulos (Drama, Comedy, Thriller) tendem a ter scores mais baixos, enquanto gêneros de nicho como History e War concentram obras mais bem avaliadas.

---

### 🏆 Página 4 — Engajamento & Popularidade no IMDb

### Votos IMDb

**A origem (Inception) lidera com 22,94 Mi de votos**, seguido de Forrest Gump (20,21 Mi) e Breaking Bad (17,76 Mi). A distribuição mostra uma queda gradual, com Os bons companheiros (GoodFellas) fechando o TOP 10 com 11,32 Mi — ainda assim um número expressivo de engajamento.

A presença de **Breaking Bad** (série) no TOP 3 de votos é notável, demonstrando que o engajamento de séries pode rivalizar com grandes produções cinematográficas.

### Popularidade

O ranking de popularidade traz uma surpresa: **Breaking Bad domina com 353,8 Mil**, quase o dobro do segundo colocado Titanic (155,7 Mil). Inception aparece em terceiro (108,3 Mil).

**Insight:** Breaking Bad é o título mais equilibrado do catálogo — está entre os mais votados **e** é de longe o mais popular, sugerindo que continua sendo ativamente buscado e assistido mesmo anos após seu lançamento. Já Titanic tem alta popularidade mas votos mais modestos, o que pode indicar um público mais casual que assiste mas não avalia.

