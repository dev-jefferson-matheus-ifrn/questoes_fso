**Questões e Respostas**

**1. Explique a diferença fundamental entre um disco rígido (HDD) e um disco de estado sólido (SSD) em termos de hardware e performance.**

**Resposta:** A principal diferença entre um HDD (Hard Disk Drive) e um SSD (Solid State Drive) reside em seu hardware e, consequentemente, em sua performance. [cite_start]HDDs são dispositivos mecânicos que utilizam um ou vários discos (platter) que giram, com braços e cabeças de leitura/escrita para acessar os dados[cite: 221, 222, 223, 236, 237, 238]. Essa natureza mecânica os torna mais lentos. [cite_start]Já os SSDs são discos de estado sólido[cite: 242, 243], o que significa que não possuem partes móveis, armazenando dados em memória flash. [cite_start]Isso lhes confere velocidades significativamente maiores, podendo chegar a 7GB/s, e eles vêm substituindo os HDDs devido a essa performance superior[cite: 244, 245].

**2. Descreva a divisão lógica de um disco rígido tradicional em termos de cilindro, trilha e setor. Qual a importância dessa organização para o funcionamento do disco?**

[cite_start]**Resposta:** Um disco rígido tradicional é dividido logicamente em cilindros, trilhas e setores[cite: 224, 225, 226, 227]. [cite_start]Uma trilha (track) é um círculo concêntrico em cada disco (platter)[cite: 230, 236]. [cite_start]Um setor (sector) é uma subdivisão de uma trilha, sendo a menor unidade de armazenamento do disco[cite: 231]. [cite_start]Um cilindro (cylinder) é o conjunto de todas as trilhas que estão na mesma posição em todos os discos de um HD[cite: 234]. Essa organização é fundamental porque define como os dados são fisicamente armazenados e acessados no disco, permitindo que o braço de leitura/escrita se posicione precisamente para ler ou gravar informações.

**3. Compare os níveis RAID 0 e RAID 1, destacando suas principais características, um benefício e uma desvantagem para cada um.**

**Resposta:**
* **RAID 0:**
    * [cite_start]**Características:** Divide os dados em "faixas" (strips) e os distribui por múltiplos discos[cite: 257, 279].
    * [cite_start]**Benefício:** Oferece maior performance de leitura e escrita devido à paralelização dos dados[cite: 258, 280].
    * [cite_start]**Desvantagem:** Possui menor segurança, pois a falha de qualquer disco resulta na perda de todos os dados do arranjo[cite: 259, 280].
* **RAID 1:**
    * [cite_start]**Características:** Cria um backup exato (espelhamento) de cada drive, duplicando os dados em dois discos ou mais[cite: 261, 297].
    * [cite_start]**Benefício:** Oferece boa segurança e redundância, pois se um disco falhar, os dados ainda estão disponíveis no disco espelho[cite: 263]. [cite_start]A escrita é igual à leitura, podendo ser até 2x mais rápida na leitura[cite: 298].
    * **Desvantagem:** Há um custo maior, pois exige o dobro da capacidade de armazenamento para guardar a mesma quantidade de dados.

**4. Quais são os principais objetivos de um sistema de arquivos? Cite as duas operações básicas que ele deve suportar.**

[cite_start]**Resposta:** Os principais objetivos de um sistema de arquivos são[cite: 342, 346]:
* [cite_start]Armazenar uma grande quantidade de informação[cite: 342, 346].
* [cite_start]Garantir que as informações sobrevivam ao término do processo[cite: 342, 346].
* [cite_start]Permitir que múltiplos processos acessem os dados simultaneamente[cite: 342, 346].

[cite_start]As duas operações básicas que um sistema de arquivos deve suportar são Leitura e Escrita[cite: 342, 346].

**5. Em sistemas de arquivos, o que são "caminho absoluto" e "caminho relativo"? Dê um exemplo de cada um.**

**Resposta:**
* **Caminho Absoluto:** É um caminho completo para um arquivo ou diretório, começando sempre pela raiz do sistema de arquivos. [cite_start]Ele define a localização exata do arquivo independentemente do diretório de trabalho atual[cite: 352].
    * [cite_start]**Exemplo:** `/home/Tadeu/Aulas/Aula4.ppt` [cite: 352]
* **Caminho Relativo:** É um caminho que considera o diretório atual ou diretório de trabalho do processo. [cite_start]Ele especifica a localização do arquivo ou diretório em relação ao diretório onde o usuário (ou processo) está atualmente[cite: 352].
    * [cite_start]**Exemplo:** `Aulas/Aula4.ppt` (se o diretório atual for `/home/Tadeu`)[cite: 352].
    * [cite_start]As entradas `.` (diretório atual) e `..` (diretório pai) são usadas em caminhos relativos[cite: 353].
