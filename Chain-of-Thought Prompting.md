Esse método de prompt se utiliza das forças do [[Few-Shot Prompting]] para tornar as LLMs capazes de "raciocinar" e tratar de problemas mais complexos do que os que as técnicas anteriores. O Chain-of-thought consiste em um processo de três passos: {entrada, pensamento, saída} [[Chain-of-Thought Prompting Elicits Reasoning in Large Language Models]]. A chain-of-thought propriamente dita se refere à série de passos em linguagem natural que está inclusa no passo de  "pensamento". Chain-of-thought prompting, então, é o nome dessa abordagem.

Uma CoT possui diversas propriedades atrativas que podem facilitar às LLMs o processo de geração de respostas:

 1 - CoTs permitem à LLM decompor processos complexos em pequenos problemas de múltiplas etapas, o que significa que computação adicional pode ser alocada para problemas que necessitam de mais passos. Isso segue os princípios da [[Decomposição da tarefa para operações complexas]].

2 - CoTs permitem visualizar o processo da LLM desde o momento em que ela recebeu uma tarefa até a parte em que ela gera uma resposta, tornando possível melhor debug e conhecimento sobre o funcionamento dela.

3 - CoTs podem ser aplicadas em tarefas como matemática, senso comum e manipulação simbólica. Há, ainda, o potencial de CoTs serem capazes de resolver qualquer tarefa que humanos possam resolver via linguagem.

4 - CoTs podem ser ensinadas a qualquer modelo existente, desde que possuam parâmetros e contexto suficientes, simplesmente incluindo exemplos por meio de [[Few-Shot Prompting]].



#tcc/prompt/tecnica 