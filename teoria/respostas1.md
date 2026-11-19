>P1: Distinga dados, informação e conhecimento. Descreva o percurso de um documento no BiblioPI ao longo dos processos de registo, codificação, armazenamento e recuperação, indicando um risco por processo.

Dados são elementos brutos e isolados, sem contexto: «2025» ou «pt», sozinhos, nada dizem. **Informação** é o resultado de processar e interpretar esses dados, dando-lhes significado útil: «tese de mestrado publicada em 2025, em português». Conhecimento é a capacidade de relacionar a informação com regras, modelos e experiência para generalizar e agir; por exemplo, saber que as teses mais requisitadas devem ter cópia digital. No modelo DIKW, cada nível depende do anterior e acrescenta interpretação.

Consideremos uma tese entregue ao BiblioPI:

1. **Registo** – o bibliotecário recolhe título, autor, data e tipo num formulário, procurando a máxima fidelidade. Risco: erros de digitação ou omissões, que comprometem todo o ciclo seguinte («garbage in, garbage out»).
2. **Codificação** – os dados passam a formatos normalizados: UTF-8, identificador DOC-0001, códigos de língua e de tipo. Risco: usar ou interpretar a codificação errada, gerando mojibake no nome do autor («João» → «JoÃ£o»).
3. **Armazenamento** – o PDF e os metadados são guardados para uso futuro. Risco: perda ou corrupção por falha de hardware, apagamento acidental ou ransomware.
4. **Recuperação** – um utilizador pesquisa no portal e obtém a tese quando precisa. Risco: resultados lentos ou irrelevantes, que tornam a informação inútil, ou exposição de intenções sensíveis nos registos de pesquisa.


>P2: Compare linguagem natural e linguagens estruturadas em cinco dimensões (regras, ambiguidade, expressividade, interpretabilidade por máquina, validação). Em que situações do BiblioPI deve ser preferida cada uma?

A linguagem natural é a forma espontânea que os seres humanos usam para comunicar; as linguagens estruturadas (XML, JSON, HTML, SQL) seguem regras sintáticas e semânticas rigorosas. Comparando-as:

- **Regras:** na natural são implícitas, variáveis e em constante evolução; nas estruturadas são explícitas, formais e estáveis.
- **Ambiguidade:** a natural é ambígua a nível lexical, sintático, semântico e pragmático, agravada por variações dialetais e culturais; nas estruturadas é minimizada ou eliminada por desenho.
- **Expressividade:** a natural é muito expressiva, transmitindo emoção e ironia; as estruturadas são expressivas apenas dentro do seu domínio formal.
- **Interpretabilidade por máquina:** a natural exige Processamento de Linguagem Natural (PLN) e mantém erros residuais; as estruturadas permitem *parsing* determinístico.
- **Validação:** na natural é difícil e subjetiva; nas estruturadas faz-se com esquemas, tipos de dados, validadores e compiladores.

No BiblioPI, a linguagem natural deve ser preferida para discutir requisitos com bibliotecários sem formação técnica, para os resumos dos documentos e para os textos de ajuda do portal. As linguagens estruturadas devem ser usadas para guardar e trocar o catálogo (catalogo.xml, catalogo.json), validá-lo automaticamente e fazer consultas exatas. As regras de empréstimo são o melhor exemplo: «até 5 livros durante 15 dias» deixa dúvidas que o regras.xml elimina com o operador `<=`, o valor 5 e a unidade explícita.


>P3: Defina os quatro tipos de ambiguidade com um exemplo original de cada. Explique a desambiguação do sentido das palavras (WSD) por contexto local e por recursos como o WordNet.

Há ambiguidade quando uma expressão admite mais do que uma interpretação legítima:

- **Lexical:** uma palavra tem vários significados, por polissemia (sentidos relacionados) ou homonímia (sem relação). «Deixei a capa na biblioteca.» – capa de um livro ou capa do traje académico.
- **Sintática:** a frase admite mais do que uma estrutura gramatical. «O resumo do artigo que foi corrigido já está no repositório.» – foi corrigido o resumo ou o artigo?
- **Semântica:** a estrutura é clara, mas a referência ou o significado global oscilam. «O orientador entregou ao aluno a tese dele.» – a tese é do aluno ou do orientador?
- **Pragmática:** a intenção do falante difere da leitura literal. «Ainda tem o livro do mês passado?», dito pela bibliotecária, pode ser uma pergunta, um lembrete de atraso ou um pedido de devolução.

