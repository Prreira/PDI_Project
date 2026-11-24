Frases do Anexo:
1. «O bibliotecário viu o aluno com o portátil.»
Tipo de Ambiguidade: Sintática;
Interpretações Possíveis: Podemos interpretar que o bibliotecário viu o aluno através do portátil ou que o aluno estava a usar um portátil e o bibliotecário o viu a usa-lo:;
Origem da Ambiguidade: A ambiguidade origina-se quando  a expressão "com o portátil" não deixa claro se o portátil está a ser utilizado pelo bibliotecário ou pelo aluno;
Reformulação: "O bibliotecário usou o portátil para ver o aluno" ou "O bibliotecário viu o aluno com o seu portátil";

2. «Todos os utilizadores requisitaram um livro.»
Tipo de Ambiguidade: Semântica;
Interpretações Possíveis: Podemos interpretar que todos os utilizadores requisitaram exatamente o mesmo livro ou que todos os utilizadores queriam apenas um livro mas de forma quantitativa ou seja só uma unidade de livro;
Origem da Ambiguidade: A ambiguidade origina-se quando a expressão "um livro" não deixa claro se os utilizadores querem todos o mesmo livro ou se a expressão de refere a um numero quantitativo de livros;
Reformulação: "Todos os utilizadores requisitaram pelo menos um livro" ou "Todos os utilizadores requisitaram o mesmo livro";

3. «A obra está em reparação.»
Tipo de Ambiguidade: Lexical;
Interpretações Possíveis: Podemos interpretar que uma construção ou edifício  está a ser reparada ou que alguma obra literária/artística está a ser restaurada ou reparada;
Origem da Ambiguidade: A ambiguidade origina-se quando "obra" é uma Polissemia pois não deixa claro se e uma obra ligada ao mundo da construção ou se é uma obra artística ou literária; 
Reformulação: "A construção está em reparação" ou "O livro está a ser restaurado";

4. «O Pedro disse ao Rui que ele tinha uma multa.»
Tipo de Ambiguidade: Semântica;
Interpretações Possíveis: Podemos interpretar que o Pedro recebeu uma multa e disse ao Rui ou que O Pedro disse ao Rui que o Rui tinha recebido uma multa;
Origem da Ambiguidade: A ambiguidade origina-se quando a expressão "ele" não deixa claro se foi o Rui ou o Pedro que recebeu a multa";
Reformulação: "O Pedro recebeu uma multa e disse ao Rui" ou "O Pedro disse ao Rui que sabia que o Rui tinha uma multa";

5. «Que maravilha, o catálogo está outra vez em baixo!»
Tipo de Ambiguidade: Pragmática;
Interpretações Possíveis: Podemos interpretar que a pessoa usou ironia para mostrar o seu descontentamento com o facto de o catálogo não estar a funcionar ou a pessoa está verdadeiramente contente por o catalogo não estar a funcionar;
Origem da Ambiguidade: A ambiguidade origina-se quando a expressão "Que maravilha" não deixa claro se a pessoa está contente ou descontente com o funcionamento do catalogo;
Reformulação: " Estou decepcionado por o catálogo estar novamente em baixo" ou " Ainda bem que o catálogo está novamente em baixo";

6. «Procuro relatórios e teses de 2025.»
Tipo de Ambiguidade: Sintática;
Interpretações Possíveis: Que a pessoa procura relatórios e teses exclusivamente de 2025 ou que está a procura de teses de 2025 e relatórios de qualquer ano inclusive 2025;
Origem da Ambiguidade: A ambiguidade origina-se quando a expressão "de 2025" não deixa claro se quer que as teses e os relatórios sejam desse ano ou se somente procura teses de 2025;
Reformulação: "Procuro relatórios de 2025 e teses de 2025" ou " Procuro relatório de qualquer ano e teses de 2025;

7. «Encontrei o título no catálogo.»
Tipo de Ambiguidade: Lexical;
Interpretações Possíveis: Que a pessoa encontrou o titulo de algum livro no catálogo ou que a pessoa usou o catálogo para encontrar exatamente o titulo que procurava;
Origem da Ambiguidade: 
Reformulação:

8. «Pode deixar a mochila à entrada?»
Tipo de Ambiguidade: Pragmática;
Interpretações Possíveis: A pessoa esta a pedir a alguém se pode deixar a sua mochila na entrada ou a pessoa esta a perguntar se existe alguma autorização que a deixe pousar a mochila na entrada;
Origem da Ambiguidade: a ambiguidade origina-se quando a frase é na verdade uma pergunta e então não fica claro se é um pedido a alguém ou se a pessoa esta a questionar algum tipo de regra ou protocolo; 
Reformulação: "É permitido deixar a mochila na entrada?" ou "Podes deixar a mochila na entrada";
-------------------------------------------------------------------------------------------------------------------------------------------------------
Frases Originais:
1.
Tipo de Ambiguidade:
Interpretações Possíveis:
Origem da Ambiguidade:
Reformulação:

2.
Tipo de Ambiguidade:
Interpretações Possíveis:
Origem da Ambiguidade:
Reformulação:

3.
Tipo de Ambiguidade:
Interpretações Possíveis:
Origem da Ambiguidade:
Reformulação:

4.
Tipo de Ambiguidade:
Interpretações Possíveis:
Origem da Ambiguidade:
Reformulação:
-------------------------------------------------------------------------------------------------------------------------------------------------------
Regras de Empréstimo:
1. R1 — «Os estudantes podem requisitar até 5 livros durante 15 dias.»
Ambiguidades encontradas: "até 5 livros" esta expressão não esclarece se o estudante só pode requisitar 5 livros em simultâneo ou se durante o período dos 15 dias o aluno pode requisitar no máximo 5 livros. "durante 15 dias" não esclarece quando começa a contagem desses 15 dias e nem se são 15 dias uteis ou 15 dias consecutivos;
Como resolver: para eliminar as duvidas é preciso deixar claro que cada estudante só pode ter 5 livros requisitados em simultâneo e que o período de 15 dias começa a contar a partir do momento do empréstimo e que são 15 dias consecutivos;
Pseudocódigo:

programa {
    funcao Emprestimo() {
        cadeia perfil = "estudante"
        cadeia tipoObra = "normal"
        inteiro emprestimosAtivos = 3

        escreva(podeRequisitar(perfil, tipoObra, emprestimosAtivos))
    }

    funcao cadeia podeRequisitar(cadeia perfil, cadeia tipoObra, inteiro emprestimosAtivos) {
        se (perfil == "estudante" e tipoObra == "normal") {
            se (emprestimosAtivos < 5) {
                inteiro prazoDias = 15
                retorne "Empréstimo autorizado por " + prazoDias + " dias"
            } senao {
                retorne "Limite de 5 livros atingido"
            }
        } senao {
            retorne "Regra R1 não aplicável"
        }
    }
}

2. R2 — «Os docentes têm prazos maiores e não pagam multas, exceto nas obras de reserva.»
Ambiguidades encontradas: "prazos maiores" esta expressão não deixa claro quantos dias a mais os docentes podem ficar com os livros. "exceto nas obras de reserva" não deixa claro se os docentes recebem multa somente neste tipo de obra ou se também deixa de puder ter estas obras por mais tempo que os estudantes;
Como resolver: Definir prazos específicos para os docentes, deixar claro que os docentes não pagam multa nos empréstimos de obras "normais" e que nas obras de reserva aplicar um prazo especifico de entrega das obras e também que os docentes pagam a multa;
Pseudocódigo:

programa {
    funcao inicio() {
        cadeia perfil = "docente"
        cadeia tipoObra = "reserva"

        escreva("Prazo: ", prazoEmprestimo(perfil, tipoObra), " dias\n")
        escreva("Paga multa: ", pagaMulta(perfil, tipoObra), "\n")
    }

    funcao inteiro prazoEmprestimo(cadeia perfil, cadeia tipoObra) {
        se (perfil == "docente" e tipoObra != "reserva") {
            retorne 30
        }
        retorne 15
    }

    funcao logico pagaMulta(cadeia perfil, cadeia tipoObra) {
        se (perfil == "docente") {
            se (tipoObra == "reserva") {
                retorne verdadeiro   
            } senao {
                retorne falso        
            }
        }
        retorne verdadeiro
    }
}

3. R3 — «É aplicada uma multa de 0,50 € por dia a partir do terceiro dia de atraso.»
Ambiguidades encontradas: "a partir do terceiro dia" não deixa claro se começa a ser aplicada a multa no terceiro dia ou se só começa a contar após o terceiro dia completo, e também não esclarece se conta dias consecutivos ou dias uteis;
Como resolver: a multa começa a ser aplicada a partir do terceiro dia de atraso, são contabilizados dias consecutivos;
Pseudocódigo:

programa {
    funcao inicio() {
        cadeia perfil = "estudante"
        cadeia tipoObra = "normal"
        inteiro diasAtraso = 5

        escreva("Multa: ", calcularMulta(perfil, tipoObra, diasAtraso), " €\n")
    }

    funcao logico pagaMulta(cadeia perfil, cadeia tipoObra) {
        se (perfil == "docente") {
            se (tipoObra == "reserva") {
                retorne verdadeiro
            } senao {
                retorne falso
            }
        }
        retorne verdadeiro
    }

    funcao real calcularMulta(cadeia perfil, cadeia tipoObra, inteiro diasAtraso) {
        se (pagaMulta(perfil, tipoObra) == falso) {
            retorne 0.0
        }

        se (diasAtraso >= 3) {
            inteiro diasMulta = diasAtraso - 2
            retorne diasMulta * 0.5
        }
        retorne 0.0
    }
}

4. R4 — «As obras raras só podem ser consultadas na sala de leitura por utilizadores autorizados.»
Ambiguidades encontradas: "utilizadores autorizados" não esclarece quem pode fornecer essa autorização nem quais os critérios para tal, "consultadas na sala de leitura" não deixa claro se o acesso necessita de alguma aviso prévio ou se alguém que tenha autorização pode aceder a sala quando quiser;
Como resolver: Apenas utilizadores que tenham recebido uma autorização previa pela biblioteca tem acesso á sala, a consulta tem de ser obrigatoriamente presencial e que as obras raras não podem ser levadas para casa apenas tem acesso a elas dentro da sala de leitura;
Pseudocódigo:

programa {
    funcao inicio() {
        cadeia tipoObra = "rara"
        cadeia local = "sala de leitura"
        logico autorizado = verdadeiro

        escreva(podeConsultar(tipoObra, local, autorizado), "\n")
        escreva("Pode levar para casa: ", podeLevarParaCasa(tipoObra), "\n")
    }

    funcao cadeia podeConsultar(cadeia tipoObra, cadeia local, logico autorizado) {
        se (tipoObra == "rara") {
            se (local == "sala de leitura" e autorizado == verdadeiro) {
                retorne "Consulta permitida"
            } senao {
                retorne "Consulta negada"
            }
        }
        retorne "Regra R4 não aplicável"
    }

    funcao logico podeLevarParaCasa(cadeia tipoObra) {
        se (tipoObra == "rara") {
            retorne falso
        }
        retorne verdadeiro
    }
}
