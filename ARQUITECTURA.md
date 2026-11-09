# Arquitectura — Treino Bruno

## Regra principal (pedido do Bruno, 9 Nov 2026)

A natação é só o início. A seguir vêm as caminhadas, que vão evoluir para corrida, depois musculação, talvez crossfit, e padel.

**Qualquer alteração à app tem de a deixar preparada para receber novos tipos de exercício sem reestruturar tudo.** Antes de escrever código novo, pergunta: "isto funciona igual quando houver corrida ou musculação?"

## Como deve crescer

O modelo de dados já é genérico. Cada registo em `atividades` tem um `tipo` (`natacao`, `caminhada`, …) e campos próprios desse tipo. Um tipo novo não muda pesagens, metas nem perfil.

O objectivo é que acrescentar um tipo novo seja **acrescentar uma entrada num registo de tipos** e não mexer em cada ecrã. A ideia é um objecto `TIPOS` em que cada tipo diz:

- **Identidade:** `nome`, `ico`, `cor`.
- **Resumo e tabela:** `resumo(a)`, para o cartão do dia, e `linha(a)`, para a tabela de actividades.
- **Agregados:** `stats(lista)`, com os totais por período.
- **Evolução:** `recordes(lista)` e `conquistas(lista)`.
- **Plano:** `plano`, opcional, com as sessões planeadas desse tipo.

Os ecrãs (Início, Treinos, Progresso, Evolução, Plano) percorrem `TIPOS` em vez de terem `if (tipo === "natacao") … else …`.

### Exemplos de campos por tipo (quando chegarem)

| Tipo | Campos típicos |
|---|---|
| Natação | distância, piscinas, ritmo /100 m, estilos, tempo parado, maior bloco |
| Caminhada / corrida | distância (km), ritmo /km, desnível, cadência |
| Musculação | exercícios × séries × repetições × carga, volume total |
| Crossfit | WOD, formato (AMRAP/EMOM/For time), rondas ou tempo |
| Padel | duração, sets/resultado, parceiro, intensidade |

Os campos comuns a todos (data, início/fim, duração, frequência cardíaca média e máxima, zonas, kcal e sensação) devem ser tratados uma só vez, de forma igual para todos os tipos.

## Pontos actuais ainda específicos da natação (v1.6.0)

Ficam para generalizar quando entrar o próximo tipo de exercício:

- `swims()` e `walks()`, mais ternários `tipo === "natacao" ? … : …` no Início, nos Treinos e na tabela de actividades.
- `agenda(d)` tem os dias de caminhada fixos (terça e sábado). O plano semanal deve passar a ser uma lista de dias por tipo.
- `PLANO` e o separador Plano são só de natação. Devem passar a ter um plano por tipo (ou sessões com `tipo`).
- `recordes()` e `conquistas()` (Evolução) são calculados só a partir dos treinos de natação e das pesagens. As categorias das medalhas (`MED_CAT`) já são extensíveis: acrescentar "Corrida", "Força" ou "Padel" é acrescentar uma cor e uma entrada.
- Os gráficos e tiles de Treinos estão divididos em "Natação" e "Caminhadas". Devem ser gerados a partir de `TIPOS`.
