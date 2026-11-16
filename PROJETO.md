# PROJETO — Coordenação de Operações de Golpes Digitais

**Case técnico Branddi | Cliente fictício: Nativa Home**

## 1. Diagnóstico e priorização das ocorrências

Minha primeira preocupação ao receber uma fila de denúncias seria diferenciar o risco efetivo de cada ocorrência da quantidade de informações disponíveis.

Nem todo uso de marca representa fraude. Da mesma forma, um ativo com pouco alcance pode representar um risco elevado quando direciona consumidores para um golpe já identificado.

Para definir a ordem de atendimento, considero o potencial de dano financeiro, a existência de vítimas, a atividade atual do golpe, o alcance do canal, a confirmação do cliente e a relação com outras ocorrências.

A priorização não é definitiva: novas evidências podem alterar tanto a criticidade quanto a ordem de execução.

| Prioridade | Caso | Justificativa | Primeira ação |
|---|---|---|---|
| **1 — Crítica** | **A — Site falso** | Domínio não reconhecido pelo cliente, identidade visual copiada, cobrança via Pix, duas vítimas relatadas e site ativo. | Preservar evidências, investigar a infraestrutura e identificar os canais de notificação pertinentes. |
| **2 — Alta** | **B — Instagram** | Perfil com 18 mil seguidores, promoção com link externo e três relatos de cobrança por mensagem privada. | Preservar publicações, mensagens e links; confirmar com o cliente a inexistência de vínculo comercial. |
| **3 — Alta** | **F — Reincidência** | Novo domínio com identidade visual e chave Pix semelhantes às de um site anteriormente denunciado. | Investigar o novo ativo e relacionar as evidências à ocorrência anterior, sem presumir autoria comum. |
| **4 — Alta, pendente de evidências** | **D — Falso suporte** | Solicitação de pagamentos e denúncia anterior recusada por insuficiência de evidências. | Recuperar URL ou ID, capturas datadas e motivo da recusa antes de reenviar. |
| **5 — Média** | **C — Facebook** | Página recente e de menor alcance que direciona ao domínio fraudulento do caso A. | Preservar a página e o redirecionamento, aproveitando a investigação do domínio relacionado. |
| **6 — Em validação** | **E — Possível parceiro** | Revenda e utilização de imagens da marca, sem alegação de oficialidade ou relatos de fraude. | Confirmar com o cliente a relação comercial e os direitos envolvidos antes de qualquer denúncia. |

### Evidências faltantes e critérios de revisão

**Caso A:** complementar capturas datadas, registros de pagamento e relatos das vítimas. Novas vítimas ou novos domínios relacionados reforçariam a necessidade de resposta imediata.

**Caso B:** obter identificadores do perfil, mensagens, publicações e confirmação do cliente sobre eventuais parcerias. A confirmação de fraude financeira ativa poderia elevar sua criticidade.

**Caso F:** preservar o novo domínio, dados técnicos, identidade visual e evidências relacionadas à chave Pix. A semelhança entre ativos indica uma possível conexão, mas não comprova que possuem os mesmos responsáveis.

**Caso D:** identificar o ativo exato e corrigir a deficiência documental que levou à recusa anterior. A gravidade potencial não justifica repetir uma denúncia sem os elementos necessários.

**Caso C:** preservar o vínculo com o domínio do caso A. O atendimento pode ocorrer de forma coordenada, sem perder o registro individual da página.

**Caso E:** consultar o cliente sobre autorização comercial e uso da marca. A ausência de um revendedor na lista de parceiros não comprova, isoladamente, uma infração.

**Primeiros atendimentos: A, B e F.** A execução dos demais casos continuaria conforme a disponibilidade de evidências, a criticidade e a capacidade da equipe.

## 2. Execução dos casos A e C

Para a condução das ocorrências, considero indispensáveis a investigação, a preservação de evidências, a identificação do destinatário adequado, a notificação, o acompanhamento e a validação do resultado.

O envio de uma denúncia representa uma etapa do processo, não sua conclusão.

### 2.1. Caso A — Site falso com cobrança via Pix

**Investigação e evidências**

O caso A exige atendimento prioritário por envolver um site ativo, utilização da identidade da Nativa Home, cobrança via Pix e relatos de duas vítimas.

