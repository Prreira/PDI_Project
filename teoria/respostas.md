>P1: Distinga dados, informação e conhecimento. Descreva o percurso de um documento no BiblioPI ao longo dos processos de registo, codificação, armazenamento e recuperação, indicando um risco por processo.

Dados são elementos brutos e isolados sem qualquer tipo de contexto.
Informação é o resultado do processamento e interpretação dos dados, dando significado e utilidade aos mesmos.
Conhecimento é quando aplicamos a informação para tomar uma decisão().

O documento no BiblioPI, passa pelo registo onde fazemos a recolha e introdução dos dados, com o objetivo de obter os dados com a melhor fidelidade possível, com isto também corremos o risco de cometer erros de digitação, falta de valores, subjetividade e a lentidão de estar a inserir os dados. O próximo passo é a codificação, que é a fase que fazemos a transformação para o formato padronizado que permitem o processamento e a interpretação, com o objetivo de garantir que todo é compreendido tanto pelas pessoas como pelas máquinas, corremos o risco de falhas de padronização o que causa perda de dados. Depois temos o armazenamento que é quando conservamos a informação para uso futuro, com o objetivo de garantir toda a acessibilidade da informação, temos é o risco de perdas de dados devido a problemas de hardware, ou ransomware. Por último temos a recuperação que é quando acedemos e obtemos a informação armazenada, com o objetivo de disponibilizar os dados corretos quando necessários, temos o risco de dificuldade na recuperação da informação devido ao excesso de registos ou a perda de acessibilidade a longo prazo caso se tornem obsoletos.


>P2: Compare linguagem natural e linguagens estruturadas em cinco dimensões (regras, ambiguidade, expressividade, interpretabilidade por máquina, validação). Em que situações do BiblioPI deve ser preferida cada uma?

A linguagem natural é a forma que os seres humanos utilizam para comunicar, tendo regras implícitas, variáveis e em constante evolução, é bastante ambígua a todos os níveis desde lexical, semântico, sintático até pragmático, devido a variações dialeticass e culturais, também muito expressiva, conseguindo transmitir emoções e ironia, para ser interpretada por máquinas, tem de ser processada por sistemas de Processamento de Linguagem Natural(PLN), que mantêm erros residuais de interpretação, sendo a sua validação bastante complicada devido à sua subjetividade.
A linguagem estruturada segue regras rigorosas, tanto sintáticas como semânticas, a ambiguidade é muito baixa ou nula, devido ao seu desenho estrutural desde o início, também é altamente expressiva, mas apenas dentro do seu domínio formal, sendo limitada fora dele, é facilmente interpretada porque foi feita exatamente para isso,ficando assim muito fácil de validar com recurso a esquemas, tipos de dados, validadores e compiladores.

No BiblioPI, é preferível usar linguagem natural para requisitos não técnicos (respostas.md, README.md), por outro lado, a linguagem estruturada deve ser utilizada na persistência de dados, na troca de informação entre sistemas e na validação automática (regras.xml, regras.json, index.html).


>P3: Defina os quatro tipos de ambiguidade com um exemplo original de cada. Explique a desambiguação do sentido das palavras (WSD) por contexto local e por recursos como o WordNet.

Lexical: Quando uma palavra pode ter vários significados, Polissemia ou Homonímia."O funcionário guardou a nova manga" (guardou um volume de banda desenhada japonesa, uma peça de vestuário ou a fruta manga).
Sintática: Quando a estrutura gramatical de uma frase permite múltiplas interpretações."O leitor viu o autor com óculos" (o leitor usou os óculos para ver o autor ou o leitor viu o autor que usava óculos).
Semântica: Quando o significado global ou a referência mudam, frequentemente devido a quantificadores ou pronomes."Todos os sócios da biblioteca requisitaram um livro do Stephen King" (um único livro foi requisitado por todos os sócios ou cada sócio requisitou um livro diferente).
Pragmática: Quando a interpretação correta depende do contexto prático."Já olhaste para a secção de devoluções de jogos retro?" (pergunta literal para saber se a pessoa já observou aquela secção, ou um pedido indireto/crítica a sugerir que a secção está desarrumada).

