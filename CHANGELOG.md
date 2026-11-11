# Registo de versões — Treino Bruno

Cada alteração ao código da app tem uma versão nova, registada aqui e marcada no GitHub com uma tag (`vX.Y.Z`).
As actualizações só de dados (pesagens, treinos) não mudam a versão: ficam no histórico de commits como `Dados: …`.

As tags e os Releases são criados automaticamente pelo GitHub (`.github/workflows/versoes.yml`) sempre que a versão muda.

Numeração: **X** = mudança grande na app · **Y** = funcionalidade nova · **Z** = correcção ou ajuste pequeno.

## v1.8.2 — 11 Nov 2026
- Novos recordes pessoais: **Ritmo mais rápido a nadar** (por 100 m, sem contar paragens) e **Mais crawl num treino**. Os dois também contam para a conquista Superação.
- Tabela "Treino a treino": novas linhas **Ritmo a nadar** e **Crawl**.
- Plano: os blocos de pernas passam a explicar que se fazem **de costas e sem prancha** (braços junto ao corpo), porque o Bruno ainda não tem prancha.
- Dados: treino de 11 Nov (sessão 4).

## v1.8.1 — 11 Nov 2026
- A conquista genérica "Um número abaixo" deu lugar a duas conquistas concretas: **Calças 42** e **Calças 40**. Ficam por ganhar mostrando o tamanho actual (44), e são marcadas quando o Bruno disser que lhe servem.
- Dados: data de aniversário (para "Aniversário activo"), tamanho de calças actual, 4 piscinas seguidas só em crawl a 3 Nov e maior bloco de 6:49 a 9 Nov.

## v1.8.0 — 10 Nov 2026
Novas conquistas aprovadas pelo Bruno (inquérito de 10 Nov) e níveis bronze/prata/ouro.
- **Níveis**: as conquistas que se repetem contam as vezes e ganham uma insígnia de bronze, prata ou ouro (ex.: Sexta-feira de campeão 1×/5×/10×).
- **Gerais**: Sexta-feira de campeão, Sexta sem copos, Fim-de-semana activo, 2/4/8/12 semanas seguidas, Mês perfeito, Volta por cima, Regresso, Madrugador, Feriado no ginásio (feriados de Moçambique), Aniversário activo, 30/100/180/365 dias de jornada, Superação, Hat-trick (3 recordes no mesmo treino) e Mais do que o plano.
- **Natação**: 1,5 km e 30 minutos sem parar, Só crawl 4/8/16, Descanso de atleta, 1,5 km e 2 km num treino, Teste 350/400/500 m, Ritmo abaixo de 3:00 e 2:30, Piscina rápida (30 s) e relâmpago (25 s), Água fria e Mês aquático.
- **Caminhada e corrida**: 5 km a caminhar, 1/5/10/20 minutos a correr, 5 e 10 km a correr, Maratona acumulada.
- **Coração**: Coração mais forte, Semana de fogo, Fornalha e Zona de queima.
- **Corpo e peso**: −25/−30/−40 kg, abaixo de 130/120/110 kg, IMC abaixo de 45/40/35, gordura abaixo de 40/35/30%, −10 e −20 kg de massa gorda, visceral abaixo de 15/12 e zona saudável, Músculo protegido, Pesagem fiel 4/8/12 e Um número abaixo.
- Dentro de cada grupo, as conquistas já ganhas aparecem primeiro.
- Novos campos opcionais nos dados: `marcos` (registos que o Bruno conta no chat, como sexta sem copos ou roupa um número abaixo), `perfil.aniversario`, `crawlBloco`, `blocoTempo` e `corridaSeguida`.
- A conquista "Abaixo dos 140" passou a ter outro identificador interno, sem efeito para o Bruno.

## v1.7.1 — 10 Nov 2026
Privacidade, a pedido do Bruno.
- Removida a conquista "Sem desculpas" e todas as referências a dias de medicação na app (avisos no Início e nos Treinos), para não aparecerem em imagens partilhadas nem em capturas de ecrã.