Iniciaria pela preservação da URL, capturas da página, data e horário da coleta, ofertas apresentadas, elementos de identidade visual, instruções de pagamento e relatos disponíveis. Também confirmaria com o cliente que o domínio não pertence à sua operação legítima.

Na investigação técnica, utilizaria RDAP/WHOIS, DNS, IP e ASN para identificar as entidades relacionadas ao domínio e à infraestrutura. A análise buscaria distinguir registrador, operador de rede, serviços intermediários e possível provedor de hospedagem.

Essa distinção é importante porque um IP associado a uma CDN ou a outro serviço intermediário não comprova onde o conteúdo está hospedado. A escolha do destinatário deve considerar sua competência para atuar sobre o recurso denunciado.

**Notificação e encaminhamento**

Com as evidências organizadas, encaminharia a comunicação ao canal pertinente, descrevendo a ocorrência de forma objetiva e apresentando o vínculo com a marca, os indícios de fraude e os registros disponíveis.

A notificação conteria o ativo denunciado, a descrição da conduta, as evidências, a solicitação de providências e os dados necessários para acompanhamento.

Em uma infraestrutura intermediada pela Cloudflare, por exemplo, avaliaria seu canal de abuso e buscaria identificar o provedor de origem, sem presumir que o serviço intermediário controla diretamente a hospedagem.

Cada encaminhamento seria registrado com destinatário, canal, data, fundamento, evidências e protocolo, quando fornecido.

**Acompanhamento e escalonamento**

Após a notificação, acompanharia as respostas e realizaria verificações periódicas do ativo.

Em caso de silêncio, faria reiterações documentadas, considerando os prazos internos e os canais disponíveis. Diante de recusa, avaliaria a justificativa, a suficiência das evidências e a possibilidade de complementação ou encaminhamento por outro canal competente.

A criticidade do caso justificaria acompanhamento próximo pela coordenação, especialmente diante de novas vítimas ou da identificação de outros domínios relacionados.

**Validação do resultado**

No cenário de acompanhamento considerado, o domínio deixa de responder em verificações realizadas por diferentes redes e dispositivos, mas não há confirmação de remoção pela entidade acionada.

Registraria o resultado como **indisponibilidade observada, sem causa confirmada**.

Não classificaria o caso como takedown confirmado. Uma eventual conclusão administrativa dependeria dos critérios acordados com o cliente, preservando o histórico, a incerteza sobre a causa e a possibilidade de reabertura.

### 2.2. Caso C — Página do Facebook vinculada ao caso A

**Investigação e evidências**

A página apresenta identidade visual relacionada à Nativa Home e direciona usuários ao domínio investigado no caso A.

Preservaria a URL e o identificador da página, publicações relevantes, imagens, ofertas, datas de coleta e evidências do direcionamento ao site falso.

O vínculo entre os ativos seria registrado no histórico das duas ocorrências. Essa associação permite aproveitar a investigação já realizada, sem afirmar que os responsáveis pela página e pelo domínio são necessariamente as mesmas pessoas.

**Notificação e encaminhamento**

Com o dossiê organizado, utilizaria o canal de denúncia aplicável da Meta, apresentando a utilização da identidade da marca e o direcionamento ao site fraudulento.

A comunicação destacaria os elementos verificáveis e a relação com o caso A, evitando uma denúncia genérica baseada apenas na semelhança visual.

O registro incluiria data do envio, canal, evidências, protocolo quando disponível e prazo para acompanhamento.

**Acompanhamento e validação**

No cenário de acompanhamento considerado, a Meta comunica a remoção da página. O analista realiza uma nova verificação e confirma que o ativo não está mais acessível.

Nesse caso, registraria **remoção confirmada pela plataforma**, preservando tanto a resposta recebida quanto a evidência da verificação.

A diferença em relação ao caso A é fundamental: aqui existe confirmação da entidade responsável, enquanto no primeiro caso foi observada apenas a indisponibilidade.

### 2.3. Critérios de decisão

Em ambos os casos, considero essenciais a qualidade das evidências, a identificação do destinatário adequado e a rastreabilidade das ações.

As decisões de reiteração, escalonamento, encerramento ou reabertura devem permanecer registradas, permitindo continuidade por outro analista e acompanhamento pela coordenação.

