# ♻️ Sistema de Captação de Óleo para Reciclagem

Projeto de extensão da **Uniara** (Engenharia da Computação), desenvolvido em grupo em **linguagem C**.
O sistema registra os lotes de óleo coletados para reciclagem e gera relatórios das coletas.

## Funcionalidades

| Opção | O que faz |
|---|---|
| Importar lote | Lê um arquivo de coleta (`dd_mm_aaaa.txt`) com dia, mês, ano e litros, e grava os registros |
| Excluir lote | Remove um lote já importado, com **backup automático** antes da exclusão |
| Relatório geral | Lista todas as coletas e exporta para `listagem.csv` |
| Relatório mensal | Soma os litros por mês e exporta para `mensal.csv` |

Os dados ficam persistidos em **arquivo binário** (`dados.bin`), usando `struct` e leitura/escrita com `fread`/`fwrite`.

## Estrutura

```
main.c        menu principal
coletas.c/.h  regras do sistema (importação, exclusão e relatórios)
pss.c/.h      biblioteca de entrada de dados do Prof. Saulo Santos (BSD-3)
```

## Como compilar e rodar

```bash
gcc main.c coletas.c pss.c -o projeto
./projeto
```

Os arquivos `01_06_2026.txt` e `15_06_2026.txt` são exemplos de lote para testar a importação.

## Conceitos praticados

Structs · manipulação de arquivos texto, binário e CSV · modularização em `.c`/`.h` · validação de entrada · Git em equipe

---

Projeto acadêmico · Leonardo Cabrini Mauro e equipe · [LinkedIn](https://www.linkedin.com/in/leonardo-cabrini-mauro-79b292355/)