## v1.7.0 — 9 Nov 2026
Cores das conquistas por tipo de exercício e imagem de evolução geral (a pedido do Bruno).
- **Uma cor por categoria**, para se perceber logo de que tipo é cada conquista. Dourado: Gerais (início, consistência, número de treinos). Azul: Natação. Verde-lima: Caminhada e corrida. Laranja: Musculação. Magenta: Crossfit. Violeta: Padel. Vermelho-coral: Coração (em qualquer exercício). Verde-água: Corpo e peso.
- Legenda das cores no topo das Conquistas e uma bolinha com a cor ao lado do nome de cada grupo. Só aparecem as categorias que já têm conquistas; Musculação, Crossfit e Padel aparecem sozinhas quando entrarem esses treinos.
- As categorias passam a viver num registo único (`CATS`): para um exercício novo basta acrescentar uma entrada, sem mexer nos ecrãs.
- Conquistas reorganizadas: Semana completa e Sem desculpas passam a Gerais; Primeira caminhada passa a Caminhada e corrida; o plano de 5 semanas passa a Natação ("Plano de natação completo").
- Novas conquistas gerais: **Início da jornada** (primeiro treino de qualquer tipo), **10, 25 e 50 treinos**.
- Imagem "Partilhar a minha evolução": o título passa a **Treino e exercício · desde 10 Out** (já não é só natação); a 2.ª caixa mostra o **total nadado** em vez das piscinas do último treino; "Actualizado a" passa a ser a data do último registo (treino ou pesagem) e não o dia em que se carrega no botão.

## v1.6.0 — 9 Nov 2026
Novo segmento **Evolução** no separador Progresso, ao lado de Corpo e Treinos.
- **Conquistas** ao estilo das medalhas do Apple Watch, em 4 grupos: Natação, Consistência, Coração e Peso (29 ao todo). As conquistadas aparecem a cores com a data; as que faltam aparecem a cinzento com o que falta (ex.: "Faltam 125 m"). São calculadas automaticamente a partir dos treinos e pesagens.
- Tocar numa medalha abre-a em grande, com a descrição, a data e o botão **Partilhar esta conquista**.
- **Recordes pessoais**: mais piscinas num treino, treino mais longo, mais tempo a nadar, maior bloco sem parar, piscina de crawl mais rápida, menos tempo parado, teste de 10 minutos, mais calorias, frequência cardíaca média mais baixa, semana com mais metros e maior perda de peso numa semana.
- **Treino a treino**: tabela dos últimos 4 treinos lado a lado, com o melhor de cada linha a negrito.
- Gráficos de tendência: tempo parado, frequência cardíaca média e piscinas por treino.
- Botão **Partilhar a minha evolução**: cria uma imagem (1080×1350) com os números principais, as últimas conquistas e os recordes, e abre a folha de partilha do iPhone (guardar nas Fotos, WhatsApp, etc.).
- Novos campos nos treinos: tempo parado, maior bloco sem parar e piscina de crawl mais rápida.
- "FC" passa a aparecer por extenso como **frequência cardíaca** em toda a app.
- Correcção: o texto do teste de 10 minutos dizia 28 Nov; passa a 30 Nov.

## v1.5.0 — 9 Nov 2026
Novos dias de treino a pedido do Bruno: natação à **segunda, quarta e sexta** a partir de 9 Nov.
- A sessão 3 (Resistência), que ficou por fazer no sábado 7 Nov, passa para segunda 9 Nov; as sessões seguintes seguem em segunda/quarta/sexta até ao novo teste, que passa para **segunda 30 Nov**.
- Caminhadas opcionais passam para **terça e sábado** (até 8 Nov continuam a aparecer à quarta e ao domingo, como estavam).
- Plano e gráficos de semanas passam a ter 5 semanas (a 5.ª é só a do novo teste); título do separador Plano passa a "Plano de natação".

## v1.4.0 — 6 Nov 2026
Cartão do corpo no Início pensado para motivar.
- Passa a chamar-se **"O meu progresso"** e mostra em destaque os **kg perdidos no total** desde a primeira pesagem (10 Out), com o peso actual ao lado.
- **Mini-gráfico do peso** desde 10 Out, com o ponto de partida e a última pesagem.
- Três mini-cartões novos: **% da meta** (com anel de progresso até aos 100 kg), **semanas seguidas a descer** e **kg perdidos por semana, em média**. Substituem a gordura perdida, a % de gordura e a gordura visceral, que continuam no separador Progresso.

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
