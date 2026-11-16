# Entity Hunter

**Investigação de domínios e preparação de notificações para operações de takedown.**

Projeto desenvolvido como parte do case técnico para a posição de Coordenação de Operações de Golpes Digitais da Branddi.

**Aplicação pronta para uso:** https://case-branddi-entity-hunter.lovable.app  
**Código-fonte no GitHub:** https://github.com/Gabrielrf-tech/case-branddi-entity-hunter

## 1. Problema e proposta

Em uma operação de takedown, a investigação de uma URL pode exigir consultas em diferentes fontes para identificar o domínio, sua infraestrutura, as entidades relacionadas e os contatos disponíveis. Depois disso, o analista ainda precisa preparar uma comunicação adequada ao destinatário e à ocorrência.

Desenvolvi o **Entity Hunter** para concentrar essas atividades em uma interface web, reduzindo consultas repetitivas e o trabalho manual de preparação das notificações.

A proposta é apoiar o analista, não substituir sua avaliação ou automatizar decisões de remoção.

## 2. Funcionalidades

- Investigação de domínio a partir de uma URL.
- Consulta de dados públicos de RDAP, DNS e ASN.
- Organização de entidades por categoria, como registrant, registrar e ISP, conforme os dados disponíveis.
- Apresentação de contatos públicos, incluindo contatos de abuso e administrativos quando identificados.
- Identificação das fontes consultadas e indicação de limitações dos resultados.
- Seleção da entidade destinatária e do tipo de ocorrência.
- Geração de título e corpo de notificação, com campos editáveis e opções de cópia.
- Personalização dos modelos de notificação.
- Interface com temas claro e escuro.

A ferramenta não envia notificações automaticamente e não confirma remoções.

## 3. Como utilizar

O **Entity Hunter está pronto para uso, sem nenhuma instalação, apenas usando diretamente no navegador** pelo endereço:

https://case-branddi-entity-hunter.lovable.app

**Fluxo de utilização:**

1. Informar a URL que será investigada.
2. Executar a consulta e analisar as entidades, os contatos e as fontes retornadas.
3. Selecionar a entidade que receberia a comunicação.
4. Definir o tipo de ocorrência.
5. Preencher o nome do cliente e da marca afetada.
6. Revisar o título e o corpo da notificação gerada e copiar o conteúdo, se necessário.

A geração exige o preenchimento de destinatário, cliente e marca. A existência de dados técnicos ou de um contato público não comprova, isoladamente, uma irregularidade nem autoriza o envio da notificação.

### Exemplo de entrada e saída

**Entrada:** `https://www.casasbahia.com.br`

Na consulta documentada, o Entity Hunter apresentou informações de domínio e infraestrutura, identificou entidades relacionadas e permitiu selecionar a Akamai Technologies, Inc. como destinatária de uma notificação simulada.

Após a escolha da ocorrência e o preenchimento dos campos, a aplicação gerou um título e um corpo de mensagem editáveis.

Esse exemplo demonstra o funcionamento técnico da ferramenta. Não representa uma denúncia real, uma irregularidade comprovada ou autorização para representar a marca.

Os resultados e as capturas estão descritos em [`TESTES.md`](./TESTES.md).

## 4. Estrutura do projeto

O código-fonte está disponível no [repositório GitHub](https://github.com/Gabrielrf-tech/case-branddi-entity-hunter).

| Diretório ou arquivo | Finalidade |
|---|---|
| `src/components/entity-hunter/` | Interface de pesquisa, resultados, entidades, notificações e templates |
| `src/lib/investigation/` | Lógica de investigação e consultas a serviços externos |
| `src/routes/` | Rotas da aplicação |
| `src/integrations/supabase/` | Integração com Supabase |
| `src/test/` | Testes automatizados presentes no código |
| `package.json` | Dependências e configuração do projeto |
| `TESTES.md` | Testes, evidências e limitações |
| `PROJETO.md` | Análise e proposta operacional do case |
| `USO_DE_IA.md` | Registro do uso de inteligência artificial |

## 5. Tecnologias, fontes e dependências

O projeto utiliza React, TypeScript, TanStack Start, Vite e integração com Supabase. Foi desenvolvido com auxílio do Lovable.

As consultas técnicas utilizam serviços públicos, incluindo:

- **IANA RDAP:** descoberta de serviços RDAP.
- **Cloudflare DNS over HTTPS:** consultas DNS.
- **Google Public DNS:** fonte alternativa para consultas DNS.
- **RIPEstat:** informações de rede e ASN.

O acesso à aplicação publicada é feito diretamente pelo navegador. A disponibilidade e os resultados dependem também dos serviços externos utilizados. A manutenção e a operação em escala podem envolver custos de hospedagem, planos de serviços e limites de uso; não foi elaborado orçamento para operação em escala.

## 6. Limitações e cuidados

- As informações dependem da disponibilidade, atualização e cobertura das fontes externas.
- A identificação de um ISP ou de uma rede intermediária não comprova a hospedagem de origem.
- Contatos públicos podem estar ausentes, desatualizados ou não ser o canal adequado para determinada ocorrência.
- A ferramenta não verifica autorização comercial, titularidade de marca ou suficiência das evidências.
- Os textos gerados são rascunhos e exigem revisão humana antes do envio.
- O protótipo não envia denúncias, acompanha protocolos ou valida a remoção de conteúdos.
- Uma indisponibilidade temporária não deve ser tratada automaticamente como takedown confirmado.

## 7. Documentação complementar

- [`PROJETO.md`](./PROJETO.md) — diagnóstico, priorização, operação, indicadores e proposta de melhoria.
- [`TESTES.md`](./TESTES.md) — testes funcionais, cenários, resultados e limitações.
- [`USO_DE_IA.md`](./USO_DE_IA.md) — ferramentas utilizadas, decisões, revisões e contribuições da IA.

O Entity Hunter é um protótipo de apoio operacional, desenvolvido para demonstrar como a centralização de consultas e a preparação assistida de notificações podem reduzir atividades manuais sem retirar do analista a responsabilidade pelas decisões.
