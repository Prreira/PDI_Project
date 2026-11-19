# Codebook do inquérito BiblioPI

## 1. Dicionário de dados

- Célula vazia = sem resposta
- `NA` = não aplicável

| Variável | Descrição | Tipo | Domínio | Codificação |
|---|---|---|---|---|
| `id` | Identificador do respondente | texto | R01–R36 | Atribuído pela ordem de chegada das respostas |
| `idade` | P1 – Idade | inteiro | 18–99 | Anos completos |
| `localidade` | P2 – Localidade de residência | texto | Concelhos de Portugal | Nome oficial do concelho |
| `situacao` | P3 – Situação principal | categórico | 1–5, 9 | 1 = Estudante; 2 = Trabalhador-estudante; 3 = Trabalhador por conta de outrem; 4 = Trabalhador independente; 5 = Sem atividade profissional; 9 = Outra |
| `livros_12m` | P4 – Livros lidos nos últimos 12 meses | inteiro | ≥ 0 | Número de livros |
| `genero` | P5 – Género literário preferido | categórico | 1–11, 99 | 1 = Romance / ficção literária; 2 = Policial / thriller / mistério; 3 = Fantasia / ficção científica; 4 = Romance histórico; 5 = Biografia / memórias; 6 = Não-ficção / ensaio; 7 = Técnico / académico; 8 = Banda desenhada / manga; 9 = Poesia; 10 = Autoajuda / desenvolvimento pessoal; 11 = Sem preferência; 99 = Outro |
| `formato` | P6 – Formato preferido | categórico | 1–3 | 1 = Papel; 2 = Digital; 3 = Ambos |
| `horas_semana` | P7 – Horas semanais de leitura | decimal | 0–168 | Horas por semana, com vírgula decimal |
| `lingua_pt`, `lingua_en`, `lingua_outra` | P8 – Línguas em que lê (escolha múltipla) | binário | 0 ou 1 | `lingua_pt` = Português; `lingua_en` = Inglês; `lingua_outra` = Outra. Em cada coluna: 1 = assinalou; 0 = não assinalou |
| `obt_compra`, `obt_biblioteca`, `obt_emprestimo`, `obt_digital`, `obt_outra` | P9 – Como obtém os livros (escolha múltipla) | binário | 0 ou 1 | `obt_compra` = Compro; `obt_biblioteca` = Requisito numa biblioteca; `obt_emprestimo` = Peço emprestados a amigos ou família; `obt_digital` = Plataformas digitais ou subscrições; `obt_outra` = Outra. Em cada coluna: 1 = assinalou; 0 = não assinalou |
| `freq_biblioteca` | P10 – Frequência de uso de bibliotecas | ordinal | 0–3 | 0 = Nunca; 1 = Menos de uma vez por mês; 2 = 1 a 3 vezes por mês; 3 = Uma vez por semana ou mais |
| `bib_municipal`, `bib_escolar`, `bib_digital`, `bib_outra` | P11 – Tipos de biblioteca usados (escolha múltipla) | binário | 0 ou 1, NA | `bib_municipal` = Municipal; `bib_escolar` = Da escola ou universidade; `bib_digital` = Biblioteca digital ou repositório online; `bib_outra` = Outra. Em cada coluna: 1 = assinalou; 0 = não assinalou |
| `doc_livro`, `doc_artigo`, `doc_tese`, `doc_relatorio`, `doc_dataset`, `doc_multimedia`, `doc_periodico` | P12 – Tipos de documento procurados (escolha múltipla) | binário | 0 ou 1, NA | `doc_livro` = Livros; `doc_artigo` = Artigos científicos; `doc_tese` = Teses e dissertações; `doc_relatorio` = Relatórios; `doc_dataset` = Conjuntos de dados; `doc_multimedia` = Recursos multimédia (vídeo, áudio, imagens); `doc_periodico` = Jornais e revistas. Em cada coluna: 1 = assinalou; 0 = não assinalou |
| `pesquisa_inicio` | P13 – Por onde começa a pesquisa | categórico | 1–6, NA | 1 = Pelo título; 2 = Pelo autor; 3 = Pelo assunto ou palavras-chave; 4 = Pelo ISBN ou DOI; 5 = Navego pelas categorias ou estantes; 6 = Peço ajuda a um funcionário |
| `facilidade` | P14 – Facilidade em encontrar o que procura | ordinal | 1–5, NA | 1 = Muito difícil … 5 = Muito fácil |
| `prob_irrelevante`, `prob_indisponivel`, `prob_sem_digital`, `prob_catalogo`, `prob_acentos`, `prob_nenhum` | P15 – Problemas encontrados (escolha múltipla) | binário | 0 ou 1, NA | `prob_irrelevante` = Resultados que não tinham nada a ver com o que procurava; `prob_indisponivel` = O documento existia mas estava indisponível ou emprestado; `prob_sem_digital` = Não havia versão digital; `prob_catalogo` = Catálogo confuso ou difícil de usar; `prob_acentos` = Nomes com acentos mal escritos ou símbolos estranhos; `prob_nenhum` = Nunca tive problemas. Em cada coluna: 1 = assinalou; 0 = não assinalou |
| `atraso` | P16 – Atrasos na devolução | categórico | 1–4, NA | 1 = Nunca requisitei; 2 = Nunca me atrasei; 3 = Uma ou duas vezes; 4 = Com frequência |
| `imp_pesquisa`, `imp_reserva`, `imp_digital`, `imp_aviso`, `imp_filtros`, `imp_recomend`, `imp_acessib` | P17 – Importância de cada funcionalidade (grelha) | ordinal | 1–5 | `imp_pesquisa` = Pesquisar o catálogo online; `imp_reserva` = Reservar e renovar empréstimos online; `imp_digital` = Ler ou descarregar documentos em formato digital; `imp_aviso` = Receber aviso antes do fim do prazo de empréstimo; `imp_filtros` = Filtrar resultados por tipo, ano e língua; `imp_recomend` = Recomendações de leitura; `imp_acessib` = Acessibilidade (leitor de ecrã, texto ampliado). Em cada coluna: 1 = Nada importante … 5 = Muito importante |
| `historico` | P18 – Aceita que se guarde o histórico de pesquisas | categórico | 1–3 | 1 = Sim; 2 = Só se for anonimizado; 3 = Não |
| `interesse_subtema` | P19 – Interesse em documentos sobre Cultura Pop | ordinal | 1–5 | 1 = Nenhum … 5 = Muito |

