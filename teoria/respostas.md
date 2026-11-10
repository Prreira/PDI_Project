<<<<<<< HEAD
P1: Distinga dados, informação e conhecimento. Descreva o percurso de um documento no BiblioPI ao longo dos processos de registo, codificação, armazenamento e recuperação, indicando um risco por processo.

Dados são elementos brutos e isolados sem qualquer tipo de contexto.
Informação é o resultado do processamento e interpretação dos dados, dando significado e utilidade aos mesmos.
Conhecimento é quando aplicamos a informação para tomar uma decisão.

O documento no BiblioPI, passa pelo registo onde fazemos a recolha e introdução dos dados, com o objetivo de obter os dados com a melhor fidelidade possível, com isto também corremos o risco de cometer erros de digitação, falta de valores, subjetividade e a lentidão de estar a inserir os dados. O próximo passo é a codificação, que é a fase que fazemos a transformação para o formato padronizado que permitem o processamento e a interpretação, com o objetivo de garantir que todo é compreendido tanto pelas pessoas como pelas máquinas, corremos o risco de falhas de padronização o que causa perda de dados. Depois temos o armazenamento que é quando conservamos a informação para uso futuro, com o objetivo de garantir toda a acessibilidade da informação, temos é o risco de perdas de dados devido a problemas de hardware, ou ransomware. Por último temos a recuperação que é quando acedemos e obtemos a informação armazenada, com o objetivo de disponibilizar os dados corretos quando necessários, temos o risco de dificuldade na recuperação da informação devido ao excesso de registos ou a perda de acessibilidade a longo prazo caso se tornem obsoletos.



P2: Compare linguagem natural e linguagens estruturadas em cinco dimensões (regras, ambiguidade, expressividade, interpretabilidade por máquina, validação). Em que situações do BiblioPI deve ser preferida cada uma?

A linguagem natural é a forma que os seres humanos utilizam para comunicar, tendo regras implícitas, variáveis e em constante evolução, é bastante ambígua a todos os níveis desde lexical, semântico, sintático até pragmático, devido a variações dialeticass e culturais, também muito expressiva, conseguindo transmitir emoções e ironia, para ser interpretada por máquinas, tem de ser processada por sistemas de Processamento de Linguagem Natural(PLN), que mantêm erros residuais de interpretação, sendo a sua validação bastante complicada devido à sua subjetividade.
A linguagem estruturada segue regras rigorosas, tanto sintáticas como semânticas, a ambiguidade é muito baixa ou nula, devido ao seu desenho estrutural desde o início, também é altamente expressiva, mas apenas dentro do seu domínio formal, sendo limitada fora dele, é facilmente interpretada porque foi feita exatamente para isso,ficando assim muito fácil de validar com recurso a esquemas, tipos de dados, validadores e compiladores.

No BiblioPI, é preferível usar linguagem natural para requisitos não técnicos (respostas.md, README.md), por outro lado, a linguagem estruturada deve ser utilizada na persistência de dados, na troca de informação entre sistemas e na validação automática (regras.xml, regras.json, index.html).



P3: Defina os quatro tipos de ambiguidade com um exemplo original de cada. Explique a desambiguação do sentido das palavras (WSD) por contexto local e por recursos como o WordNet.

Lexical - 
Sintática - 
Semântica - 
Pragmática - 



P4:Compare mapa mental, mapa concetual e ontologia (finalidade, estrutura, rigor, público). Explique o papel do RDF, da OWL, do Dublin Core e do Schema.org.

O mapa mental apoia o brainstorming (baixo rigor, público geral). O mapa concetual estrutura conhecimento em rede (rigor moderado). A ontologia usa axiomas lógicos estritos, sendo desenhada para processamento por máquinas. Na Web, o RDF estrutura os dados em triplos lógicos (Sujeito-Predicado-Objeto). A OWL adiciona restrições complexas e classes. O Dublin Core padroniza metadados globais (autor, data), e o Schema.org otimiza a indexação do HTML5 nos motores de busca.



P5:Explique os três tipos de metadados e as três funções das marcas (estrutura, forma, semântica). Distinga marcação estruturada de marcação não estruturada.

