# Registo de versões — Treino Bruno

Cada alteração ao código da app tem uma versão nova, registada aqui e marcada no GitHub com uma tag (`vX.Y.Z`).
As actualizações só de dados (pesagens, treinos) não mudam a versão: ficam no histórico de commits como `Dados: …`.

As tags e os Releases são criados automaticamente pelo GitHub (`.github/workflows/versoes.yml`) sempre que a versão muda.

Numeração: **X** = mudança grande na app · **Y** = funcionalidade nova · **Z** = correcção ou ajuste pequeno.

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