A Desambiguação do Sentido da Palavra (WSD), é o processo de identificar, entre os vários significados possíveis de uma palavra, aquele a que ela corresponde, tendo em conta o contexto em que a palavra aparece.
Utilizando o Contexto Local, temos de olhar para as palavras próximas àquela que queremos identificar o significado. Utilizando o WordNet, recorremos a um recurso linguístico que organiza palavras de acordo com os seus significados e relações semânticas, como se fosse um dicionário estruturado para computadores.


>P4: Compare mapa mental, mapa concetual e ontologia (finalidade, estrutura, rigor, público). Explique o papel do RDF, da OWL, do Dublin Core e do Schema.org.

Mapa Mental: Tem como finalidade a criatividade e a memorização, apresentando uma estrutura radial e livre, como o seu público são os estudantes e as equipas de trabalho, o seu nível de rigor é baixo-médio.
Mapa Conceptual: Tem como finalidade compreender as relações lógicas, tendo uma estrutura proposicional com ligações explícitas e rotuladas, como se direciona para o ensino e a análise, apresenta um rigor médio.
Ontologia: Destina-se à representação formal do conhecimento para máquinas interpertarem, estrutura-se em classes, propriedades e axiomas, como o seu público abrange a Inteligência Artificial, a Web Semântica e a interoperabilidade, o seu nível de rigor é alto, baseado em lógica.

RDF: É o modelo base da Web Semântica, que descreve recursos web através de triplos sujeito-predicado-objeto.
OWL: É uma linguagem para ontologias ricas sobre RDF, onde temos diferentes perfis de expressividade e decidibilidade, que permitem restrições avançadas de cardinalidade e propriedades complexas.
Dublin Core: É um conjunto de metadados descritivos, que são amplamente adotados para padronizar a descrição de documentos em bibliotecas digitais e repositórios, como o BiblioPI (incluindo elementos como title, creator, date, subject, etc).
Schema.org: É um vocabulário colaborativo utilizado para inserir marcações semânticas em páginas web, fazendo com que os motores de pesquisa interpretem o conteúdo com maior precisão e gerem melhores resultados (Product, Person, Event, Article).



>P5: Explique os três tipos de metadados e as três funções das marcas (estrutura, forma, semântica). Distinga marcação estruturada de marcação não estruturada.

Metadados descritivos: São como o "cartão de visita" do recurso, que permitem identificar a partir de elementos como título, autor, resumo, palavras-chave e datas, em catálogos bibliográficos permitindo encontrar documentos sem aceder ao texto integral.
Metadados estruturais: Explicam a organização interna e a relação entre os componentes.
Metadados administrativos: É a gestão do ficheiro, onde temos direitos de autor, licenças, formato, tamanho, etc.

Estrutura: Texto organizado em secções lógicas, tais como títulos e capítulos.
Forma: Controla o aspeto visual da exibição do texto, com a aplicação de formatações como negrito ou itálico.
Semântica: Dar significado aos dados, especificando o contexto e o papel de elementos como o autor, a data e o local.

Marcação não estruturada: É simples e fácil para o humano utilizar, falhando na parte de garantir a interpretação uniforme por máquinas, usando formatos como Markdown ou o RTF.
Marcação estruturada: Tem regras formais rigorosas que permitem a validação e robustez no tratamento automático, incluindo linguagens como SGML, XML ou HTML.



>P6: Explique ASCII, ISO-8859-1, Unicode e UTF-8. Porque ocorre o mojibake e como se previne em HTML, XML e JSON?

ASCII: É um padrão de 7 bits que representa 128 caracteres, entre letras inglesas maiúsculas e minúsculas, dígitos e pontuação, não suportando acentos, nem outros alfabetos.
ISO-8859-1: É a extensão a 8 bits para línguas europeias ocidentais, adicionando acentos e "ç".
Unicode: É um padrão universal que cobre praticamente todas as línguas, símbolos matemáticos, musicais e emojis, com mais de 140 000 caracteres.
UTF-8: É uma forma de armazenamento de Unicode com um comprimento variável (1 a 4 bytes por carácter), sendo compatível com ASCII, é o padrão usado atualmente na Web e em grande parte dos sistemas modernos.