A Desambiguação do Sentido da Palavra (WSD) identifica, entre os sentidos possíveis de uma palavra, o que corresponde ao contexto em que aparece. Com contexto local, o sistema analisa as palavras vizinhas: em «capa», «encadernação» e «título», capa é a cobertura do livro; em «capa», «traje» e «praxe», é vestuário. O WordNet é um recurso linguístico, como um dicionário estruturado para computadores, que organiza as palavras pelos seus significados e relações: sinónimos, palavras mais gerais e mais específicas. Para «capa», regista sentidos distintos (cobertura de livro; peça de vestuário) e o sistema escolhe aquele cujas relações combinam com o contexto: junto de «encadernação», capa é parte de um livro.


>P4: Compare mapa mental, mapa concetual e ontologia (finalidade, estrutura, rigor, público). Explique o papel do RDF, da OWL, do Dublin Core e do Schema.org.

Os três organizam conceitos, mas com finalidades e rigor diferentes:

- **Mapa mental:** finalidade criativa e de memorização; estrutura radial e livre a partir de um tema central, só com palavras-chave; rigor baixo a médio; público de estudantes e equipas. No BiblioPI, serve o brainstorm inicial (Documento, Utilizador, Empréstimo).
- **Mapa concetual:** serve para compreender relações; estrutura proposicional com ligações rotuladas por verbos («Documento — é descrito por — Metadado»); rigor médio; público do ensino e da análise.
- **Ontologia:** representação formal de um domínio para máquinas, com classes, indivíduos, propriedades e axiomas; rigor alto, baseado em lógica, que permite inferência; público da IA, da Web Semântica e da interoperabilidade. No BiblioPI, teria classes como Documento, Tese e Autor e a propriedade temAutor.

Quanto às tecnologias:

- **RDF:** modelo de triplos sujeito–predicado–objeto que descreve recursos na Web e é a base da Web Semântica (ex.: DOC-0001 — dc:creator — Autor12).
- **OWL:** linguagem para ontologias ricas sobre RDF, com perfis de expressividade e decidibilidade, restrições de cardinalidade, disjunções e propriedades inversas (ex.: Tese e Livro como classes disjuntas).
- **Dublin Core:** conjunto de metadados descritivos (title, creator, date, subject…) adotado em repositórios e bibliotecas digitais; é o namespace `dc` do catalogo.xml.
- **Schema.org:** vocabulário colaborativo para marcar páginas web com significado (Book, Person, Article), lido pelos motores de busca; é usado nas páginas de detalhe do portal.


>P5: Explique os três tipos de metadados e as três funções das marcas (estrutura, forma, semântica). Distinga marcação estruturada de marcação não estruturada.

Metadados são «dados sobre dados» que permitem descrever, identificar, gerir e recuperar documentos:

- **Descritivos:** o «cartão de visita» do recurso – título, autor, resumo, palavras-chave, datas; permitem encontrar um documento sem abrir o texto integral (no BiblioPI, `dc:title` e `dc:creator`).
- **Estruturais:** explicam a organização interna e a relação entre componentes, como os capítulos de uma tese ligados à obra ou as faixas de um recurso áudio.
- **Administrativos:** apoiam a gestão do ficheiro – direitos de autor, licença, formato, tamanho, software de criação e política de retenção (no BiblioPI, os elementos do namespace `adm`).

As marcas inseridas no texto têm três funções:

- **Estrutura:** organizar o texto em secções lógicas, como títulos e capítulos (`h1`, `h2`);
- **Forma:** controlar o aspeto visual, com formatações como negrito ou itálico;
- **Semântica:** dar significado ao conteúdo, indicando o papel de elementos como autor, data ou local (`<dc:creator>`, `<time>`).