Os canais e as políticas de abuso aplicáveis devem ser verificados nas fontes oficiais dos serviços envolvidos. Dados técnicos de domínio e infraestrutura não substituem as regras de denúncia das plataformas nem comprovam autoria.

## 3. Registro, validação e reincidência

### 3.1. Rastreabilidade das ocorrências

Utilizaria um registro individual para cada ativo, com identificação do cliente, URL ou ID, categoria, criticidade, responsável, evidências, destinatários acionados, comunicações, protocolos, status e próxima ação.

O histórico precisa permitir compreender o que foi investigado, quais decisões foram tomadas, quais respostas foram recebidas e por que determinado resultado foi classificado daquela forma.

**Exemplo de acompanhamento do caso A:**

| Etapa | Registro operacional |
|---|---|
| Recebimento | Site suspeito, uso de marca e relatos de pagamento via Pix |
| Triagem | Criticidade crítica, com atendimento imediato pelo risco financeiro e vítimas relatadas |
| Investigação | Preservação das evidências e identificação de entidades relacionadas |
| Encaminhamento | Notificação ao canal pertinente, com dossiê e protocolo quando disponível |
| Acompanhamento | Reiterações e verificações periódicas |
| Verificação | Site indisponível em diferentes condições de acesso |
| Resultado | Indisponibilidade observada; remoção não confirmada |
| Próxima ação | Acompanhar respostas e aplicar os critérios de conclusão acordados com o cliente |

Os registros operacionais também devem incluir datas, horários, responsáveis e referências às evidências de cada etapa.

### 3.2. Validação de resultados

Para validar uma ocorrência, não consideraria suficiente uma única tentativa de acesso.

A verificação deve observar, conforme o tipo de ativo:

- Acesso em diferentes redes, dispositivos ou navegadores.
- URL exata e eventuais redirecionamentos.
- Data e horário das verificações.
- Respostas recebidas das plataformas ou entidades notificadas.
- Persistência do conteúdo denunciado ou reaparecimento em outro endereço.

Uma mensagem de erro, bloqueio localizado ou indisponibilidade temporária não comprova remoção definitiva.

Os resultados devem ser classificados separadamente, distinguindo remoção confirmada, indisponibilidade sem causa confirmada e outras formas de resolução ou encerramento administrativo.

### 3.3. Encerramento contradito por novo relato

No cenário em que um ativo foi encerrado após uma única checagem e um consumidor posteriormente relata acesso pelo celular, minha primeira decisão seria reabrir a análise.

Preservaria o histórico do encerramento anterior, registraria o novo relato e solicitaria a reprodução do acesso, incluindo URL, dispositivo, rede, horário e evidências disponíveis.

O analista repetiria as verificações em ambientes distintos. Confirmada a permanência do conteúdo, retomaria as tratativas e corrigiria o status da ocorrência.

Também avaliaria a necessidade de revisar os critérios de encerramento adotados pela equipe, evitando a repetição do problema.

### 3.4. Reincidência e novos ativos

Quando a mesma URL volta a apresentar o conteúdo denunciado, considero apropriado reabrir a ocorrência original, preservando as ações anteriores.

Quando surge um novo domínio ou perfil, criaria um registro próprio e o vincularia aos casos relacionados, quando houver evidências suficientes.

Elementos como identidade visual, chave Pix, conteúdo, redirecionamentos e infraestrutura podem ajudar a identificar relações entre ocorrências, mas não comprovam, isoladamente, autoria comum.

Essa organização permite identificar padrões, evitar retrabalho e tratar campanhas relacionadas de forma coordenada, sem perder a rastreabilidade de cada ativo.

## 4. Diagnóstico e gestão da operação

O cenário apresenta uma equipe formada por três analistas e uma pessoa na coordenação, com uma fila de primeiras análises durante uma semana de cinco dias.

| Indicador operacional | Quantidade |
|---|---:|
| Fila inicial | 60 |
| Novas ocorrências | 120 |
| Primeiras análises concluídas | 90 |
| **Fila final** | **90** |
| Denúncias enviadas | 40 |
| Ativos indisponíveis na checagem final | 24 |
| Remoções confirmadas | 8 |
| Indisponibilidades sem causa confirmada | 16 |

