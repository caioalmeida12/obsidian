Quando a tarefa se torna muito complexa para que a utilização do [[Zero-Shot Prompting]] baste, o Few-Shot Prompting pode ser uma boa opção. 
Consiste em, no prompt, incluir n exemplos de perguntas/respostas que sigam o mesmo padrão da que se deseja saber no prompt em questão. Geralmente, utiliza-se de [[Delimitadores de estrutura]] -- no exemplo em questão, são as // -- para tornar mais explícito à LLM o que está acontecendo.

Prompt:
```md
This is awesome! // Positive
This is bad! // Negative
Wow that movie was rad! // Positive
What a horrible show! //
```

Output:
```md
Negative
```

Existem limites para as capacidades de raciocínio dos prompts Few-Shot. Eles não são capazes de executar tarefas que possuam nivel de complexidade um pouco maior. Ex:

Prompt zero-shot:
```md
The odd numbers in this group add up to an even number: 15, 32, 5, 13, 82, 7, 1. 
A:
```

Output zero-shot:
```
Yes, the odd numbers in this group add up to 107, which is an even number.
```

Prompt few-shot: 
```md
The odd numbers in this group add up to an even number: 4, 8, 9, 15, 12, 2, 1.
A: The answer is False.

The odd numbers in this group add up to an even number: 17,  10, 19, 4, 8, 12, 24.
A: The answer is True.

The odd numbers in this group add up to an even number: 16,  11, 14, 4, 8, 13, 24.
A: The answer is True.

The odd numbers in this group add up to an even number: 17,  9, 10, 12, 13, 4, 2.
A: The answer is False.

The odd numbers in this group add up to an even number: 15, 32, 5, 13, 82, 7, 1. 
A: 
```

Output few-shot:
```md
The answer is True.
```

Essa limitação evidencia que são necessários modelos de linguagem capazes de raciocinar esses problemas mais complexos, envolvendo cálculos aritméticos, senso comum ou racionalização simbólica.

Quando a tarefa for muito complexa para um prompt few-shot, é comum recorrer ao [[Chain-of-Thought Prompting]].

#tcc/prompt/tecnica 