A marcação não estruturada (Markdown, RTF) é simples e fácil de usar por pessoas, mas não garante interpretação uniforme por máquinas. A marcação estruturada (SGML, XML, HTML) tem regras formais rigorosas que permitem validação e robustez no tratamento automático. No BiblioPI, o README.md usa marcação não estruturada, pensada para leitura humana, enquanto o catalogo.xml usa marcação estruturada, validada pelo catalogo.xsd.


>P6: Explique ASCII, ISO-8859-1, Unicode e UTF-8. Porque ocorre o mojibake e como se previne em HTML, XML e JSON?

- **ASCII:** 128 caracteres em 7 bits – letras inglesas, dígitos e pontuação; não suporta acentos nem outros alfabetos.
- **ISO-8859-1 (Latin-1):** extensão a 8 bits para línguas da Europa Ocidental, com «é», «ç» e «ã», mas sem grego, cirílico ou árabe.
- **Unicode:** padrão universal com mais de 140 000 caracteres; atribui a cada um um *code point* (U+00E7 para «ç»), definindo a identidade do carácter, não os bytes.
- **UTF-8:** forma de armazenamento do Unicode com 1 a 4 bytes por carácter; os primeiros 128 coincidem com o ASCII e é o padrão da Web.

O mojibake surge quando um texto é gravado numa codificação e lido noutra; a mistura de ISO-8859-1 com UTF-8 é a causa clássica. Em UTF-8, «ç» ocupa dois bytes, C3 A7 (Yergeau, 2003); lidos como ISO-8859-1, cada byte vira um carácter e «coração» aparece como «coraÃ§Ã£o». No BiblioPI, o risco típico é importar um CSV antigo em Latin-1 como se fosse UTF-8, estragando nomes de autores.

Previne-se declarando a codificação de ponta a ponta e gravando os ficheiros nessa codificação:

- **HTML:** `<meta charset="UTF-8">` no `head` e `Content-Type: text/html; charset=utf-8` no servidor;
- **XML:** `<?xml version="1.0" encoding="UTF-8"?>` na primeira linha;
- **JSON:** o RFC 8259 exige UTF-8 no JSON trocado entre sistemas; nas APIs usa-se `Content-Type: application/json; charset=utf-8` e, se necessário, escapes como `\u00E7` (Bray, 2017).


>P7: Distinga XML bem formado de XML válido. Porque supera o XSD a DTD? Para que servem os namespaces? Indique três critérios para escolher entre XML e JSON.

Um XML bem formado cumpre as regras sintáticas da linguagem: um único elemento raiz, tags bem aninhadas e fechadas, atributos entre aspas e caracteres especiais escapados (`&lt;`, `&amp;`). Um XML válido é bem formado e, além disso, respeita um esquema (DTD ou, preferencialmente, XSD) que define os elementos permitidos, os tipos de dados, a cardinalidade e as restrições. No BiblioPI, `<dc:date>2025-13-40</dc:date>` é bem formado, mas inválido se o catalogo.xsd exigir `xs:date`.

O XSD supera a DTD porque define tipos de dados (inteiros, datas, decimais), enquanto a DTD trata tudo como texto; integra-se com namespaces; é escrito em XML, podendo ser processado pelas mesmas ferramentas; e dá mais controlo sobre ordem e cardinalidade.

Os namespaces evitam colisões de nomes quando se combinam vocabulários num documento. São identificados por URIs únicos: no catálogo, `dc:title` (Dublin Core) distingue-se dos elementos do repositório e do prefixo `adm`.

Três critérios para escolher entre XML e JSON:

1. **Verbosidade:** o JSON é mais compacto, sem tags de fecho; o XML é mais verboso.
2. **Uso dominante:** o JSON domina nas APIs REST e aplicações web e mobile; o XML nos documentos complexos, no SOAP e no intercâmbio B2B.
3. **Tipos e recursos:** o JSON tem tipos nativos (string, number, boolean, null, object, array); o XML trata tudo como texto e depende do XSD, mas oferece atributos, namespaces e conteúdo misto.


>P8: Distinga compressão com e sem perdas. Relacione entropia e comprimento médio do código de Huffman. Em que condições a RLE aumenta o tamanho dos dados?

