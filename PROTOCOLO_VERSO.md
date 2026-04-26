# O Protocolo Verso
### Documento de Produto — MVP para os Primeiros 1.000 Usuários (SOM)

---

## 1. Visão Executiva

O Verso é uma rede social literária cuja unidade atômica de interação é o **capítulo**, não o livro. A plataforma funciona como uma "segunda tela" para leitores: enquanto leem, abrem o Verso para reagir, debater e teorizar — sempre protegidos de spoilers por travas estruturais no código.

**Posicionamento:** Substituir Goodreads/Skoob com uma experiência social-first, onde a conversa é tão importante quanto a estante.

**Identidade Visual:** Estética "The Canvas" — tons off-white, sálvia e verde-oliva. Minimalista. Funcional. Zero entulho visual.

---

## 2. User Stories Prioritárias (3 Fluxos de Retenção)

### Fluxo 1: "Reação ao Capítulo" (Core Loop)

> **Como** leitora que acabou de ler um capítulo intenso,
> **Quero** abrir o Verso e ver o que outros leitores acharam daquele capítulo específico,
> **Para** validar minha reação emocional e me sentir parte de uma comunidade que entende o que acabei de sentir.

**Critérios de Aceite:**
- O post exige seleção obrigatória do **livro**.
- Seleção opcional (mas incentivada via UI) do **capítulo/página** (checkpoint).
- Flag **"Contém Spoiler" [ON/OFF]** visível e obrigatória em todo post.
- O fórum do livro organiza posts por capítulo com navegação por abas numéricas (1, 2, 3, 4, ..., 8, 9).
- O leitor que está no Capítulo 5 **não vê conteúdo** marcado para capítulos 6+ (trava de spoiler no código).

**Métricas-chave:** Posts/dia por usuário, taxa de clique em "ver mais..." por capítulo.

---

### Fluxo 2: "Descoberta Social" (Growth Loop)

> **Como** leitor que terminou um livro e quer o próximo,
> **Quero** ver o que as pessoas que reagiram como eu estão lendo agora,
> **Para** descobrir meu próximo livro através de afinidade emocional, não de algoritmo genérico.

**Critérios de Aceite:**
- Timeline global ("Explorar") mostra posts de alta interação de livros que o usuário **não** está lendo.
- Timeline "Seguindo" mostra posts de quem o usuário segue.
- Cada post na timeline exibe contexto: **nome do livro + capítulo**, clicável para ir ao fórum.
- Busca por título, autor ou gênero com card de livro contendo: capa, sinopse, rating, contagem de leitores ativos ("35K lendo agora"), e botão "Ver Fórum do Livro".

**Métricas-chave:** Taxa de conversão "ver fórum" → "adicionar à estante", livros adicionados via descoberta social vs. busca direta.

---

### Fluxo 3: "Identidade Literária" (Retention Loop)

> **Como** leitora assídua,
> **Quero** que meu perfil reflita minha jornada de leitura com dados visuais,
> **Para** construir uma identidade literária que me diferencia e me dá status na comunidade.

**Critérios de Aceite:**
- Perfil exibe **heatmap de leitura** (estilo GitHub contributions — páginas/dia).
- **Gráfico de gêneros** lidos (distribuição visual).
- **Badges comportamentais** desbloqueáveis:
  - "Teorista do Cap. 5" — fez 10+ posts teóricos antes do meio do livro.
  - "Maratonista" — leu 3 livros em 7 dias.
  - "Primeiro a Chegar" — primeiro post em um fórum de capítulo recém-aberto.
  - "Debate Aceso" — post com 50+ respostas.
- Contadores públicos: **Seguidores**, **Livros Lidos**, **Posts**.

**Métricas-chave:** % de usuários que personalizam perfil, frequência de visita ao próprio perfil, badges mais desbloqueados.

---

## 3. Mecanismo de Retenção: Gamificação do "Fórum por Capítulo"

### 3.1 O Loop "Virou a Página → Abriu o Verso"

O objetivo é condicionar o comportamento: **a cada capítulo terminado, o leitor sente a necessidade de abrir o Verso.**

| Gatilho | Mecânica | Recompensa |
|---------|----------|------------|
| Terminou um capítulo | Novo fórum de capítulo se "desbloqueia" para o leitor | Conteúdo novo e exclusivo (posts que antes estavam travados) |
| Entrou no fórum do capítulo | Contagem de "X pessoas reagiram a este capítulo" | Validação social + FOMO positivo |
| Fez seu primeiro post no capítulo | Badge "Primeiro a Chegar" (se for o 1º) | Status + diferenciação |
| Recebeu resposta no seu post | Notificação push com preview | Dopamina de interação social |
| Avançou para o próximo capítulo | Teaser: "23 pessoas já estão discutindo o Cap. 6" | Curiosidade → leitura mais rápida → mais posts |

### 3.2 Mecânicas de Gamificação Específicas

