# Registo de versões — Treino Bruno

Cada alteração ao código da app tem uma versão nova, registada aqui e marcada no GitHub com uma tag (`vX.Y.Z`).
As actualizações só de dados (pesagens, treinos) não mudam a versão: ficam no histórico de commits como `Dados: …`.

As tags e os Releases são criados automaticamente pelo GitHub (`.github/workflows/versoes.yml`) sempre que a versão muda.

Numeração: **X** = mudança grande na app · **Y** = funcionalidade nova · **Z** = correcção ou ajuste pequeno.

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