Mojibake acontece quando existem caracteres corrompidos e ilegíveis num ficheiro que inicialmente é guardado numa codificação com esses caracteres e depois é interpretado ou lido noutra codificação (guardado como UTF-8 e lido em ISO-8859-1).

Para prevenir o mojibake, temos de garantir que cada formato declara o encoding que está a usar. Para HTML, definimos a metatag (<meta charset="UTF-8">) no cabeçalho, para XML, temos de especificar na declaração inicial (<?xml version="1.0" encoding="UTF-8"?>), e em JSON, o formato assume nativamente o UTF-8, tendo de garantir que os ficheiros associados estão configurados com o mesmo encoding.


>P7: Distinga XML bem formado de XML válido. Porque supera o XSD a DTD? Para que servem os namespaces? Indique três critérios para escolher entre XML e JSON.

Um XML bem formado segue as regras sintáticas fundamentais da linguagem, que são apenas um único elemento raiz, as tags estão bem aninhadas e fechadas, os atributos estão entre aspas e os caracteres especiais estão corretamente representados, enquanto um XML válido, atende a todos os requisitos anteriores e garante a conformidade com um esquema formal (DTD ou, preferencialmente, XSD), que estipula os elementos permitidos, os tipos de dados, a cardinalidade e as restrições estruturais.

O XSD é superior ao DTD pois possibilita a definição de tipos de dados específicos, como inteiros, datas e decimais, incorpora namespaces e é escrito na própria sintaxe XML.

Os namespaces servem para prevenir colisões e conflitos de nomes ao combinar diversos vocabulários em um único documento. 

Para escolhermos entre XML e JSON, temos de ter atenção à verbosidade, que no JSON apresenta uma verbosidade bem menor por não precisar de tags de fecho, enquanto o XML é notavelmente mais verboso,o uso dominante, que no JSON é o formato mais comum em APIs REST, aplicativos web mobile e interações com JavaScript, enquanto o XML é mais adequado para documentos elaborados, SOAP e intercambialidade em ecossistemas corporativos legados ou B2B, e por fim temos os tipos de dados nativos, que para o JSON possui suporte nativo para tipos de dados (como string, number, boolean, null, object e array), enquanto o XML trata tudo como texto de forma nativa, dependendo do XSD para definir outros tipos.


>P8: Distinga compressão com e sem perdas. Relacione entropia e comprimento médio do código de Huffman. Em que condições a RLE aumenta o tamanho dos dados?

A compressão com perdas baseia-se na eliminação dos detalhes e é utilizada para comprimir ficheiros multimédia, suporta formatos como JPEG, MP3 e MP4, agora na compressão sem perdas baseia-se na remoção das redundâncias da informação e é usada para comprimir dados críticos, texto e programas, utilizando algoritmos como Run-length, Huffman ou Lempel-Ziv.

A entropia é diretamente calculada com base numa probabilidade matemática através da fórmula $S_x = -log_2(P_x)$, que representa o limite teórico mínimo de bits necessários para representar um símbolo, a sua relação com o código de Huffman é direta, devido ao algoritmo basear-se nessas mesmas probabilidades para tentar reduzir o comprimento médio do código, atribuindo códigos binários mais curtos aos símbolos mais frequentes, e códigos mais longos aos símbolos menos frequentes.

Em que condições a RLE aumenta o tamanho dos dados?
-------Não há informação nos slides!!--------


>P9: Descreva a hierarquia de memória e explique porque o RAID não substitui o backup. Compare os modelos de base de dados relacional, documental, chave-valor e em grafo.

A hierarquia de memória é organizada em camadas e baseia-se no compromisso custo/capacidade/velocidade, em que os meios mais rápidos tornam-se mais caros por gigabyte e oferecem menor capacidade. No topo da hierarquia encontram-se os registos de processadores e caches, depois surge a memória RAM, abaixo temos os dispositivos secundários (SSD, NVMe, HDD), e na base temos os arquivos terciários.

