# T4 – Compressão sem perdas: Huffman e entropia

Original = 8 bits/carácter (ASCII). Custo da tabela (hipótese): por símbolo, 8 bits (símbolo) + 4 bits (comprimento) + bits do código.

## Caso comum: `A_BIBLIOTECA_DIGITAL_DO_ISPGAYA` (N=31, 14 símbolos)

**Frequências, entropia e códigos**

| Símbolo | fᵢ | pᵢ | −pᵢ·log₂pᵢ | Código | lᵢ |
|---|---|---|---|---|---|
| A | 5 | 0.1613 | 0.4246 | `110` | 3 |
| I | 5 | 0.1613 | 0.4246 | `111` | 3 |
| ␣(_) | 4 | 0.1290 | 0.3812 | `010` | 3 |
| B | 2 | 0.0645 | 0.2551 | `0011` | 4 |
| D | 2 | 0.0645 | 0.2551 | `0110` | 4 |
| G | 2 | 0.0645 | 0.2551 | `0111` | 4 |
| L | 2 | 0.0645 | 0.2551 | `1000` | 4 |
| O | 2 | 0.0645 | 0.2551 | `1001` | 4 |
| T | 2 | 0.0645 | 0.2551 | `1010` | 4 |
| C | 1 | 0.0323 | 0.1598 | `10110` | 5 |
| E | 1 | 0.0323 | 0.1598 | `10111` | 5 |
| P | 1 | 0.0323 | 0.1598 | `0000` | 4 |
| S | 1 | 0.0323 | 0.1598 | `0001` | 4 |
| Y | 1 | 0.0323 | 0.1598 | `0010` | 4 |

H = 3.5600 bits/símbolo; entropia total = 110.36 bits.

**Construção da árvore** (juntam-se os dois menores: 1.º → 0, 2.º → 1; N = nó novo)

- Passo 1: junta C(1) [0] + E(1) [1] → N1(2)
- Passo 2: junta P(1) [0] + S(1) [1] → N2(2)
- Passo 3: junta Y(1) [0] + B(2) [1] → N3(3)
- Passo 4: junta D(2) [0] + G(2) [1] → N4(4)
- Passo 5: junta L(2) [0] + O(2) [1] → N5(4)
- Passo 6: junta T(2) [0] + N1(2) [1] → N6(4)
- Passo 7: junta N2(2) [0] + N3(3) [1] → N7(5)
- Passo 8: junta ␣(_)(4) [0] + N4(4) [1] → N8(8)
- Passo 9: junta N5(4) [0] + N6(4) [1] → N9(8)
- Passo 10: junta A(5) [0] + I(5) [1] → N10(10)
- Passo 11: junta N7(5) [0] + N8(8) [1] → N11(13)
- Passo 12: junta N9(8) [0] + N10(10) [1] → N12(18)
- Passo 13: junta N11(13) [0] + N12(18) [1] → N13(31)

**Cadeia codificada** (112 bits):

`1100100011111001110001111001101010111101101100100110111011111110101101000010011010010101110001000001111100010110`

**Métricas**

| Métrica | Valor |
|---|---|
| Original | 248 bits |
| Comprimido | 112 bits |
| L | 3.6129 bits/símbolo |
| Eficiência H/L | 98.54 % |
| Razão de compressão | 2.2143 |
| Taxa de compressão | 45.16 % |
| Ganho | 54.84 % |
| Tabela de códigos | 223 bits |
| Ganho com tabela | (1 − 335/248) × 100 = -35.08 % |

## Caso do grupo: `BIBLIOPI_ISPGAYA_RECURSOS_DIGITAIS` (N=34, 16 símbolos)

**Frequências, entropia e códigos**