**Cálculo da fila:**

60 + 120 − 90 = **90 ocorrências pendentes de primeira análise**.

A fila cresceu em 30 ocorrências na semana. Isso demonstra que o volume de novas entradas superou a capacidade de primeiras análises no período.

O dado não permite concluir, isoladamente, que a equipe esteja com baixo desempenho. Antes de definir medidas, avaliaria a complexidade das ocorrências, o tempo gasto em cada etapa, a distribuição da demanda e os principais gargalos.

As 40 denúncias enviadas não devem ser subtraídas da fila de primeiras análises, pois representam outra etapa do processo.

Da mesma forma, dos 24 ativos indisponíveis, apenas oito possuem confirmação de remoção. Os outros 16 não podem ser apresentados como takedowns confirmados.

### 4.1. Organização do fluxo

**Recebimento → triagem → priorização → investigação → validação de evidências → notificação → acompanhamento → verificação → encerramento ou reabertura.**

Na triagem, classificaria as ocorrências por criticidade e identificaria possíveis agrupamentos por plataforma, domínio, campanha ou características relevantes.

Defendo que os analistas mantenham responsabilidade pelo fluxo integral dos casos, mas com redistribuição dinâmica para equilibrar a fila e aproveitar especializações.

Casos relacionados podem ser tratados em conjunto sem perder seus registros individuais.

A coordenação acompanharia capacidade, prioridades, qualidade das evidências e gargalos, participando diretamente das investigações críticas quando necessário.

Para ocorrências de maior impacto, utilizaria alinhamentos rápidos ou war rooms, especialmente quando houver múltiplos ativos, vítimas ou dependência de outras áreas.

### 4.2. Metas internas de atendimento

Como ponto de partida, adotaria metas internas diferenciadas por criticidade:

| Criticidade | Primeira análise | Primeira notificação, quando cabível |
|---|---|---|
| Crítica | Até 2 horas | Até 6 horas |
| Alta | Até 4 horas | Até 12 horas |
| Média | Até 1 dia útil | Até 2 dias úteis |
| Baixa | Até 2 dias úteis | Até 3 dias úteis |

Esses prazos são referências propostas para organização da operação, não compromissos contratuais da Branddi ou prazos de resposta das plataformas.

Sua aplicação dependeria do horário operacional, da disponibilidade de evidências, das particularidades do cliente e da necessidade de validações adicionais.

O objetivo não seria enviar denúncias incompletas para cumprir uma meta, mas identificar rapidamente o que falta e evitar que a ocorrência permaneça sem encaminhamento.

## 5. Indicadores de gestão

Escolhi três KPIs que permitem avaliar capacidade, velocidade e resultado, sem confundir volume de atividades com remoções efetivas.

### KPI 1 — Taxa de cobertura das entradas

**Fórmula:**

Primeiras análises concluídas no período ÷ novas ocorrências recebidas no período × 100.

**Resultado do cenário:**

90 ÷ 120 × 100 = **75%**.

O indicador permite avaliar se a capacidade de primeiras análises acompanha o volume de novas entradas.

A comparação utiliza volumes do período. Como as análises concluídas podem incluir ocorrências da fila inicial, o resultado não significa necessariamente que 75% das novas ocorrências específicas tenham sido analisadas.

**Fonte:** registros de entrada e conclusão da primeira análise no sistema de casos.

**Acompanhamento:** diário, com consolidação semanal.

**Decisão apoiada:** redistribuição de capacidade, identificação de crescimento da fila e revisão dos processos que consomem mais tempo.

### KPI 2 — Tempo até a primeira notificação

**Fórmula:**

Média de (data e hora da primeira notificação − data e hora de recebimento), considerando os casos efetivamente notificados e segmentando por criticidade.

Esse indicador permite identificar atrasos entre o recebimento, a investigação e o primeiro encaminhamento.

**Fonte:** histórico de eventos e notificações.

**Acompanhamento:** diário e semanal, com análise por criticidade.

**Decisão apoiada:** identificação de gargalos, revisão de prioridades e avaliação da necessidade de apoio ou automação.

O cenário fornecido não apresenta os horários necessários para calcular esse KPI.

