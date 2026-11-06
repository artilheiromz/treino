# Registo de versões — Treino Bruno

Cada alteração ao código da app tem uma versão nova, registada aqui e marcada no GitHub com uma tag (`vX.Y.Z`).
As actualizações só de dados (pesagens, treinos) não mudam a versão: ficam no histórico de commits como `Dados: …`.

As tags e os Releases são criados automaticamente pelo GitHub (`.github/workflows/versoes.yml`) sempre que a versão muda.

Numeração: **X** = mudança grande na app · **Y** = funcionalidade nova · **Z** = correcção ou ajuste pequeno.

## v1.3.0 — 6 Nov 2026
Disposição dos ecrãs igual ao mockup em vidro (a v1.2.0 só tinha mudado cores e efeitos).
- **Início:** sem a faixa de quadradinhos no topo; cartão do corpo com o peso em destaque, etiqueta da variação desde 10 Out e três mini-cartões (gordura perdida, % gordura, visceral); cartão da semana com barra de sessões feitas e piscinas, tempo e caminhadas; aviso da pesagem em cápsula. O cartão "Plano" sai do Início (continua no separador Plano).
- **Treinos:** faixa da semana numa única cápsula de vidro; cartão da sessão com o número de piscinas em destaque; botão compacto "Cartão para a piscina"; blocos do treino com número (passa a ✓ quando feito), intensidade no título e piscinas à direita; caixas de verificação redondas no estilo da app.
- **Plano:** o próximo treino aparece como "Próximo".
- Barra de separadores mais fina e etiqueta "Feito" mais verde.

## v1.2.2 — 6 Nov 2026
- Correcção: o iPhone continuava a mostrar o ícone antigo guardado em cache. Os endereços do ícone e do manifest passam a levar a versão (`?v=122`), para obrigar o Safari a ir buscar o ícone novo.

## v1.2.1 — 6 Nov 2026
- Novo ícone da app em vidro (proposta A): fundo de água azul com um painel de vidro e a linha de ritmo cardíaco a branco. Substitui o ícone anterior no ecrã principal, no ecrã do código e no separador do browser.
- Para o iPhone mostrar o ícone novo é preciso apagar o atalho e voltar a adicioná-lo ao ecrã principal.

## v1.2.0 — 6 Nov 2026
Novo visual em vidro, inspirado no estilo do iOS 26 (aprovado a partir do mockup de 6 Nov).
- Fundo de água azul com reflexos de luz e superfícies translúcidas desfocadas em todos os cartões, linhas do plano, blocos do treino, botões e selectores.
- Barra de separadores flutuante em cápsula de vidro, com o separador activo destacado.
- Dia seleccionado, selector Corpo/Treinos e etiqueta "Hoje" em branco sólido; "Feito" em verde-menta; caminhadas em lilás.
- Tipografia do sistema do iPhone (SF Pro); ecrã do código e botão "Entrar" no mesmo estilo.
- O cartão da piscina mantém o fundo preto, para ler bem no ecrã bloqueado.

## v1.1.1 — 5 Nov 2026
- Descansos explicados: nos blocos com repetições aparece "desc. 30 s **entre repetições**" (na página do treino e no cartão da piscina), e o cartão lembra "entre blocos: cerca de 1 min".
- Resumo do treino mostra a frequência cardíaca pós-treino (no fim, 1 min e 2 min depois), para acompanhar a recuperação.

## v1.1.0 — 3 Nov 2026
Ajustes depois do primeiro treino (teste de nível de 3 Nov).
- **Cartão para a piscina:** na página de cada treino por fazer há um botão que abre o treino em letra grande, com os blocos numerados. Pensado para tirar print e pôr como fundo do ecrã bloqueado, porque na piscina não dá para mexer no telemóvel com as mãos molhadas.
- **Plano das sessões 2 a 12 reescrito em piscinas** (ex.: "4 × 4 piscinas: 2 crawl + 2 bruços"), com menos blocos por sessão para ser fácil de memorizar. Volume ajustado ao teste (12 piscinas em 10 min): semana 1 ≈ 2400 m, semana 2 ≈ 2900 m, semana 3 ≈ 3300 m, semana 4 ≈ 3800 m.
- **Resumo do treino mais completo:** piscinas, tempo a nadar, ritmo a nadar, kcal activas, esforço, SWOLF, metros por estilo, tempo por zona de FC, hora e temperatura da água, e detalhe do teste de 10 min.
- Progresso: o teste de 10 min mostra também o número de piscinas.

## v1.0.0 — 2 Nov 2026
Primeira versão no GitHub Pages.
- App instalável no iPhone em ecrã inteiro (sem a barra do Claude), com ícone e nome "Treino".
- Ecrã de código de acesso; os dados (pesagens e actividades) ficam encriptados em `dados.enc.json` (AES-GCM, chave PBKDF2). Opção "Lembrar neste telemóvel" e botão **Bloquear** no Início.
- Site marcado para não ser indexado por motores de pesquisa.
- Número da versão visível no fundo do Início.

## Versões anteriores (dentro do Claude, antes do GitHub)
- **v0.3 — 2 Nov 2026:** nome mudado para "Treino Bruno"; ícone do separador Treinos passou de nadador para actividade genérica.
- **v0.2 — 2 Nov 2026:** menu de entrada (Início); Treinos dia a dia com faixa da semana e resumo dos dias feitos; Progresso com Corpo/Treinos, vista geral ou por data/semana; caminhadas opcionais (qua e dom); ritmo médio calculado a partir do ritmo do Apple Watch.
- **v0.1 — 2 Nov 2026:** primeira app: Hoje, Plano de 4 semanas de natação, Progresso com dados da balança de 10 a 31 Out.
