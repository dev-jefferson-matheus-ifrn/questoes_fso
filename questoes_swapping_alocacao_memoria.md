**Questões**

1.  Explique a principal diferença entre "swap out" e "swap in" no contexto de swapping de memória.
2.  [cite_start]Descreva o problema da fragmentação da memória que ocorre com o swapping[cite: 59]. [cite_start]Como a compactação da memória busca resolver isso [cite: 91][cite_start], e por que essa estratégia não é comumente utilizada na prática[cite: 163, 164]?
3.  [cite_start]Qual é o papel da Memory Management Unit (MMU) na memória virtual[cite: 178, 179]? [cite_start]O que são endereços virtuais e endereços físicos[cite: 179]?
4.  Considere uma memória de 2 Gigabytes que está separada em blocos de 16 bytes. Qual deve ser o tamanho do mapa de bits para esta memória? (Considere 1 GB = 1.000.000.000 bytes). Justifique sua resposta.
5.  Compare os algoritmos Worst Fit e Quick Fit para alocação de memória. Descreva uma vantagem e uma desvantagem de cada um.

**Respostas**

1.  [cite_start]"Swap out" é o processo de retirar um processo da memória principal (RAM) e copiar seu conteúdo para a memória secundária (HD/SSD) quando o espaço na RAM é insuficiente[cite: 23]. [cite_start]Já o "swap in" ocorre quando esse processo precisa ser executado novamente, sendo trazido de volta da memória secundária para a memória principal[cite: 24, 25, 26].
2.  [cite_start]O problema da fragmentação da memória surge após diversas operações de swap-in e swap-out, onde a memória pode ficar com espaços livres não contíguos [cite: 60][cite_start], desperdiçando áreas que são muito pequenas para novos processos[cite: 77, 78, 81]. [cite_start]A compactação da memória tenta resolver isso movendo todos os processos para baixo na memória, fazendo com que ele ocupe os espaços vazios abaixo do seu endereço base[cite: 162]. [cite_start]No entanto, essa estratégia não é normalmente usada [cite: 163] [cite_start]devido ao tempo excessivo necessário para mover todos os processos para o fim da memória, que seria muito grande comparado com o tempo de troca de contexto[cite: 164].
3.  [cite_start]A Memory Management Unit (MMU) é responsável pela tradução de endereços virtuais para endereços físicos[cite: 179]. [cite_start]Endereços virtuais são os endereços que são acessados pelo processo [cite: 179][cite_start], enquanto endereços físicos são os endereços reais da memória[cite: 179].
4.  Para calcular o tamanho do mapa de bits:
    * Tamanho da memória: 2 Gigabytes = $2 \times 1.000.000.000$ bytes = $2.000.000.000$ bytes.
    * Tamanho do bloco: 16 bytes.
    * Número total de blocos: $2.000.000.000 \text{ bytes} / 16 \text{ bytes/bloco} = 125.000.000$ blocos.
    * [cite_start]Cada bloco é representado por 1 bit no mapa de bits[cite: 193].
    * Tamanho do mapa de bits em bits: $125.000.000$ bits.
    * Tamanho do mapa de bits em bytes: $125.000.000 \text{ bits} / 8 \text{ bits/byte} = 15.625.000$ bytes.
    * [cite_start]Justificativa: O mapa de bits utiliza 1 bit para cada área de tamanho X bytes para informar se está ocupada (1) ou livre (0)[cite: 193]. [cite_start]Portanto, o consumo de espaço para o mapa é fixo e proporcional ao tamanho da memória[cite: 194].
5.  * **Worst Fit (Pior encaixe):**
        * [cite_start]**Vantagem:** Irá percorrer toda a lista para encontrar o espaço que "desperdiçará" o máximo possível [cite: 203][cite_start], e esse espaço desperdiçado pode ser depois alocado para outro processo[cite: 203].
        * [cite_start]**Desvantagem:** Exige percorrer toda a lista para encontrar o maior espaço[cite: 203].
    * **Quick Fit (Encaixe rápido):**
        * [cite_start]**Vantagem:** Cria várias listas de espaços livres agrupadas por tamanhos comuns de alocação[cite: 203], o que pode acelerar o processo de encontrar um espaço livre.
        * **Desvantagem:** A complexidade de gerenciar múltiplas listas pode ser maior.