RAID é a combinação de discos para criar redundância e/ou melhorar o desempenho, conseguindo proteger contra a falha física de um disco, o que não substitui o backup, devido a não conseguir proteger contra o apagamento acidental ou ransomware.

Relacional: Organiza os dados em tabelas (relações), linhas (tuplos), colunas (atributos) e chaves (primárias/estrangeiras), utilizando a linguagem SQL, sendo o modelo dominante em sistemas transacionais exigentes (Bancos, ERP, Hospitalares).
Documental: Armazena a informação em documentos (JSON/BSON), sendo organizados em coleções (MongoDB, CouchDB), adequando-se à variedade de conteúdos e de APIs orientadas a documentos.
Chave-valor: Armazena a informação em pares chave-valor, dando acesso ultrarrápido (Redis, DynamoDB), sendo a escolha ideal para sistemas de caches, gestão de sessões e contadores.
Em grafo: Baseia-se em nós e arestas com propriedades (Neo4j, Amazon Neptune), destacando-se na gestão de relações complexas, onde se torna ideal para ser usada em redes sociais, deteção de fraudes e knowledge graphs.


>P10: Compare os modelos de recuperação booleano, vetorial e probabilístico. Explique o índice invertido, a recuperação semântica, o RAG e os riscos de privacidade nos registos de pesquisa e nos índices.

O modelo de recuperação booleana usa operadores lógicos (AND, OR, NOT) para fazer pesquisas específicas, porém tem algumas restrições, por não conseguir ordenar os resultados por relevância, já o modelo vetorial apresenta documentos e consultas como vetores num espaço de termos, recorrendo à similaridade do cosseno para permitir correspondência parcial e ordenação (ranking), e o modelo probabilístico calcula a probabilidade de um documento ser relevante para a consulta, utilizando bases teóricas como o BM25.

Para prevenir que se verifique todo o conjunto, full scan, usa-se o índice invertido que mapeia cada termo para a lista de documentos em que ocorre, sendo desta forma a estrutura central dos motores de pesquisa. A recuperação semântica vai além pois capta o significado e a intenção das palavras-chave. O RAG, Retrieval-Augmented Generation, usa a combinação da recuperação de informação com grandes modelos de linguagem, recuperando passagens relevantes e dando contexto ao LLM, evitando assim alucinações e ancorando as respostas fonte.

De forma a combater a falta de privacidade, os registos de pesquisa (logs), revelam intenções sensíveis dos utilizadores. As normas indicadas pelo RGPD e as regras de minimização aplicam-se da mesma forma aos índices e às cópias derivadas, dando origem a um erro grave de compliance ao apagar o documento-fonte e esquecer de remover os dados do índice.


>P11: Distinga classificação supervisionada de não supervisionada, e taxonomia, folksonomia e vocabulário controlado. Explique o papel das expressões regulares na extração e validação de informação e analise, componente a componente, três dos pattern usados no trabalho. Comente o enviesamento semântico nos sistemas de classificação.

A diferença entre a classificação supervisionada e não supervisionada é que a classificação supervisionada trabalha com um conjunto de dados já rotulados pois ela é uma Machine Learning que é um algoritmo que mapeia as características dos dados de cada um dos rótulos, o pipeline por si só abrange features, validação, previsão e treino em novos dados. 
Já a classificação não supervisionada ( clustering ) , é uma outra variável de Machine Learning que tem como função encontrar estruturas ocultas nos dados criando grupos ou clusters com os itens semelhantes.	Em um contexto digital as taxonomias são estruturas hierárquicas fixas que organizam e classificam a informação, já as folksonomias são categorias criadas por utilizadores de um sistema de forma livre. o vocabulário controlado define e restringe termos de forma a tentar evitar possíveis redundâncias e sinônimos.

----------FALTA AS EXPRESSOES REGULARES----------

No enviesamento semântico nos sistemas de classificação acontece quando não e neutra a semântica aprendida. Em alguns modelos como LLM e embeddings recolhem estereótipos ( religião, etário), ou seja para tratar de alguma situação são necessárias mitigações que inclua a inspeção de dados, constraints, dados de treino curados.
