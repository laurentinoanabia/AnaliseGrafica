# Exercício 1 — ALOS3 (Allos)

**Ferramenta:** TradingView
**Janela de observação:** 30/10/2025 a 30/10/2026
**Quantidade:** 1 ação por operação

## Enunciado (resumo)
1. Identificar as tendências **primária, secundária e terciária** e suas **fases**.
2. Relacionar **volume** com a tendência.
3. Identificar **congestões** (acumulação/distribuição) e o **ângulo** das tendências.
4. Comparar estratégias: **Buy and Hold**, **Teórica** (compra no mínimo, venda no máximo) e **Suporte e Resistência / Tendências de Dow** (5 operações).

## Referências de preço
| Referência | Data | Preço (R$) |
|---|---|---|
| Fechamento inicial | 30/10/2025 | 24,73 |
| Máxima da janela | 21/10/2026 | 36,26 |
| Mínima | 30/10/2026 | 22,99 |
| Fechamento final | 30/10/2026 | 23,50 |

## Boleta

### Buy and Hold
| Compra | Preço | Venda | Preço | Dias | Lucro (R$) | % |
|---|---|---|---|---|---|---|
| 30/10/2025 | 24,73 | 30/10/2026 | 23,50 | 365 | −1,23 | −4,97% |

### Teórica
| Compra | Preço | Venda | Preço | Dias | Lucro (R$) | % |
|---|---|---|---|---|---|---|
| 30/10/2025 | 24,73 | 21/10/2026 | 36,26 | 356 | +11,53 | **46,62%** |

> Na boleta em papel está 49,62%; o correto é 11,53 ÷ 24,73 = **46,62%**.

### Suporte e Resistência (5 operações)
| Op. | Compra | Preço | Venda | Preço | Dias | Lucro (R$) | % |
|---|---|---|---|---|---|---|---|
| S&R1 | 30/10/2025 | 24,73 | 14/11/2025 | 28,81 | 15 | 4,08 | 16,50% |
| S&R2 | 22/12/2025 | 27,38 | 27/02/2026 | 32,69 | 67 | 5,31 | 19,39% |
| S&R3 | 31/03/2026 | 30,34 | 17/04/2026 | 33,80 | 17 | 3,46 | 11,40% |
| S&R4 | 18/08/2026 | 25,37 | 08/09/2026 | 29,22 | 21 | 3,85 | 15,18% |
| S&R5 | 28/09/2026 | 28,57 | 08/10/2026 | 35,83 | **10** | 7,26 | **25,41%** |
| **Total** | | 136,39 | | | **130** | **+23,96** | **17,57%** |

> Correções em relação à boleta em papel: S&R5 = **25,41%** (estava 25,88%) e **10 dias** (estava 11), o que leva o total a **130 dias** (estava 131).

**Pay off** = lucro das séries ÷ investimento total das séries = 23,96 ÷ 136,39 = **17,57%**.

## Comparação
| Estratégia | Resultado | Dias posicionada |
|---|---|---|
| Teórica (limite máximo) | +46,62% | 356 |
| Suporte e Resistência | **+17,57%** | 130 |
| Buy and Hold | −4,97% | 365 |

**Conclusão:** as 5 operações de S&R superaram o Buy and Hold em mais de 22 pontos percentuais, ficando posicionadas só ~36% do tempo. A estratégia Teórica é inalcançável na prática (exige acertar o mínimo e o máximo exatos) e serve de teto de referência.

## A completar
- [ ] Tendência primária, secundária e terciária no gráfico (com datas)
- [ ] Fases (acumulação, alta sensível, euforia / distribuição, baixa sensível, pânico)
- [ ] Volume × tendência
- [ ] Congestões e ângulos
- [ ] Prints do TradingView em `atividades/img/`