## 2. Regra de anonimização

- Não se recolheram dados que identifiquem o respondente (nome, e-mail, telefone, número de estudante).
- Cada resposta é identificada apenas pelo código R01–R36.
- A data e hora de cada resposta e as perguntas de consentimento foram retiradas dos dados.
- A localidade é registada só ao nível do concelho.
- Só entram nos dados respostas de pessoas com 18 ou mais anos que deram consentimento (36 em 36).

## 3. Registos problemáticos e tratamento

| ID | Variável | Valor original | Problema | Tratamento | Valor final |
|---|---|---|---|---|---|
| R03 | `localidade` | «Vale de cambra » | Grafia inconsistente: minúscula e espaço no fim | Corrigir para o nome oficial | Vale de Cambra |
| R06, R16 | `localidade` | «Matosinhos » | Grafia inconsistente: espaço no fim | Remover o espaço | Matosinhos |
| R11 | `localidade` | «Póvoa de Varzim » | Grafia inconsistente: espaço no fim | Remover o espaço | Póvoa de Varzim |
| R13 | `localidade` | «Santa Maria da feira » | Grafia inconsistente: minúscula e espaço no fim | Corrigir para o nome oficial | Santa Maria da Feira |
| R14, R23 | `localidade` | «Santa Maria da Feira » | Grafia inconsistente: espaço no fim | Remover o espaço | Santa Maria da Feira |
| R17, R19 | `localidade` | «Coimbra » | Grafia inconsistente: espaço no fim | Remover o espaço | Coimbra |
| R32, R34 | `localidade` | «Vila Nova de Gaia » | Grafia inconsistente: espaço no fim | Remover o espaço | Vila Nova de Gaia |
| R30 | `localidade` | «Caramulo» | Não é um concelho: é uma localidade da freguesia de Guardão, concelho de Tondela | Substituir pelo concelho | Tondela |
| R16 | `livros_12m` | «4 » | Número com espaço no fim | Remover o espaço | 4 |
| R23 | `horas_semana` | «1.5» | Ponto decimal em vez de vírgula | Converter para vírgula decimal | 1,5 |
| R01 | `imp_acessib` | (vazio) | Valor em falta: pergunta opcional não respondida | Manter vazio e excluir só dos cálculos desta variável | (vazio) |