Os metadados descritivos identificam o recurso (título), os estruturais organizam as suas partes (capítulos) e os administrativos gerem permissões e histórico. As marcas desempenham três funções: definem a estrutura (parágrafos), controlam a forma visual (negrito) e atribuem semântica processável (datas). A marcação estruturada (XML) separa o conteúdo da apresentação. A não estruturada foca-se apenas no aspeto visual, não sendo processável automaticamente pela máquina.



P6:Explique ASCII, ISO-8859-1, Unicode e UTF-8. Porque ocorre o mojibake e como se previne em HTML, XML e JSON?

O ASCII usa 7 bits e não tem acentos. O ISO-8859-1 usa 8 bits (suporta acentos europeus). O Unicode é a tabela universal de todos os caracteres do mundo, e o UTF-8 a sua implementação mais eficiente (1 a 4 bytes). O mojibake ocorre ao interpretar um texto em UTF-8 usando outra codificação como o ISO-8859-1. Previne-se no HTML com <meta charset="UTF-8">, no XML com a declaração de encoding e no JSON pela adoção nativa.



P7:Distinga XML bem formado de XML válido. Porque supera o XSD a DTD? Para que servem os namespaces? Indique três critérios para escolher entre XML e JSON.

Um XML bem formado cumpre apenas a sintaxe básica (tags fechadas, raiz única). O válido respeita adicionalmente as restrições de um esquema como o XSD. O XSD supera a DTD por usar sintaxe XML e validar tipos de dados complexos. Os namespaces evitam colisões de nomes idênticos de origens diferentes (ex: dc:title vs adm:title). Escolhe-se JSON para APIs e aplicações web leves, e XML para documentos de texto com marcações mistas e validações rigorosas.



P8:Distinga compressão com e sem perdas. Relacione entropia e comprimento médio do código de Huffman. Em que condições a RLE aumenta o tamanho dos dados?

A compressão com perdas elimina dados impercetíveis e impede o restauro exato (MP3, JPEG). Sem perdas garante o restauro total (ZIP, XML). A entropia dita o número mínimo de bits para comprimir um símbolo. O código de Huffman cria códigos variáveis cujo tamanho médio se aproxima dessa entropia, maximizando a eficiência sem perdas. O método RLE aumenta o tamanho do ficheiro se não existirem caracteres repetidos de forma consecutiva (ex: "ABC" torna-se "1A1B1C").



P9:Descreva a hierarquia de memória e explique porque o RAID não substitui o backup. Compare os modelos de base de dados relacional, documental, chave-valor e em grafo.

A hierarquia de memória desce de elementos rápidos e caros (Cache, RAM) para soluções lentas, massivas e mais baratas (Discos, Fitas). O RAID espelha dados para alta disponibilidade, mas não é um backup: se o ficheiro for apagado, apaga-se em todos os discos. Base de dados relacional gere tabulações exatas (requisições). Documental gere ficheiros heterogéneos em JSON (catálogo). Chave-valor gere dados temporários rápidos (sessões). Grafo conecta dados (recomendações).



P10:Compare os modelos de recuperação booleano, vetorial e probabilístico. Explique o índice invertido, a recuperação semântica, o RAG e os riscos de privacidade nos registos de pesquisa e nos índices.

O modelo booleano retorna correspondências exatas; o vetorial usa cálculos de geometria (cosseno) para medir relevância; o probabilístico estima estatisticamente a probabilidade do documento ser útil. O índice invertido mapeia termos aos IDs dos documentos, acelerando as pesquisas. A pesquisa semântica avalia conceitos e não letras exatas, e o RAG junta essa pesquisa a modelos de IA para produzir respostas textuais fidedignas. Estes índices podem expor perigosamente temas sensíveis dos utilizadores se não existirem controlos de privacidade.



P11:Distinga classificação supervisionada de não supervisionada, e taxonomia, folksonomia e vocabulário controlado. Explique o papel das expressões regulares na extração e validação de informação e analise, componente a componente, três dos pattern usados no trabalho. Comente o enviesamento semântico nos sistemas de classificação.

=======
P1: Distinga dados, informação e conhecimento. Descreva o percurso de um documento no BiblioPI ao
longo dos processos de registo, codificação, armazenamento e recuperação, indicando um risco
por processo.

