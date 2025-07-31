**Questões e Respostas**

**Perguntas**

1.  Explique por que o escalonamento do processador é necessário na maioria dos sistemas operacionais modernos.
2.  Compare os escalonadores "Preemptivo" e "Não-preemptivo". Qual tipo é mais comum e por quê?
3.  Descreva três objetivos distintos que um escalonador pode ter, considerando diferentes tipos de sistemas (todos os sistemas, sistemas em lote, interativos ou de tempo real).

**Respostas**

1.  O escalonamento do processador é necessário porque, na maioria dos casos, o número de processos prontos para executar é maior que o número de processadores disponíveis. Isso exige que o sistema escolha qual processo da fila de prontos irá usar a CPU e por quanto tempo.
2.  Um escalonador "Preemptivo" pode interromper um processo em execução a qualquer momento, retomando-o posteriormente. Já um escalonador "Não-preemptivo" permite que um processo, uma vez em execução, não seja retirado da CPU até que termine sua execução ou fique bloqueado. Os escalonadores preemptivos são os mais comuns, pois aproveitam melhor o tempo de CPU e E/S em sistemas multitarefa.
3.  Três objetivos distintos que um escalonador pode ter são:
    * **Justiça (Todos os sistemas):** Dar a cada processo uma porção justa da CPU.
    * **Vazão (Sistemas em lote):** Maximizar o número de tarefas concluídas por hora.
    * **Tempo de Resposta (Sistemas interativos):** Responder rapidamente às requisições dos usuários.
    * (Alternativamente) **Cumprimento dos Prazos (Sistemas de tempo real):** Evitar a perda de dados em sistemas que exigem respostas dentro de limites de tempo estritos.
