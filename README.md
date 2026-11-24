# BiblioPI – Repositório Digital

## 1. Identificação

| Campo | Valor |
|---|---|
| Unidade curricular | Processamento de Informação |
| Curso | Licenciatura em Engenharia Informática, ISPGAYA |
| Ano letivo | 2026/2027 |
| Docente | Henrique Teixeira |
| Grupo | 2 |
| Subtema | Cultura Pop |
| Entrega | 09/12/2026 |

| N.º de aluno | Nome completo |
|---|---|
| 2024104849 | David Queirós Monteiro Carido |
| 2024103850 | Luis Filipe Gonçalves Pereira |
| 2024103637 | Tomás Daniel Oliveira Pereira |

## 2. Estrutura de pastas

```
PdI_Grupo2/
├── README.md
├── registo_horas.csv
├── declaracao_honra.md
├── declaracao_honra_assinada.pdf
├── teoria/
│   └── respostas.md
├── t01_registo/
│   ├── inquerito_codebook.md
│   ├── inquerito_dados.csv
│   └── analise_inquerito.xlsx
├── t02_linguagem/
│   ├── ambiguidade.md
│   ├── regras.xml
│   └── regras.json
├── t03_conceitos/
│   ├── mapa_mental.jpg
│   └── mapa_concetual.jpg
├── t04_compressao/
│   ├── compressao.md
│   ├── arvore_comum.xml
│   └── arvore_grupo.json
├── t05_xml/
│   ├── catalogo.xml
│   ├── catalogo.xsd
│   ├── dc_subset.xsd
│   ├── adm.xsd
│   ├── validacao.md
│   └── testes/
│       ├── nao_bem_formado.xml
│       └── catalogo_invalido.xml
├── t06_json/
│   ├── catalogo.json
│   ├── catalogo.schema.json
│   ├── equivalencia_xml_json.md
│   └── testes/
│       ├── catalogo_invalido.json
│       └── sintaxe_invalida.json
├── t07_portal/
│   ├── index.html
│   ├── catalogo.html
│   ├── pesquisa.html
│   ├── requisicao.html
│   └── documentos/
│       ├── doc-0001.html
│       ├── doc-0002.html
│       └── doc-0003.html
├── t08_armazenamento/
│   ├── armazenamento.md
│   └── plano_backup.json
└── evidencias/
    └── capturas PNG das validações (prefixo da tarefa, ex.: t05_valido.png)
```

## 3. Como validar cada artefacto

Todos os ficheiros de texto estão em UTF-8. As capturas de cada validação estão na pasta `evidencias/`, com o prefixo da tarefa.