A compressão sem perdas remove redundâncias e permite reconstruir exatamente o original; aplica-se a dados críticos, texto e programas (RLE, Huffman, Lempel-Ziv). A compressão com perdas elimina detalhes pouco percetíveis e aplica-se a multimédia (JPEG, MP3, MP4). No BiblioPI, o catalogo.xml só admite compressão sem perdas; o vídeo de uma conferência pode usar MP4.

A entropia de cada símbolo calcula-se pela sua probabilidade, Sₓ = −log₂(Pₓ), e o Huffman atribui códigos curtos aos símbolos frequentes e longos aos raros, reduzindo o número médio de bits por símbolo (Teixeira, 2026a). A entropia média, H = Σ Pₓ·Sₓ, é o limite mínimo desse número médio para qualquer código sem perdas, e o comprimento médio do Huffman cumpre H ≤ L < H + 1 (Cover & Thomas, 2006). No exercício L–P das aulas, H ≈ 2,24 e L ≈ 2,26 bits por símbolo: eficiência H/L de cerca de 99 %.

A RLE (*run-length encoding*) substitui cada sequência de símbolos iguais por um par contador + símbolo: «AAAAAA» passa a «6A». Por isso, aumenta o tamanho quando há poucas repetições seguidas: em «ABCD», cada símbolo isolado passa a ocupar dois («1A1B1C1D»), duplicando o tamanho (Salomon & Motta, 2010). É o caso da cadeia A_BIBLIOTECA_DIGITAL_DO_ISPGAYA, que não tem nenhum símbolo repetido consecutivamente.


>P9: Descreva a hierarquia de memória e explique porque o RAID não substitui o backup. Compare os modelos de base de dados relacional, documental, chave-valor e em grafo.

A hierarquia de memória organiza o armazenamento em camadas segundo o compromisso custo/capacidade/velocidade: quanto mais rápido o meio, mais caro por gigabyte e menor a capacidade. No topo estão os registos do processador e as caches; depois a RAM, volátil; abaixo os meios secundários (SSD, NVMe, HDD); e, na base, o armazenamento terciário, como fitas LTO. No BiblioPI, o índice de pesquisa ficaria em NVMe e o arquivo de longo prazo em fita.

O RAID combina discos para redundância e/ou desempenho e protege contra a falha física de um disco. Não substitui o backup porque replica de imediato qualquer alteração em todos os discos: se um bibliotecário apagar o catálogo ou um ransomware o cifrar, o RAID reproduz o erro. Só um backup, idealmente segundo a regra 3-2-1-1-0, permite recuperar uma versão anterior.

- **Relacional:** tabelas, linhas e colunas, com chaves primárias e estrangeiras e SQL; dominante em sistemas transacionais. No BiblioPI: utilizadores, empréstimos e multas.
- **Documental:** documentos JSON/BSON em coleções, com esquema flexível (MongoDB). Serve o catálogo, cujos metadados variam por tipo de documento.
- **Chave-valor:** pares chave→valor de acesso ultrarrápido (Redis). Serve sessões e cache de pesquisas.
- **Grafo:** nós e arestas com propriedades (Neo4j). Serve as relações entre documentos, autores e assuntos.


>P10: Compare os modelos de recuperação booleano, vetorial e probabilístico. Explique o índice invertido, a recuperação semântica, o RAG e os riscos de privacidade nos registos de pesquisa e nos índices.

O modelo boolean trata os documentos como conjuntos de termos e usa AND, OR e NOT; é simples e exato, mas não ordena por relevância e é sensível a reformulações. O vetorial representa documentos e consultas como vetores num espaço de termos e ordena-os pela similaridade do cosseno, permitindo correspondência parcial e ranking. O probabilístico estima a probabilidade de um documento ser relevante para a consulta, com bases como o BM25 (Teixeira, 2026b). No BiblioPI, «tese AND 2025 NOT relatório» é uma consulta booleana; o modelo vetorial ordenaria as teses pela proximidade à pesquisa.