| Símbolo | fᵢ | pᵢ | −pᵢ·log₂pᵢ | Código | lᵢ |
|---|---|---|---|---|---|
| I | 7 | 0.2059 | 0.4694 | `00` | 2 |
| S | 4 | 0.1176 | 0.3632 | `010` | 3 |
| A | 3 | 0.0882 | 0.3090 | `1101` | 4 |
| ␣(_) | 3 | 0.0882 | 0.3090 | `1110` | 4 |
| B | 2 | 0.0588 | 0.2404 | `11111` | 5 |
| G | 2 | 0.0588 | 0.2404 | `0110` | 4 |
| O | 2 | 0.0588 | 0.2404 | `0111` | 4 |
| P | 2 | 0.0588 | 0.2404 | `1000` | 4 |
| R | 2 | 0.0588 | 0.2404 | `1001` | 4 |
| C | 1 | 0.0294 | 0.1496 | `10100` | 5 |
| D | 1 | 0.0294 | 0.1496 | `10101` | 5 |
| E | 1 | 0.0294 | 0.1496 | `10110` | 5 |
| L | 1 | 0.0294 | 0.1496 | `10111` | 5 |
| T | 1 | 0.0294 | 0.1496 | `11000` | 5 |
| U | 1 | 0.0294 | 0.1496 | `11001` | 5 |
| Y | 1 | 0.0294 | 0.1496 | `11110` | 5 |

H = 3.7004 bits/símbolo; entropia total = 125.81 bits.

**Construção da árvore** (juntam-se os dois menores: 1.º → 0, 2.º → 1; N = nó novo)

- Passo 1: junta C(1) [0] + D(1) [1] → N1(2)
- Passo 2: junta E(1) [0] + L(1) [1] → N2(2)
- Passo 3: junta T(1) [0] + U(1) [1] → N3(2)
- Passo 4: junta Y(1) [0] + B(2) [1] → N4(3)
- Passo 5: junta G(2) [0] + O(2) [1] → N5(4)
- Passo 6: junta P(2) [0] + R(2) [1] → N6(4)
- Passo 7: junta N1(2) [0] + N2(2) [1] → N7(4)
- Passo 8: junta N3(2) [0] + A(3) [1] → N8(5)
- Passo 9: junta ␣(_)(3) [0] + N4(3) [1] → N9(6)
- Passo 10: junta S(4) [0] + N5(4) [1] → N10(8)
- Passo 11: junta N6(4) [0] + N7(4) [1] → N11(8)
- Passo 12: junta N8(5) [0] + N9(6) [1] → N12(11)
- Passo 13: junta I(7) [0] + N10(8) [1] → N13(15)
- Passo 14: junta N11(8) [0] + N12(11) [1] → N14(19)
- Passo 15: junta N13(15) [0] + N14(19) [1] → N15(34)

**Cadeia codificada** (127 bits):

`1111100111111011100011110000011100001010000110110111110110111101001101101010011001100101001110101110101010001100011000110100010`

**Métricas**

| Métrica | Valor |
|---|---|
| Original | 272 bits |
| Comprimido | 127 bits |
| L | 3.7353 bits/símbolo |
| Eficiência H/L | 99.06 % |
| Razão de compressão | 2.1417 |
| Taxa de compressão | 46.69 % |
| Ganho | 53.31 % |
| Tabela de códigos | 261 bits |
| Ganho com tabela | (1 − 388/272) × 100 = -42.65 % |

## Interpretação

Em ambos os casos L fica muito perto de H (eficiência ≈ 99 %), e o ganho bruto ronda os 53–55 %. Mas a tabela de códigos ocupa mais bits do que os dados comprimidos, pelo que, em cadeias curtas, o ficheiro final fica maior do que o original (ganho negativo). O Huffman compensa em textos longos.

## Compressão com perdas no BiblioPI

- **JPEG** (imagem): capas e digitalizações; descarta detalhe visual pouco percetível (DCT + quantização).
- **MP3** (áudio): audiolivros e podcasts; descarta sons mascarados pelo ouvido (modelo psicoacústico).
- **MP4** (vídeo): vídeos de formação; usa a semelhança entre fotogramas.

Usam-se na consulta/streaming, em que o tamanho importa mais do que a fidelidade; o texto e os metadados ficam sem perdas.
