# Painel de Inteligência da Cana-de-Açúcar · MS

Conab · Superintendência Regional de Mato Grosso do Sul (SUREG-MS) · SEGEO-MS

## O que tem neste repositório
| Arquivo | Para que serve |
|---|---|
| `index.html` | O painel. Só muda quando o painel ganha alguma alteração. |
| `dados/agricola.xls` | Série histórica Conab da cana · Agrícola (área, produtividade, produção) |
| `dados/industria.xls` | Série histórica Conab da cana · Indústria (açúcar, etanol, ATR, etanol de milho) |
| `dados/area_total.xls` | Série histórica Conab da cana · Área Total (renovação e expansão) |
| `dados/frete.txt` | Pesquisa de frete da Conab (rotas de MS) |

## Como atualizar a cada levantamento (sem mexer no código)
1. Baixe as três planilhas no site da Conab: gov.br/conab → Informações agropecuárias → Safras → Séries históricas → Cana-de-açúcar (Agrícola, Indústria e Área Total).
2. No GitHub, abra a pasta `dados`, clique em **Add file → Upload files** e envie as três planilhas.
   - Pode manter o nome original da Conab (`CanaSerieHist - Agricola.xls` etc.) ou renomear para `agricola.xls`, `industria.xls` e `area_total.xls`.
   - Se usar os nomes curtos, o GitHub substitui os antigos. Se usar os nomes originais, apague os arquivos de nome curto para não haver duas versões.
3. Clique em **Commit changes**. Em 1 a 2 minutos o painel mostra o levantamento novo, inclusive o rótulo ("estimativa de novembro de 2026, 3º levantamento"), que é lido da nota da própria planilha.
4. O frete é atualizado do mesmo jeito, substituindo `dados/frete.txt`.

Para conferir: aba **Notas e fontes → Versão** mostra de onde o painel leu cada dado e a data do arquivo.
Se uma planilha estiver com problema, o painel ignora só aquela e usa a cópia que vem dentro do `index.html`.

## Publicação (GitHub Pages)
*Settings → Pages → Deploy from a branch → main → / (root)*. Endereço: `https://<sua-conta>.github.io/painel-cana-ms/`.

## Importante
Este repositório é público. **Nunca envie para cá as planilhas das usinas.**
O clima é lido do painel "Levantamento de Safras MS" (atualização diária automática).