### KPI 3 — Tempo até resolução validada, por motivo

**Fórmula:**

Média de (data e hora da resolução − data e hora de abertura), agrupada pelo motivo de resolução dos casos concluídos.

Separaria pelo menos:

- Remoção confirmada pela entidade responsável.
- Resolução por ajuste ou providência aceita pelo cliente.
- Encerramento administrativo sem confirmação da causa da indisponibilidade.

Casos ainda abertos permaneceriam fora da média de resolvidos e seriam acompanhados separadamente.

**Fonte:** histórico dos casos, registros de encerramento e evidências de validação.

**Acompanhamento:** semanal e mensal.

**Decisão apoiada:** avaliar o tempo de resolução por tipo de desfecho, identificar atrasos e evitar que encerramentos administrativos sejam confundidos com remoções confirmadas.

O cenário não apresenta datas suficientes para calcular esse indicador.

### Leitura conjunta dos indicadores

A taxa de cobertura mostra se a equipe acompanha a entrada de ocorrências. O tempo até a primeira notificação revela a velocidade do encaminhamento. O tempo até a resolução validada permite avaliar os desfechos.

Também manteria visíveis os volumes absolutos de denúncias enviadas, ativos indisponíveis e remoções confirmadas, pois esses números contextualizam os KPIs, mas não são equivalentes entre si.

## 6. Projeto de melhoria operacional — Entity Hunter

### 6.1. Problema identificado

Na investigação de uma URL, o analista frequentemente precisa alternar entre ferramentas para consultar domínio, DNS, infraestrutura e contatos de abuso.

Depois dessas consultas, ainda precisa selecionar o destinatário adequado e preparar manualmente uma notificação ou preencher um modelo externo.

Esse processo consome tempo, favorece retrabalho e pode dificultar a identificação dos contatos mais relevantes.

Minha proposta foi atacar esse gargalo específico, em vez de tentar desenvolver uma plataforma completa de gestão de takedowns.

### 6.2. Solução desenvolvida

O **Entity Hunter** é uma aplicação web que centraliza consultas técnicas e auxilia na preparação de notificações.

**Aplicação:** https://case-branddi-entity-hunter.lovable.app

**Código-fonte:** https://github.com/Gabrielrf-tech/case-branddi-entity-hunter

A ferramenta permite:

- Informar uma URL e consultar dados públicos de domínio e infraestrutura.
- Visualizar entidades relacionadas e seus contatos disponíveis.
- Diferenciar contatos administrativos e de abuso, quando identificados.
- Consultar as fontes utilizadas e observar ressalvas sobre os dados.
- Selecionar a entidade destinatária e o tipo de ocorrência.
- Informar cliente e marca para gerar título e corpo de notificação editáveis.
- Personalizar modelos de comunicação.

A aplicação utiliza serviços públicos de RDAP, DNS e ASN, incluindo IANA RDAP, Cloudflare DNS, Google Public DNS e RIPEstat.

A inteligência artificial foi utilizada como apoio ao desenvolvimento e ao refinamento da solução. Isso não significa que o protótipo utilize um modelo de linguagem para decidir automaticamente sobre cada consulta ou denúncia.

### 6.3. Comparação dos fluxos

**Fluxo manual:**

Receber URL → consultar fontes separadamente → identificar entidades e contatos → selecionar destinatário → preparar notificação em modelo externo → revisar.

**Fluxo com Entity Hunter:**

Informar URL → analisar resultados centralizados → selecionar entidade → definir ocorrência e cliente/marca → gerar rascunho → revisar.

O protótipo não substitui a validação do cliente, a análise de evidências, o envio das denúncias, o acompanhamento dos protocolos ou a confirmação de remoções.

### 6.4. Resultados e testes

Durante o desenvolvimento, consultei mais de dez URLs de diferentes categorias, incluindo marketplaces, lojas virtuais e sites institucionais.

A demonstração documentada utiliza `www.casasbahia.com.br` para verificar o funcionamento técnico e a geração simulada de uma notificação. A consulta não representa uma alegação de irregularidade contra o domínio.

Pela minha experiência operacional, o processo manual de consulta e preparação de texto pode levar aproximadamente **5 a 10 minutos**.