Dados são elementos brutos e isolados sem qualquer tipo de contexto.
Informação é o resultado do processamento e interpretação dos dados, dando significado e utilidade aos mesmos.
Conhecimento é quando aplicamos a informação para tomar uma decisão.

O documento no BiblioPI, passa pelo registo onde fazemos a recolha e introdução dos dados, com o objetivo de obter os dados com a melhor fidelidade possível, com isto também corremos o risco de cometer erros de digitação, falta de valores, subjetividade e a lentidão de estar a inserir os dados. O próximo passo é a codificação, que é a fase que fazemos a transformação para o formato padronizado que permitem o processamento e a interpretação, com o objetivo de garantir que todo é compreendido tanto pelas pessoas como pelas máquinas, corremos o risco de falhas de padronização o que causa perda de dados. Depois temos o armazenamento que é quando conservamos a informação para uso futuro, com o objetivo de garantir toda a acessibilidade da informação, temos é o risco de perdas de dados devido a problemas de hardware, ou ransomware. Por último temos a recuperação que é quando acedemos e obtemos a informação armazenada, com o objetivo de disponibilizar os dados corretos quando necessários, temos o risco de dificuldade na recuperação da informação devido ao excesso de registos ou a perda de acessibilidade a longo prazo caso se tornem obsoletos.



P2:Compare linguagem natural e linguagens estruturadas em cinco dimensões (regras, ambiguidade,
expressividade, interpretabilidade por máquina, validação). Em que situações do BiblioPI deve ser
preferida cada uma?

A linguagem natural tem regras flexíveis, é infinitamente expressiva, mas inerentemente ambígua e de processamento computacional complexo. As linguagens estruturadas (XML/JSON) têm sintaxe rígida, ambiguidade nula, expressividade limitadas ao esquema e validação automática nativa. No BiblioPI, a linguagem natural deve ser usada nos resumos e títulos, enquanto as linguagens estruturadas devem normalizar as regras de negócio, metadados e os identificadores únicos.



P3:Defina os quatro tipos de ambiguidade com um exemplo original de cada. Explique a
desambiguação do sentido das palavras (WSD) por contexto local e por recursos como o WordNet.

Lexical: Múltiplo significado ("banco" de sentar vs. base de dados).

Sintática: Estrutura confusa ("leu o artigo com os óculos" - tema do artigo ou instrumento?).

Semântica: Quantificadores lógicos ("todos requisitaram um livro" - o mesmo livro ou vários?).

Pragmática: Contexto ("tem horas?").
A desambiguação (WSD) resolve isto avaliando o contexto local (palavras vizinhas) ou recorrendo ao WordNet, que mapeia o termo exato para redes semânticas lógicas (synsets).



P4:Compare mapa mental, mapa concetual e ontologia (finalidade, estrutura, rigor, público). Explique
o papel do RDF, da OWL, do Dublin Core e do Schema.org.

O mapa mental apoia o brainstorming (baixo rigor, público geral). O mapa concetual estrutura conhecimento em rede (rigor moderado). A ontologia usa axiomas lógicos estritos, sendo desenhada para processamento por máquinas. Na Web, o RDF estrutura os dados em triplos lógicos (Sujeito-Predicado-Objeto). A OWL adiciona restrições complexas e classes. O Dublin Core padroniza metadados globais (autor, data), e o Schema.org otimiza a indexação do HTML5 nos motores de busca.



P5:Explique os três tipos de metadados e as três funções das marcas (estrutura, forma, semântica).
Distinga marcação estruturada de marcação não estruturada.

Os metadados descritivos identificam o recurso (título), os estruturais organizam as suas partes (capítulos) e os administrativos gerem permissões e histórico. As marcas desempenham três funções: definem a estrutura (parágrafos), controlam a forma visual (negrito) e atribuem semântica processável (datas). A marcação estruturada (XML) separa o conteúdo da apresentação. A não estruturada foca-se apenas no aspeto visual, não sendo processável automaticamente pela máquina.



P6:Explique ASCII, ISO-8859-1, Unicode e UTF-8. Porque ocorre o mojibake e como se previne em
HTML, XML e JSON?

