# USO DE INTELIGÊNCIA ARTIFICIAL

## 1. Ferramentas utilizadas

Para o desenvolvimento do Entity Hunter, utilizei duas ferramentas de inteligência artificial: **ChatGPT (OpenAI)** e **Lovable**.

Escolhi o ChatGPT por considerá-lo uma das principais ferramentas de IA generativa conversacional disponíveis no mercado. Além de ser amplamente reconhecido, possui uma interface intuitiva e uma versão gratuita com recursos suficientes para discutir soluções, explorar alternativas técnicas e estruturar instruções de desenvolvimento.

O Lovable foi escolhido pela facilidade de transformar requisitos em uma aplicação web funcional, especialmente para quem já conhece seu funcionamento. Seu plano gratuito também oferece recursos consistentes para desenvolver, testar e aprimorar um protótipo sem investimento inicial.

Utilizei o ChatGPT principalmente para discutir a estrutura da solução, esclarecer dúvidas técnicas e preparar instruções de implementação. No Lovable, desenvolvi a aplicação e realizei ajustes na interface e nas funcionalidades a partir dos resultados obtidos.

O processo foi iterativo: defini os requisitos, implementei as funcionalidades, testei o comportamento da aplicação e utilizei as ferramentas para corrigir os problemas identificados.

## 2. Processo de desenvolvimento com IA

Entre os dias **10 e 16 de novembro de 2026**, utilizei o ChatGPT para desenvolver a proposta do Entity Hunter antes de iniciar sua implementação no Lovable.

Comecei discutindo problemas comuns da operação de takedown e alternativas para reduzir tarefas manuais. A partir dessas conversas, fui refinando a ideia até chegar a uma ferramenta que centralizasse informações técnicas de uma URL e facilitasse a preparação de notificações.

Em vez de solicitar diretamente a criação de uma aplicação, utilizei o ChatGPT para construir o escopo por meio de perguntas, questionamentos e ajustes sucessivos. Discutimos quais dados seriam necessários, como identificar entidades e contatos, quais informações deveriam aparecer na interface e como organizar o fluxo de trabalho do analista.

Com os requisitos definidos, utilizei essas discussões para estruturar um prompt mais completo para o Lovable, descrevendo as funcionalidades, a organização visual, os campos necessários e o comportamento esperado da aplicação. Dessa forma, o desenvolvimento começou com uma especificação mais clara, reduzindo a necessidade de alterações estruturais posteriores.

## 3. Evolução da solução

A primeira versão funcional já permitia realizar consultas técnicas e preparar notificações, mas os testes mostraram oportunidades de melhoria.

Um dos principais problemas foi o excesso de informações apresentadas nos resultados. Algumas classificações também precisavam ser ajustadas para evitar interpretações incorretas sobre as entidades responsáveis pela infraestrutura.

Retomei essas questões com apoio da IA e refinei as instruções enviadas ao Lovable. A versão revisada passou a organizar melhor as entidades, destacar os contatos relevantes e apresentar as fontes e limitações das consultas.

Mantive as funcionalidades que atendiam ao objetivo inicial, como a centralização das informações e a geração de notificações editáveis. Corrigi problemas de classificação e apresentação dos dados e descartei elementos que não contribuíam diretamente para o trabalho do analista.

Esse processo de revisão também foi importante para delimitar o papel da ferramenta: o Entity Hunter auxilia na investigação e na preparação das comunicações, mas não substitui a análise humana nem determina automaticamente a responsabilidade das entidades identificadas.

## 4. Testes e validação

Após as implementações, testei a aplicação com mais de dez URLs de diferentes categorias, verificando as informações retornadas, os contatos identificados e o funcionamento do gerador de notificações.

Quando encontrava resultados inadequados ou informações pouco úteis, utilizava esses exemplos para formular novas instruções de correção, implementava os ajustes e repetia as verificações.

Também avaliei o preenchimento dos campos obrigatórios, a edição dos textos e a apresentação das fontes consultadas.
