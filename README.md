# Micha do Terreno

### Análise exploratória das propostas do OGE em Angola (2012–2024)

Este repositório contém o código, os dados processados e os artefactos visuais do projeto **Micha do Terreno**, uma análise exploratória e descritiva das **propostas do Orçamento Geral do Estado (OGE)** de Angola, com foco na **distribuição provincial e regional** dos recursos entre 2012 e 2024.

O projeto privilegia **transparência metodológica**, **reprodutibilidade** e **visualização de dados**, não avaliando execução orçamental nem impacto económico.

---

## Objetivo analítico

* Extrair e estruturar dados orçamentais a partir de fontes oficiais em PDF
* Construir um dataset provincial consistente para o período 2012–2024
* Agregar dados por província, região e ano
* Identificar padrões, assimetrias e anos excecionais
* Produzir visualizações claras e comparáveis

---

## Fonte dos dados

* Ministério das Finanças de Angola
* Documentos: *Resumos da Despesa por Local* (PDF)
* Tipo de dado: OGE **proposto**
* Unidade monetária: Kwanzas (Kz), valores nominais

Anos **2025 e 2026** não são incluídos devido à nova divisão político administrativa, que introduz novas províncias e quebra a comparabilidade temporal.

---

## Pipeline de dados

1. **Extração**

   * Download manual dos PDFs oficiais
   * Extração tabular a partir de PDFs

2. **Limpeza**

   * Normalização de nomes das províncias
   * Conversão de valores monetários
   * Verificação de inconsistências entre anos

3. **Transformação**

   * Estruturação em formato tabular (long format)
   * Agregação por:

     * Província
     * Região
     * Ano
   * Cálculo de totais e percentagens

4. **Análise**

   * Estatísticas descritivas
   * Identificação de outliers e anos excecionais
   * Comparações interprovinciais e regionais

5. **Visualização**

   * Gráficos de linhas, colunas, mapas de árvore
   * Escalas em 10⁹ e 10¹² Kz
   * Ênfase em leitura visual e comparabilidade

---

## Estrutura do repositório

```
micha-do-terreno/
│
├── data/
│   ├── raw/              # PDFs originais
│   ├── intermediate/     # Dados extraídos e limpos
│   └── processed/        # Datasets finais usados nos gráficos
│
├── notebooks/            # Exploração e análise
│
├── scripts/              # Extração, limpeza e transformação
│
├── visuals/              # Gráficos finais e figuras
│
├── docs/                 # Texto explicativo e metodologia
│
└── README.md
```

---

## Regiões utilizadas na análise

* Norte: Cabinda, Zaire, Uíge, Lunda Norte
* Centro: Malanje, Bié, Huambo
* Sul: Namibe, Huíla, Cunene, Cuando Cubango
* Leste: Lunda Sul, Moxico
* Oeste: Luanda, Bengo, Cuanza Norte, Cuanza Sul, Benguela

---

## Premissas e limitações

* Valores nominais em kwanzas
* Sem ajuste inflacionário ou cambial
* Análise restrita ao OGE proposto
* Comparações internacionais apenas indicativas
* Alterações administrativas não incorporadas

---

## Reprodutibilidade

Todo o processo foi desenhado para permitir:

* Reexecução do pipeline a partir dos PDFs
* Atualização futura com novos anos
* Extensão para análise da execução orçamental

Dependências, versões e instruções de execução podem ser adicionadas conforme evolução do projeto.

---

## Licença e uso

Este repositório é disponibilizado para fins analíticos, educativos e de investigação.
Reutilização permitida com atribuição.
