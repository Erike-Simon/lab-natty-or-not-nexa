# Natural ou Fake Natty? Como Vencer na Era das IAs Generativas

## 🚀 Introdução

> Woooow! Look at this 👀

Olá pessoal, Venilton da DIO aqui! Inspirado na hype _"Natty or Not"_ do fisiculturismo, este Lab da DIO te convida a conhecer o mundo das IAs Generativas, explorando o potencial dessas tendências tecnológicas incríveis!

## 🎯 Bora Pro Desafio!? Você Já Venceu 💪🤓

### Objetivos

1. **Explorar IAs Generativas**: Utilize essas tecnologias para criar conteúdos que sejam o mais realista possível. Seja criativo! Você pode produzir imagens, textos, áudios, vídeos ou combinações de tudo isso!
1. **Potfólio de Projetos**:
    1. Faça o "fork" deste repositório, criando uma cópia em seu GitHub pessoal;
    2. Edite seu README com os detalhes do seu projeto, siga nosso [Template](#template) (é só copiar, colar e preencher);
    3. Submeta o link do seu repositório na plataforma da DIO. Pronto, você acabou de fortalecer seu portfólio de projetos nos perfis do GitHub e DIO 🚀
1. **Efeito de Rede**: Compartilhe seus resultados nas redes sociais com a hashtag **#LabDIONattyOrNot**. Não esqueça de nos marcar: [DIO](https://www.linkedin.com/school/dio-makethechange) e [falvojr](https://www.linkedin.com/in/falvojr).

### Template

```markdown
# Título do Projeto Extremamente Aesthetic ;)

## 📒 Descrição
Meu projeto visa gerar uma base de dados fictícia para uma simulação de operação de uma empresa do ramo de alimentos PET.
É um projeto da disciplina Inovação Tecnológica, do curso de Pós Graduação em Engenharia e Análise de Dados da CESAR School.

O projeto deve conter:

- A ideia de negócio
- A definição do cliente com insights, dados e hipóteses levantadas
- o modelo de negócios com as camadas de negócios e camadas de dados explicadas-
- Um painel analítico com dados simulados da operação do modelo de negócios com os principais indicadores descritos na camada de dados

Para esse último entregável, foi necessária a geração de uma base de dados relativamente simples para simulação do painel analítico.
Então surgiu a ideia de escrever um prompt para o chat GPT com o auxílio também do Gemini, de maneira que ele me gerasse a base
exatamente adequada com as features necessárias.

## 🤖 Tecnologias Utilizadas

Chat GPT e Gemini.

## 🧐 Processo de Criação

Primeiro descrevi as ideias de negócio da empresa, definições do cliente e insights. A partir do modelo estruturado,
foi possível identificar quais dados seriam necessários para uma simulação básica de operação dessa empresa.

O modelo de prompt imputado no Chat GPT pode ser observado abaixo:

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                                                                                                                                                                                                                                            
Gere uma tabela .csv com as seguintes colunas:                                                                                                                                                                                                                               
                                                                                                                                                                                                                                                                            
- data: de 01/01/2021 até 31/12/2023 no formato dd-mm-yyyy de forma sequencial.                                                                                                                                                                                                
- qtd_avulso: inteiro no intervalo de 0 à 20.                                                                                                                                                                                                                               
- qtd_ass_mensal: quantidade diária de clientes que contratam assinatura mensal. numero inteiro no intervalo de 0 à 5 (incluindo o 0 e o 5).
  Os valores dessa coluna nunca devem ser negativos.                                                                                                                           
- qtd_churn_ass_mensal: quantidade de clientes que cancelam assinatura mensal. Varie esse valor aleatoriamente entre 0 e 3 (incluindo o 0 e o 2).
  Os valores dessa coluna nunca devem ser negativos.                                                                        
- qtd_acumulada_ass_mensal: quantidade acumulada de assinantes mensais. Incremente essa coluna somando o valor anterior e atual da coluna  'qtd_ass_mensal'
  e decremente do próximo valor dessa coluna também o valor anterior da coluna 'qtd_churn_ass_mensal'.            
- qtd_ass_tri: quantidade diária de clientes que contratam assinatura trimestral. numero inteiro no intervalo de 0 à 5 (incluindo o 0 e o 5).
  Os valores dessa coluna nunca devem ser negativos.                                                                            
- qtd_churn_ass_tri: quantidade de clientes que cancelam assinatura trimestral. Varie esse valor aleatoriamente entre 0 e 2 (incluindo o 0 e o 2).
  Os valores dessa coluna nunca devem ser negativos.                                                                       
- qtd_acumulada_ass_tri: quantidade acumulada de assinantes trimestrais. Incremente essa coluna somando o valor anterior e atual da coluna  'qtd_ass_tri'e
  decremente do próximo valor dessa coluna também o valor anterior da coluna 'qtd_churn_ass_tri'.                  
- faturamento: (qtd_acumulada_ass_tri * 279,90) + (qtd_acumulada_ass_mensal * 329,90) + (qtd_avulso * 12,90).                                                                                                                                                               
- custo: custo de operacional da empresa diário. esse valor não pode ser maior do que os valores da coluna 'faturamento'. Faça-o variar de maneira que
  o 'custo' diário oscile sempre em uma faixa de valor em torno de 40% a 70%  menor do que a coluna 'faturamento'.     
- custo_marketing: o custo de marketing diário da empresa. O valor dessa coluna deve ser sempre variar em torno de 5% a 10% do valor da coluna 'custo'.                                                                                                                     
                                                                                                                                                                                                                                                                            
-> Considerações sobre as assinaturas:                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                            
Cada mês deve ter no máximo 60 assinaturas (considerando 'qtd_ass_mensal' + 'qtd_ass_tri').                                                                                                                                                                                 
                                                                                                                                                                                                                                                                            
-> Considerações sobre os cancelamentos das assinaturas:                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                            
Cada mês deve ter no máximo 10 cancelamentos de assinaturas (considerando 'qtd_churn_ass_tri' + 'qtd_churn_ass_mensal').                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
Me exiba ao final um resumo das estatísticas por ano e do primeiro mês de cada ano e o arquivo .csv para download.                                                                                                                                                         
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🚀 Resultados

A base de dados .csv pode ser observada no repositório, junto com um notebook onde foram feitas algumas operações, gerações de gráficos e testes de verificação.

Um exemplo simples dos 5 primeiros registros do dataset:

data	    qtd_avulso	qtd_ass_mensal	qtd_churn_ass_mensal	qtd_acumulada_ass_mensal	qtd_ass_tri	 qtd_churn_ass_tri	qtd_acumulada_ass_tri	faturamento	custo	      custo_marketing
01-01-2021	6	        1	            0	                    0	                        1	         0	                0	                    77.4	     53.728794	  2.981580
02-01-2021	19	        1	            0	                    1	                        0	         0	                0	                    575.0	     267.035041	  25.150481
03-01-2021	14	        0	            0	                    1	                        2	         0	                2	                    1070.3	     449.708223	  30.196326
04-01-2021	10	        2	            0	                    3	                        1	         0	                3	                    1958.4	     1132.844732  95.378170
05-01-2021	7	        1	            0	                    4	                        1	         0	                4	                    2529.5	     1572.488978  80.617469

## 💭 Reflexão

Não foi tão fácil obter o conjunto de dados da maneira que imaginava. Até o chat GPT entender realmente o que eu queria, tive que fazer diversos ajustes e descrições
específicas das colunas para ajustar uma sem interferir nos valores das demais. Um problema que tive e não consegui contornar muito bem sem prejudicar o resto dos dados
foram as imputações de churn para assinaturas mensais e trimestrais. Sempre que estes dados eram ajustados, valores negativos surgiam nestas colunas mesmo estando explicito
na descrição que isso não deveria acontecer. Resolvi então zerar esses dados e imputar de outra maneira nos próximos passos do projeto de inovação.
No mais, foi de extrema importância obter essa base de dados como ponto de partida para melhores decisões nos próximos passos do projeto.

```

### Exemplos e Insigths

- [E-BOOK](/exemplos/E-BOOK.md)
- [Podcast](/exemplos/PODCAST.md)
- [Vídeo (Avatar Virtual)](/exemplos/VIDEO.md)

## Links Interessantes

[Base10: If You’re Not First, You’re Last: How AI Becomes Mission Critical](https://base10.vc/post/generative-ai-mission-critical/)

![Base10's Trend Map Generative AI](https://github.com/digitalinnovationone/lab-natty-or-not/assets/730492/f4df26e8-f8f7-4419-8252-c69d73ea930c)