| Artefacto | Ferramenta | Passos | Evidência |
|---|---|---|---|
| `t01_registo/inquerito_dados.csv` | Excel ou LibreOffice Calc | Importar com Dados → Texto/CSV, origem 65001: Unicode (UTF-8) e delimitador ponto e vírgula. Confirmar 36 linhas, 46 colunas e acentos corretos. | `t01_csv.png` |
| `t01_registo/analise_inquerito.xlsx` | Excel ou LibreOffice Calc | Abrir as folhas `limpeza` e `estatisticas` e ativar Fórmulas → Mostrar Fórmulas (Ctrl + `). Confirmar que não há valores escritos à mão nem macros. | `t01_formulas.png` |
| `t02_linguagem/regras.xml` | VS Code com a extensão XML (Red Hat) ou validador XML em linha | Abrir o ficheiro e confirmar que não há erros de bem-formação. | `t02_regras_xml.png` |
| `t02_linguagem/regras.json` | jsonschemavalidator.net | Colar o JSON à direita, com o esquema `{}` à esquerda, e confirmar que não há erros de sintaxe. | `t02_regras_json.png` |
| `t03_conceitos/*.jpg` | Visualizador de imagens | Mapa mental: tema central, pelo menos 6 ramos e no máximo 4 níveis. Mapa concetual: pelo menos 15 proposições conceito–ligação–conceito. | – |
| `t04_compressao/arvore_comum.xml` | VS Code com a extensão XML | Confirmar a bem-formação. | `t04_arvore_xml.png` |
| `t04_compressao/arvore_grupo.json` | jsonschemavalidator.net | Colar o JSON à direita, com o esquema `{}` à esquerda, e confirmar que não há erros de sintaxe. | `t04_arvore_json.png` |
| `t05_xml/catalogo.xml` | VS Code com a extensão XML (Red Hat) | Abrir a pasta `t05_xml/` inteira, para que o `catalogo.xsd` encontre o `dc_subset.xsd` e o `adm.xsd` importados. Confirmar 0 erros no separador Problemas. | `t05_valido.png` |
| `t05_xml/testes/nao_bem_formado.xml` | VS Code com a extensão XML | Registar a mensagem de cada um dos 3 erros. | `t05_nao_bem_formado_1.png` a `_3.png` |
| `t05_xml/testes/catalogo_invalido.xml` | VS Code com a extensão XML | Registar as mensagens dos 6 ou mais erros de validade, cada um contra uma regra diferente do XSD. | `t05_invalido.png` |
| `t06_json/catalogo.json` | jsonschemavalidator.net (draft 2020-12) | Colar o `catalogo.schema.json` à esquerda e o `catalogo.json` à direita; confirmar «No errors found». | `t06_valido.png` |
| `t06_json/testes/catalogo_invalido.json` | jsonschemavalidator.net | Mesmo esquema; registar os 6 ou mais erros. | `t06_invalido.png` |
| `t06_json/testes/sintaxe_invalida.json` | jsonschemavalidator.net | Registar a mensagem do erro de sintaxe. | `t06_sintaxe.png` |
| `t07_portal/**/*.html` | W3C Nu HTML Checker (validator.w3.org/nu) | Escolher «File upload», enviar cada uma das 7 páginas e confirmar «Document checking completed. No errors or warnings to show.» | `t07_index.png`, `t07_catalogo.png`, … (uma por página) |
| `t08_armazenamento/plano_backup.json` | jsonschemavalidator.net | Colar o JSON à direita, com o esquema `{}` à esquerda, e confirmar que não há erros de sintaxe. | `t08_plano_json.png` |

Dois cuidados na validação:

- **XML com `xs:import`:** muitos validadores em linha aceitam só um XSD e não conseguem abrir o `dc_subset.xsd` e o `adm.xsd` importados pelo `catalogo.xsd`. Por isso, o `catalogo.xml` é validado no VS Code, com os quatro ficheiros na mesma pasta.
- **Erros de bem-formação:** os analisadores XML param no primeiro erro fatal. Para documentar os 3 erros do `nao_bem_formado.xml`, corrige-se um de cada vez numa cópia de trabalho e regista-se a mensagem seguinte.

## 4. Distribuição do trabalho

A parte teórica (P1–P11) foi feita por todos os elementos em conjunto, as restantes tarefas T1 a T9 foram divididas pelos três elementos, ficando cada um responsável por três. Todas as horas estão registadas no `registo_horas.csv`.
 
| Elemento | Tarefas da sua responsabilidade | Parte teórica |
|---|---|---|
| 2024104849 - David Queirós Monteiro Carido | T3, T4, T6 | P1–P11, em conjunto |
| 2024103850 - Luis Filipe Gonçalves Pereira | T1, T7, T9 | P1–P11, em conjunto |
| 2024103637 - Tomás Daniel Oliveira Pereira | T2, T5, T8 | P1–P11, em conjunto |

## 5. Verificação cruzada

Cada documento tem de ter o mesmo identificador, o mesmo título e a mesma classificação (tipo e assunto) em todos os sítios onde aparece. A verificação foi feita documento a documento, comparando:

1. o atributo `id` e os elementos `dc:title`, `dc:subject` e o tipo no `catalogo.xml`;
2. as chaves equivalentes no `catalogo.json`;
3. a linha do documento no `catalogo.html` e, quando existe, a sua página de detalhe em `documentos/`;
4. a entrada do documento no índice de pesquisa.

Na tabela, «OK» significa que o valor coincide com o do `catalogo.xml`.

| ID | Título | Tipo | `catalogo.json` | `catalogo.html` | Página de detalhe | Índice |
|---|---|---|---|---|---|---|
| DOC-0001 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | [ ] | [ ] |
| DOC-0002 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | [ ] | [ ] |
| DOC-0003 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | [ ] | [ ] |
| DOC-0004 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0005 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0006 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0007 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0008 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0009 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0010 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0011 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0012 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0013 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0014 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0015 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0016 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0017 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0018 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0019 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |
| DOC-0020 | [PREENCHER] | [PREENCHER] | [ ] | [ ] | – | [ ] |

Discrepâncias encontradas e como foram corrigidas: [PREENCHER, ou «nenhuma»].

## 6. Limitações conhecidas

**T1 - Recolha, registo e tabulação de dados**

- A amostra é de conveniência: 36 respostas recolhidas em dois dias, sobretudo no Grande Porto (Porto e Maia somam 17). Os resultados descrevem estes respondentes e não a população em geral.
- 22 das 36 pessoas nunca usam bibliotecas, por isso as perguntas 11 a 16 têm só 14 respostas.
- A opção «Trabalhor/Estudante» da pergunta 3 tinha uma gralha no formulário. As respostas foram codificadas como trabalhador-estudante.
- A localidade «Caramulo» foi substituída pelo concelho de Tondela, a que pertence. A decisão está documentada no codebook.

**T2 - Linguagem natural, ambiguidade e representação estruturada**

**T3 - Concetualização: mapa mental e mapa concetual**

**T4 - Compressão sem perdas: Huffman e entropia**

**T5 - Catálogo XML**

**T6 - Catálogo JSON e equivalência XML ↔ JSON**

**T7 - Portal HTML5 semântico, acessível e validado**

**T8 - Armazenamento e backup**

**T9 - Integração, README e verificação final**

## Fontes

JSON Schema Validator. (s.d.). *JSON Schema validator*. https://www.jsonschemavalidator.net/
W3C. (s.d.). *Nu Html Checker*. https://validator.w3.org/nu/