O índice invertido evita percorrer toda a coleção (*full scan*): mapeia cada termo para a lista de documentos, e posições, em que ocorre (ex.: «huffman» → DOC-0003, DOC-0011). A recuperação semântica vai além das palavras-chave e procura a intenção e o significado, usando ontologias e pesquisa vetorial. O RAG recupera passagens relevantes e fornece-as como contexto a um LLM, reduzindo alucinações e ancorando as respostas em fontes.

Quanto à privacidade, os registos de pesquisa revelam intenções sensíveis, como pesquisas repetidas sobre uma doença. Deve minimizar-se a retenção desses registos, cifrá-los e controlar quem lhes acede. O RGPD, incluindo o princípio da minimização, aplica-se também aos índices e às cópias derivadas: apagar o documento-fonte e esquecer o índice é um erro de conformidade.


>P11: Distinga classificação supervisionada de não supervisionada, e taxonomia, folksonomia e vocabulário controlado. Explique o papel das expressões regulares na extração e validação de informação e analise, componente a componente, três dos pattern usados no trabalho. Comente o enviesamento semântico nos sistemas de classificação.

A classificação supervisionada aprende com exemplos rotulados (features → treino → validação → previsão), como Naïve Bayes; a não supervisionada (clustering, ex.: K-means) descobre grupos sem rótulos. A taxonomia é uma hierarquia fixa (Documento > Texto > Tese); a folksonomia são etiquetas livres dos utilizadores; o vocabulário controlado fixa termos para evitar sinónimos.

As expressões regulares descrevem padrões de texto e servem para extrair informação, como encontrar um ISBN num resumo (Friedl, 2006), e para validar formatos através de `pattern` no XSD e no JSON Schema (Teixeira, 2026d). No XSD o padrão aplica-se ao valor inteiro; no JSON Schema é preciso ancorá-lo com `^` e `$` (Biron & Malhotra, 2004; Wright et al., 2022). Componentes, segundo a sintaxe descrita por Friedl (2006):

- `DOC-[0-9]{4}` (id): literal «DOC-», classe `[0-9]` (um dígito) e quantificador `{4}` (exatamente quatro).
- `97[89][0-9]{10}` (ISBN-13): literal «97», classe `[89]` (prefixo 978 ou 979) e mais dez dígitos; não verifica o dígito de controlo (International ISBN Agency, 2017).
- `10\.[0-9.]+/\S+` (DOI): «10», ponto escapado `\.`, `[0-9.]+` para o código do registante, «/» e `\S+`, um ou mais caracteres sem espaço (International DOI Foundation, 2017).

O enviesamento semântico surge porque embeddings e LLM absorvem estereótipos de género, etnia ou profissão: a semântica aprendida não é neutra e pode desvalorizar autores sub-representados no BiblioPI. Mitiga-se com auditoria, dados curados e supervisão humana.


## Referências
### Fontes externas

Biron, P. V., & Malhotra, A. (Eds.). (2004). *XML Schema part 2: Datatypes second edition* (Apêndice F – Regular expressions). W3C. https://www.w3.org/TR/xmlschema-2/

Bray, T. (Ed.). (2017). *The JavaScript Object Notation (JSON) data interchange format* (RFC 8259). IETF. https://www.rfc-editor.org/rfc/rfc8259

Cover, T. M., & Thomas, J. A. (2006). *Elements of information theory* (2.ª ed.). Wiley.

Friedl, J. E. F. (2006). *Mastering regular expressions* (3.ª ed.). O'Reilly Media.

International DOI Foundation. (2017). *DOI handbook: 2 Numbering*. https://www.doi.org/doi_handbook/2_Numbering.html

International ISBN Agency. (2017). *ISBN users' manual* (7.ª ed. internacional). https://www.isbn-international.org/content/isbn-users-manual/29

Salomon, D., & Motta, G. (2010). *Handbook of data compression* (5.ª ed.). Springer.

Wright, A., Andrews, H., & Hutton, B. (Eds.). (2022). *JSON Schema Validation: A vocabulary for structural validation of JSON* (Draft 2020-12, draft-bhutton-json-schema-validation-01). IETF. https://json-schema.org/draft/2020-12/json-schema-validation

Yergeau, F. (2003). *UTF-8, a transformation format of ISO 10646* (RFC 3629). IETF. https://www.rfc-editor.org/rfc/rfc3629
