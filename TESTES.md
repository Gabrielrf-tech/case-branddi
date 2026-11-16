# TESTES — Entity Hunter

## 1. Objetivo e condições

Desenvolvi o Entity Hunter para facilitar uma das etapas mais trabalhosas do takedown: investigar um domínio, identificar possíveis entidades responsáveis e seus contatos e preparar uma notificação adequada ao destinatário e ao tipo de ocorrência.

Durante o desenvolvimento, realizei consultas com mais de dez URLs de diferentes categorias, incluindo marketplaces, lojas virtuais e sites institucionais. O objetivo foi observar a qualidade dos dados retornados, a organização das entidades e o funcionamento do gerador de notificações.

A aplicação está disponível publicamente em:

https://case-branddi-entity-hunter.lovable.app

Os testes foram realizados pela interface web, utilizando informações públicas. Nenhuma denúncia real foi enviada.

Os cenários de risco apresentados adiante incluem situações hipotéticas do case e decisões que permanecem sob responsabilidade do analista. Não representam cinco execuções independentes do protótipo.

## 2. Teste funcional documentado

**Entrada:** `https://www.casasbahia.com.br`

**Resultado esperado:** consultar as informações técnicas disponíveis, identificar possíveis entidades e contatos, permitir a seleção do destinatário e gerar uma notificação editável conforme a ocorrência.

**Resultado obtido:**

- Investigação concluída, com identificação de duas entidades: VIA VAREJO S/A, classificada como registrant, e Akamai Technologies, Inc., classificada como ISP.
- Apresentação de contatos públicos, diferenciando contato de abuso e contato administrativo.
- Identificação das fontes de consulta e seus resultados.
- Aviso de que os dados de rede não confirmam a hospedagem de origem.
- Geração de título e corpo de notificação para o tipo de ocorrência selecionado, com possibilidade de edição e cópia.

Para demonstrar o gerador, utilizei um preenchimento de teste com a marca Casas Bahia e a Akamai como destinatária. A notificação não foi enviada. O teste não representa uma alegação de irregularidade, autorização de representação ou denúncia contra o domínio consultado.

**Resultado:** fluxo de investigação e preparação de notificação executado conforme esperado.

**Limites:** os dados retornados dependem das fontes externas; a identificação de um ISP não comprova o provedor de hospedagem; o texto gerado exige revisão humana antes de qualquer utilização.

## 3. Cenários de risco e revisão humana

| Cenário | Esperado e tratamento previsto | Resultado ou limite identificado |
|---|---|---|
| **Caso completo** | Consultar domínio, selecionar entidade, definir ocorrência, informar cliente e marca e preparar notificação. | Fluxo executado no teste documentado. |
| **URL, data ou evidência faltante** | Solicitar complementação e evitar conclusões sem sustentação. | A ferramenta exige destinatário, cliente e marca para gerar o texto, exibindo aviso quando não preenchidos. A suficiência das demais evidências depende do analista. |
| **Possível parceiro não validado** | Confirmar a relação comercial com o cliente antes de tratar a atividade como irregular. | A ferramenta não determina se uma empresa é parceira autorizada. A decisão permanece humana. |
| **Indisponibilidade sem remoção confirmada** | Verificar a ocorrência em diferentes condições e não confundir indisponibilidade com takedown. | O Entity Hunter não confirma remoções. A validação e a classificação do resultado são externas ao protótipo. |
| **Acesso contradiz encerramento** | Revisar o encerramento quando a ocorrência continuar acessível em outro dispositivo ou rede. | A verificação em diferentes ambientes e a decisão de reabertura permanecem no fluxo operacional do analista. |

Os quatro últimos cenários representam avaliações de risco e condutas previstas, não testes completos de remoção executados na ferramenta.

## 4. Falhas, melhorias e reteste

Durante o desenvolvimento, identifiquei que a apresentação de informações em excesso dificultava a leitura dos resultados e a identificação dos contatos mais relevantes.

A versão atual apresenta as entidades agrupadas por categoria, diferencia contatos de abuso e administrativos, informa as fontes utilizadas e destaca limitações importantes, como a impossibilidade de confirmar a hospedagem de origem apenas pelos dados de rede.

Também permite selecionar a entidade, definir a ocorrência e gerar uma notificação utilizando modelos editáveis.

A consulta documentada de `www.casasbahia.com.br` demonstra o funcionamento dessa versão revisada. Não foram realizadas medições isoladas de cada correção.

## 5. Comparação antes e depois

No processo manual, a investigação de um domínio, a identificação de entidades e contatos e a preparação de uma notificação podem levar aproximadamente **5 a 10 minutos**, considerando minha experiência operacional.

Com o Entity Hunter, o fluxo demonstrado pode ser realizado em **menos de 1 minuto**: informar a URL, investigar, selecionar a entidade, definir a ocorrência, preencher cliente e marca e gerar o texto.

| Critério | Processo manual | Entity Hunter |
|---|---|---|
| Consulta de infraestrutura | Consultas separadas | Consulta centralizada |
| Identificação de contatos | Pesquisa e conferência manual | Contatos públicos organizados por entidade |
| Preparação da notificação | Redação ou preenchimento de modelo externo | Geração de rascunho conforme os campos selecionados |
| Tempo estimado | 5–10 minutos | Menos de 1 minuto |
| Revisão humana | Necessária | Necessária |

**Amostra e condições:** foram consultadas mais de dez URLs durante o desenvolvimento. A evidência detalhada apresentada neste documento corresponde a uma consulta completa. Os tempos são estimativas operacionais, não resultados de um experimento cronometrado com amostras pareadas.

O ganho observado está relacionado à redução de etapas manuais. Não representa remoção efetiva de conteúdo nem garante a correção de todas as informações retornadas.

## 6. Evidências e conclusão

As capturas da consulta documentada mostram a identificação das entidades, a notificação gerada, as fontes consultadas e a configuração dos modelos. As imagens serão acrescentadas ao final deste documento na publicação do repositório.

O Entity Hunter demonstrou capacidade de apoiar a investigação técnica e a preparação de notificações, concentrando atividades que normalmente exigiriam diferentes consultas e ferramentas.

A decisão de notificar, a validação das evidências, a confirmação da entidade competente e a verificação de remoção continuam sob responsabilidade do analista.

Como evolução, considero importante ampliar os testes com amostras controladas, medir tempos de execução e qualidade das notificações e acompanhar eventuais falhas das fontes externas antes de propor uma utilização operacional mais ampla.
