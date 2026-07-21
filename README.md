# Teste de Temperamentos

App web estático (uma página, zero dependências) que aplica o teste clássico dos
quatro temperamentos: **Sanguíneo, Colérico, Melancólico e Fleumático**.

## Regra de pontuação

Fiel à planilha original em Excel:

| Fase | Temperamento | Fórmula original |
|------|--------------|------------------|
| Fase 1 | Sanguíneo   | `=COUNTIF(D16:D35,TRUE)` |
| Fase 2 | Colérico    | `=COUNTIF(D12:D31,TRUE)` |
| Fase 3 | Melancólico | `=COUNTIF(D12:D31,TRUE)` |
| Fase 4 | Fleumático  | `=COUNTIF(D12:D31,TRUE)` |

- Pontos de cada temperamento = número de respostas **Sim** na sua fase (0 a 20)
- Percentual = pontos ÷ total de “Sim” do teste (`=C14/C23`)
- Resultado final = **combinação do 1º com o 2º maior**, entre as 12 possíveis

## Rodar localmente

```bash
python3 -m http.server 8899
```

## Créditos

Fonte original: planilha de Marcos Turim (Turim Admin) · conteúdo de educamais.com
Ferramenta de autoconhecimento — não substitui avaliação psicológica.