O fluxo assistido demonstrado pode ser realizado em **menos de 1 minuto**, passando pela consulta, seleção da entidade, definição da ocorrência, preenchimento dos campos e geração do texto.

Esses tempos são estimativas operacionais, não medições cronometradas em condições controladas. Também não representam ganho comprovado em taxa de remoção.

Durante o desenvolvimento, identifiquei excesso de informações na apresentação dos resultados. A versão revisada passou a organizar melhor as entidades, destacar contatos relevantes e apresentar limitações das fontes.

Os resultados, as condições e as evidências estão documentados em [`TESTES.md`](./TESTES.md).

### 6.5. Regras, exceções e revisão humana

A geração de notificações exige destinatário, cliente e marca. Quando esses campos não são preenchidos, a interface solicita sua complementação.

Além dessa validação, o analista deve revisar ou interromper o encaminhamento quando houver:

- Evidências insuficientes ou desatualizadas.
- Possibilidade de parceiro comercial autorizado.
- Contato ou entidade sem competência confirmada para a tratativa.
- Incerteza sobre a hospedagem de origem.
- Alegação de representação da marca ainda não validada.
- Indisponibilidade sem confirmação de remoção.

O Entity Hunter não determina automaticamente se existe fraude, não envia denúncias e não encerra casos.

Essas decisões permanecem sob responsabilidade do analista e devem ser registradas no sistema de acompanhamento da operação.

## 7. Implantação, riscos e evolução

Minha proposta seria iniciar com um piloto supervisionado, mantendo revisão humana obrigatória e utilizando ocorrências fictícias ou previamente autorizadas.

### Etapa 1 — Validação técnica

Verificar a consistência dos dados, a disponibilidade das fontes, a qualidade dos contatos retornados e o funcionamento dos modelos de notificação.

### Etapa 2 — Piloto assistido

Disponibilizar a ferramenta para um grupo reduzido de analistas, acompanhando o uso e registrando situações que exigem correção manual.

### Etapa 3 — Comparação operacional

Comparar o esforço necessário, a qualidade das informações e a necessidade de correções em relação ao processo manual.

A avaliação deve considerar não apenas velocidade, mas também a precisão dos destinatários e a adequação dos rascunhos produzidos.

### Etapa 4 — Ampliação gradual

Com resultados satisfatórios, avaliar integrações com o sistema de casos, histórico de consultas, registro de evidências e acompanhamento de notificações.

Essa evolução dependeria de priorização conjunta com Produto, Engenharia e DevOps, considerando impacto operacional, segurança, custo e manutenção.

### Critérios para ampliar ou interromper

Ampliaria o piloto se os resultados demonstrassem redução consistente do esforço manual, boa identificação dos destinatários e qualidade suficiente dos rascunhos após revisão.

Interromperia ou restringiria o uso diante de erros frequentes na atribuição de entidades, contatos inadequados, falhas persistentes das fontes externas ou geração de comunicações que induzissem a conclusões sem evidências.

Os principais riscos são:

- Dependência da disponibilidade e atualização de serviços externos.
- Informações públicas incompletas ou desatualizadas.
- Identificação incorreta da infraestrutura ou da competência do destinatário.
- Utilização de textos gerados sem revisão e validação da representação do cliente.
- Ampliação prematura da ferramenta sem critérios de qualidade definidos.

A evolução deve ser orientada por métricas reais, validação dos usuários e redução de riscos, não apenas pela quantidade de funcionalidades implementadas.

## 8. Considerações finais

Minha proposta combina três frentes: **qualidade da investigação, controle da operação e melhoria contínua com tecnologia**.

A prioridade é agir rapidamente diante de golpes com potencial de dano, sem transformar hipóteses em fatos ou confundir indisponibilidade com remoção confirmada.

Na gestão, busco equilibrar capacidade, criticidade e qualidade, utilizando indicadores que apoiem decisões e não apenas contabilizem atividades.

O Entity Hunter representa uma melhoria prática dentro dessa visão: reduzir consultas repetitivas e facilitar a preparação de notificações, mantendo o analista responsável pela validação das informações e pelos encaminhamentos.

O objetivo não é automatizar decisões sensíveis, mas permitir que a equipe dedique mais tempo à investigação, ao acompanhamento e à resolução dos casos.
