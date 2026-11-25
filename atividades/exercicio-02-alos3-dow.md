# Exercício 2 — ALOS3 (Allos) · Tendências de Dow

**Boleta:** Trade002.xlsx · **Ferramenta:** TradingView
**Janela de observação:** 01/10/2025 a 30/10/2026
**Quantidade:** 1 ação por operação · **Dias:** corridos
**Planilha preenchida:** [exercicio-02-alos3-dow.xlsx](exercicio-02-alos3-dow.xlsx) (com fórmulas e aba de dados)

## Fonte dos dados
Cotações diárias da **ALOS3.SA no Yahoo Finance** (fechamento sem ajuste de proventos), salvas em [dados/alos3-diario-2025-09-a-2026-10.csv](dados/alos3-diario-2025-09-a-2026-10.csv).
Elas batem com as anotações do exercício 1: fechamento de 30/10/2025 = 24,73; máxima de 21/10/2026 = 36,26 (a data está confirmada); fechamento de 30/10/2026 = 23,50. A mínima de 30/10/2026 aparece como **23,00** no Yahoo (no papel está 22,99: diferença de arredondamento entre fontes).

> ⚠️ Esta janela começa em **01/10/2025**, um mês antes da do exercício 1 (30/10/2025). Por isso o B&H e a Teórica mudam.

## Boleta

| | Compra | Preço | Venda | Preço | Dias | Lucro R$ | % |
|---|---|---|---|---|---|---|---|
| **B&H** | 01/10/2025 | 25,61 | 30/10/2026 | 23,50 | 394 | −2,11 | **−8,24%** |
| **Teórica** | 15/10/2025 | 23,44 | 21/10/2026 | 36,26 | 371 | +12,82 | **+54,69%** |
| **Dow1** | 03/11/2025 | 24,97 | 22/12/2025 | 27,38 | 49 | +2,41 | +9,65% |
| **Dow2** | 12/01/2026 | 29,43 | 19/01/2026 | 28,44 | 7 | −0,99 | −3,36% |
| **Dow3** | 01/04/2026 | 30,98 | 22/04/2026 | 32,86 | 21 | +1,88 | +6,07% |
| **Dow4** | 25/06/2026 | 27,69 | 07/07/2026 | 27,17 | 12 | −0,52 | −1,88% |
| **Dow5** | 01/09/2026 | 27,32 | 26/10/2026 | 26,19 | 55 | −1,13 | −4,14% |
| **Pay off** | | **140,39** | | 142,04 | **144** | **+1,65** | **+1,18%** |

**Pay off** = lucro das 5 operações ÷ investimento total = 1,65 ÷ 140,39 = **1,18%**.

- **B&H:** compra no fechamento do 1º pregão da janela, venda no fechamento do último.
- **Teórica:** compra na **mínima** antes do topo (15/10/2025, 23,44) e venda na **máxima** da janela (21/10/2026, 36,26). A mínima de 30/10/2026 (23,00) vem *depois* do topo, então não serve para a compra. Se o professor quiser só fechamentos: 23,79 (14/10/2025) → 35,83 (09/10/2026) = +50,61%.

## A regra usada (Teoria de Dow)
Para as operações serem verificáveis, usei uma regra fixa, aplicada pregão a pregão:

1. **Topo** = máxima maior que as dos 2 pregões antes e dos 2 depois. **Fundo** = mínima menor que as dos 2 pregões antes e dos 2 depois. (Só se "sabe" que é topo/fundo 2 pregões depois.)
2. **Compra:** depois de um **fundo ascendente** (fundo mais alto que o anterior), o preço **fecha acima do último topo**. É a confirmação de topos e fundos ascendentes.
3. **Venda:** o preço **fecha abaixo do último fundo**. A sequência de fundos ascendentes foi quebrada (fim da tendência).

## Operação por operação (para conferir no TradingView)

| Op. | Por que comprou | Por que vendeu |
|---|---|---|
| Dow1 | Fundos 22/10 (24,04) → 30/10 (24,29), ascendente; fechou 24,97 em 03/11, acima do topo de 27/10 (24,96). | Fechou 27,38 em 22/12, abaixo do fundo de 17/12 (27,42). |
| Dow2 | Fundos 22/12 (27,21) → 08/01 (28,64); fechou 29,43 em 12/01, acima do topo de 23/12 (28,41). | Fechou 28,44 em 19/01, abaixo do fundo de 13/01 (28,49). Falso rompimento. |
| Dow3 | Fundos 20/03 (28,58) → 30/03 (28,70); fechou 30,98 em 01/04, acima do topo de 25/03 (30,65). | Fechou 32,86 em 22/04, abaixo do fundo de 16/04 (33,05). |
| Dow4 | Fundos 16/06 (26,17) → 23/06 (26,44); fechou 27,69 em 25/06, acima do topo de 22/06 (27,16). | Fechou 27,17 em 07/07, abaixo do fundo de 30/06 (27,50). |
| Dow5 | Fundos 18/08 (25,20) → 28/08 (25,93); fechou 27,32 em 01/09, acima do topo de 26/08 (26,80). | Stop no fundo de 14/10 (33,76), mas em **26/10/2026** a ação abriu em **gap de baixa** (fechou 35,14 em 23/10 e abriu 24,01, com volume de 27 milhões). Venda no fechamento do dia, 26,19. |

## Comparação

| Estratégia | Resultado | Dias posicionada |
|---|---|---|
| Teórica (teto) | +54,69% | 371 |
| Dow (5 operações) | **+1,18%** | 144 |
| Buy and Hold | −8,24% | 394 |
| *S&R (exercício 1, outra janela)* | *+17,57%* | *130* |

## Observações / o que aprender
- **Dow ganhou do B&H** (+1,18% × −8,24%) ficando posicionada só ~37% do tempo, mas ficou bem abaixo do S&R do exercício 1.
- **Dow entra atrasado e sai atrasado:** espera o topo ser rompido para comprar e o fundo ser perdido para vender. Em tendências longas isso é ótimo; em **lateralidade** (jan/26, jun–jul/26) gera falsos sinais (Dow2 e Dow4).
- **O gap de 26/10/2026 é a grande lição:** pela regra a Dow5 estaria com lucro de ~+24% (stop em 33,76), mas o gap pulou o stop. Nenhuma linha de tendência protege contra uma queda de ~25% em um dia. Sem o gap, o pay off da série seria bem positivo.
- **Volume:** a alta de out/26 veio com volume muito acima da média (22 mi em 05/10), confirmando a tendência; o colapso de 26/10 veio com volume ainda maior (27 mi), típico de **pânico**.
- Esta é a versão **mecânica**. Se você marcar os topos e fundos "no olho" no gráfico, os sinais podem mudar um ou dois pregões; o importante é justificar com topo/fundo ascendente e com a quebra.

## Como conferir no TradingView
1. ALOS3, diário, de 01/10/2025 a 30/10/2026.
2. Para cada Dow, marque os dois fundos e o topo da tabela acima (ferramenta de linha horizontal) e veja o candle de compra fechar acima do topo.
3. Marque o fundo da coluna "Por que vendeu" e veja o candle de venda fechar abaixo dele.
4. Se algum preço diferir em centavos, use o do TradingView e atualize a planilha (as fórmulas recalculam).
