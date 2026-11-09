Respostas à Parte Teórica (Versão Reduzida)

P1: Dados, informação, conhecimento e percurso no BiblioPI
Dados são factos brutos ("15"). Informação é o dado com contexto ("15 dias de prazo"). Conhecimento é aplicar a informação para agir (avisar o aluno do prazo). O documento passa pelo registo (risco: inserir dados com grafias inválidas), codificação estruturada (risco: mojibake sem UTF-8), armazenamento físico (risco: falha de hardware sem backup) e recuperação (risco: falsos negativos por falta de metadados semânticos no portal).

P2: Linguagem natural vs. estruturadas
A linguagem natural tem regras flexíveis, é infinitamente expressiva, mas inerentemente ambígua e de processamento computacional complexo. As linguagens estruturadas (XML/JSON) têm sintaxe rígida, ambiguidade nula, expressividade limitadas ao esquema e validação automática nativa. No BiblioPI, a linguagem natural deve ser usada nos resumos e títulos, enquanto as linguagens estruturadas devem normalizar as regras de negócio, metadados e os identificadores únicos.

P3: Ambiguidades e Desambiguação (WSD)

Lexical: Múltiplo significado ("banco" de sentar vs. base de dados).

Sintática: Estrutura confusa ("leu o artigo com os óculos" - tema do artigo ou instrumento?).

Semântica: Quantificadores lógicos ("todos requisitaram um livro" - o mesmo livro ou vários?).

Pragmática: Contexto ("tem horas?").
A desambiguação (WSD) resolve isto avaliando o contexto local (palavras vizinhas) ou recorrendo ao WordNet, que mapeia o termo exato para redes semânticas lógicas (synsets).

P4: Mapas, Ontologias e Semântica
O mapa mental apoia o brainstorming (baixo rigor, público geral). O mapa concetual estrutura conhecimento em rede (rigor moderado). A ontologia usa axiomas lógicos estritos, sendo desenhada para processamento por máquinas. Na Web, o RDF estrutura os dados em triplos lógicos (Sujeito-Predicado-Objeto). A OWL adiciona restrições complexas e classes. O Dublin Core padroniza metadados globais (autor, data), e o Schema.org otimiza a indexação do HTML5 nos motores de busca.

P5: Metadados e Marcação
Os metadados descritivos identificam o recurso (título), os estruturais organizam as suas partes (capítulos) e os administrativos gerem permissões e histórico. As marcas desempenham três funções: definem a estrutura (parágrafos), controlam a forma visual (negrito) e atribuem semântica processável (datas). A marcação estruturada (XML) separa o conteúdo da apresentação. A não estruturada foca-se apenas no aspeto visual, não sendo processável automaticamente pela máquina.

P6: Codificações e Mojibake
O ASCII usa 7 bits e não tem acentos. O ISO-8859-1 usa 8 bits (suporta acentos europeus). O Unicode é a tabela universal de todos os caracteres do mundo, e o UTF-8 a sua implementação mais eficiente (1 a 4 bytes). O mojibake ocorre ao interpretar um texto em UTF-8 usando outra codificação como o ISO-8859-1. Previne-se no HTML com <meta charset="UTF-8">, no XML com a declaração de encoding e no JSON pela adoção nativa.

P7: XML, XSD e JSON
Um XML bem formado cumpre apenas a sintaxe básica (tags fechadas, raiz única). O válido respeita adicionalmente as restrições de um esquema como o XSD. O XSD supera a DTD por usar sintaxe XML e validar tipos de dados complexos. Os namespaces evitam colisões de nomes idênticos de origens diferentes (ex: dc:title vs adm:title). Escolhe-se JSON para APIs e aplicações web leves, e XML para documentos de texto com marcações mistas e validações rigorosas.

P8: Compressão, Entropia e RLE
A compressão com perdas elimina dados impercetíveis e impede o restauro exato (MP3, JPEG). Sem perdas garante o restauro total (ZIP, XML). A entropia dita o número mínimo de bits para comprimir um símbolo. O código de Huffman cria códigos variáveis cujo tamanho médio se aproxima dessa entropia, maximizando a eficiência sem perdas. O método RLE aumenta o tamanho do ficheiro se não existirem caracteres repetidos de forma consecutiva (ex: "ABC" torna-se "1A1B1C").

P9: Memória, RAID e Bases de Dados
A hierarquia de memória desce de elementos rápidos e caros (Cache, RAM) para soluções lentas, massivas e mais baratas (Discos, Fitas). O RAID espelha dados para alta disponibilidade, mas não é um backup: se o ficheiro for apagado, apaga-se em todos os discos. Base de dados relacional gere tabulações exatas (requisições). Documental gere ficheiros heterogéneos em JSON (catálogo). Chave-valor gere dados temporários rápidos (sessões). Grafo conecta dados (recomendações).

P10: Recuperação, Índice e RAG
O modelo booleano retorna correspondências exatas; o vetorial usa cálculos de geometria (cosseno) para medir relevância; o probabilístico estima estatisticamente a probabilidade do documento ser útil. O índice invertido mapeia termos aos IDs dos documentos, acelerando as pesquisas. A pesquisa semântica avalia conceitos e não letras exatas, e o RAG junta essa pesquisa a modelos de IA para produzir respostas textuais fidedignas. Estes índices podem expor perigosamente temas sensíveis dos utilizadores se não existirem controlos de privacidade.

P11: Classificação e Regex
Classificação supervisionada requer treino prévio com etiquetas humanas; a não supervisionada agrupa dados por matemática cega. Taxonomias são estritas e hierárquicas, folksonomias são orgânicas (tags de utilizadores) e vocabulários controlados são listas forçadas de termos autorizados. As Regex (expressões regulares) garantem o rigor: ^DOC-\d{4}$ obriga ao uso de 4 dígitos após "DOC-"; ^[0-9]{13}$ exige 13 algarismos (ISBN); ^[a-fA-F0-9]{64}$ exige 64 caracteres hexadecimais (SHA-256). Estas classificações apresentam enviesamentos, herdando os preconceitos ou limitações ocidentais de quem as cria.