O ASCII usa 7 bits e não tem acentos. O ISO-8859-1 usa 8 bits (suporta acentos europeus). O Unicode é a tabela universal de todos os caracteres do mundo, e o UTF-8 a sua implementação mais eficiente (1 a 4 bytes). O mojibake ocorre ao interpretar um texto em UTF-8 usando outra codificação como o ISO-8859-1. Previne-se no HTML com <meta charset="UTF-8">, no XML com a declaração de encoding e no JSON pela adoção nativa.



P7:Distinga XML bem formado de XML válido. Porque supera o XSD a DTD? Para que servem os
namespaces? Indique três critérios para escolher entre XML e JSON.

Um XML bem formado cumpre apenas a sintaxe básica (tags fechadas, raiz única). O válido respeita adicionalmente as restrições de um esquema como o XSD. O XSD supera a DTD por usar sintaxe XML e validar tipos de dados complexos. Os namespaces evitam colisões de nomes idênticos de origens diferentes (ex: dc:title vs adm:title). Escolhe-se JSON para APIs e aplicações web leves, e XML para documentos de texto com marcações mistas e validações rigorosas.



P8:Distinga compressão com e sem perdas. Relacione entropia e comprimento médio do código de
Huffman. Em que condições a RLE aumenta o tamanho dos dados?

A compressão com perdas elimina dados impercetíveis e impede o restauro exato (MP3, JPEG). Sem perdas garante o restauro total (ZIP, XML). A entropia dita o número mínimo de bits para comprimir um símbolo. O código de Huffman cria códigos variáveis cujo tamanho médio se aproxima dessa entropia, maximizando a eficiência sem perdas. O método RLE aumenta o tamanho do ficheiro se não existirem caracteres repetidos de forma consecutiva (ex: "ABC" torna-se "1A1B1C").



P9:Descreva a hierarquia de memória e explique porque o RAID não substitui o backup. Compare os
modelos de base de dados relacional, documental, chave-valor e em grafo.

A hierarquia de memória desce de elementos rápidos e caros (Cache, RAM) para soluções lentas, massivas e mais baratas (Discos, Fitas). O RAID espelha dados para alta disponibilidade, mas não é um backup: se o ficheiro for apagado, apaga-se em todos os discos. Base de dados relacional gere tabulações exatas (requisições). Documental gere ficheiros heterogéneos em JSON (catálogo). Chave-valor gere dados temporários rápidos (sessões). Grafo conecta dados (recomendações).



P10:Compare os modelos de recuperação booleano, vetorial e probabilístico. Explique o índice
invertido, a recuperação semântica, o RAG e os riscos de privacidade nos registos de pesquisa e
nos índices.

O modelo booleano retorna correspondências exatas; o vetorial usa cálculos de geometria (cosseno) para medir relevância; o probabilístico estima estatisticamente a probabilidade do documento ser útil. O índice invertido mapeia termos aos IDs dos documentos, acelerando as pesquisas. A pesquisa semântica avalia conceitos e não letras exatas, e o RAG junta essa pesquisa a modelos de IA para produzir respostas textuais fidedignas. Estes índices podem expor perigosamente temas sensíveis dos utilizadores se não existirem controlos de privacidade.



P11:Distinga classificação supervisionada de não supervisionada, e taxonomia, folksonomia e
vocabulário controlado. Explique o papel das expressões regulares na extração e validação de
informação e analise, componente a componente, três dos pattern usados no trabalho. Comente
o enviesamento semântico nos sistemas de classificação.

>>>>>>> 051558644381eb577ba5b917163d2fb196c61486
Classificação supervisionada requer treino prévio com etiquetas humanas; a não supervisionada agrupa dados por matemática cega. Taxonomias são estritas e hierárquicas, folksonomias são orgânicas (tags de utilizadores) e vocabulários controlados são listas forçadas de termos autorizados. As Regex (expressões regulares) garantem o rigor: ^DOC-\d{4}$ obriga ao uso de 4 dígitos após "DOC-"; ^[0-9]{13}$ exige 13 algarismos (ISBN); ^[a-fA-F0-9]{64}$ exige 64 caracteres hexadecimais (SHA-256). Estas classificações apresentam enviesamentos, herdando os preconceitos ou limitações ocidentais de quem as cria.