- **Progresso Visível:** Barra de progresso no fórum do livro mostrando "Você está no Cap. 5 de 12. Continue lendo para desbloquear mais discussões."
- **Ranking por Livro:** "Top Comentaristas" de cada livro — os 3 leitores mais ativos no fórum ganham destaque.
- **Streaks de Leitura:** Heatmap no perfil fica verde a cada dia que o leitor registra progresso. Streak de 7 dias = badge "Semana Literária".
- **Spoiler Shield como Feature, não Limitação:** Posicionar a trava de spoiler como algo desejável. Copy: "Leia no seu ritmo. O Verso protege sua experiência."

### 3.3 Ciclo de Retenção Semanal

```
Seg-Sex: Lê capítulos → posta reações → recebe respostas
Sáb:     Review da semana no perfil (heatmap atualiza, possível badge novo)
Dom:     "Explorar" mostra destaques da semana → descobre próximo livro
```

---

## 4. Estratégia de Dados: Métricas para Validar o "Efeito Comunidade"

### 4.1 North Star Metric

**Posts com pelo menos 1 resposta dentro de 24h (%)** — Se esta métrica sobe, o efeito comunidade está vivo. Se posts ficam sem resposta, a rede está morta.

### 4.2 Métricas de Validação (Antes de Escalar para 10K)

| Categoria | Métrica | Meta MVP (1K users) | Sinal de Alerta |
|-----------|---------|---------------------|-----------------|
| **Ativação** | % de novos usuários que postam nos primeiros 3 dias | ≥ 30% | < 15% |
| **Engajamento** | Posts/semana por usuário ativo | ≥ 2 | < 0.5 |
| **Comunidade** | % de posts que recebem ≥1 resposta em 24h | ≥ 40% | < 20% |
| **Retenção** | D7 Retention (voltou no dia 7) | ≥ 35% | < 20% |
| **Retenção** | D30 Retention | ≥ 20% | < 10% |
| **Spoiler Trust** | % de posts com flag de spoiler ativada corretamente | ≥ 60% dos posts de cap. 5+ | Denúncias de spoiler > 5% |
| **Discovery** | % de livros adicionados via "Explorar" (não busca) | ≥ 25% | < 10% |
| **Depth** | Média de capítulos discutidos por livro por usuário | ≥ 3 | < 1 |
| **Network** | Follows mútuos / total de follows | ≥ 15% | < 5% |

### 4.3 Cohort Analysis Framework

Segmentar usuários em cohorts semanais e monitorar:

1. **Curva de Retenção por Cohort** — A curva deve se achatar (plateau), não cair a zero. Se o cohort da semana 4 retém melhor que o da semana 1, o produto está melhorando.

2. **Ativação por Livro** — Quais livros geram mais comunidade? Isso direciona parcerias com editoras e curadoria de conteúdo.

3. **Power Users vs. Lurkers** — Proporção ideal: ~10% power users (5+ posts/semana), ~30% contributors (1-4 posts/semana), ~60% lurkers (leem mas não postam). Se lurkers > 80%, o friction de postagem está alto.

### 4.4 Sinais de "Pronto para Escalar"

O produto está pronto para ir de 1K → 10K quando:

- [ ] D7 Retention ≥ 35% por 4 cohorts consecutivos
- [ ] North Star (posts respondidos em 24h) ≥ 40%
- [ ] Pelo menos 3 livros com fóruns ativos (≥50 posts/semana cada)
- [ ] NPS ≥ 50 em pesquisa com amostra de 100+ usuários
- [ ] Taxa de denúncia de spoiler < 3%

---

## 5. Stack Técnica Recomendada (MVP)

| Camada | Tecnologia | Justificativa |
|--------|------------|---------------|
| Frontend | React + Tailwind CSS | Velocidade de prototipação, estética consistente |
| Backend | Node.js + Express ou Next.js API Routes | Fullstack JS, time enxuto |
| Database | PostgreSQL + Prisma ORM | Relacional (livros → capítulos → posts → respostas) |
| Auth | Clerk ou NextAuth | Auth social rápida (Google, Apple) |
| Real-time | WebSockets (Socket.io) ou Supabase Realtime | Notificações de resposta em tempo real |
| Analytics | Mixpanel ou PostHog | Funnels, cohorts, retenção |
| Deploy | Vercel + Supabase | Zero DevOps no MVP |

---

## 6. Roadmap MVP (8 Semanas)

| Semana | Entrega |
|--------|---------|
| 1-2 | Auth + modelo de dados (livros, capítulos, posts) + estante básica |
| 3-4 | Timeline global + fórum por capítulo + postagem com contexto |
| 5 | Spoiler flag + trava de conteúdo por checkpoint |
| 6 | Perfil com heatmap + badges (v1) |
| 7 | Busca + discovery social + notificações |
| 8 | Polish visual (The Canvas), testes com 50 beta users, ajustes |

---

*Documento gerado como parte do Protocolo Verso. Versão 1.0 — Abril 2026.*
