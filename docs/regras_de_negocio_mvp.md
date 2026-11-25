# Regras de negócio do MVP

O projeto tem duas áreas públicas, **Apoio gratuito** e **Serviços e vagas**. A visitante pode pesquisar, abrir os detalhes e seguir para o canal externo de atendimento ou candidatura. As referências na última coluna correspondem aos IDs do documento de requisitos do MVP.

## Acesso e perfis

| ID | Regra | Requisitos relacionados |
|---|---|---|
| RN01 | A visitante pode pesquisar, consultar detalhes e acessar canais externos nas duas áreas sem criar conta. | RF01, RNF03 |
| RN02 | O cadastro público permite criar contas de profissional, ONG ou empresa. A equipe atribui o perfil de administrador fora do cadastro público. | RF09, RNF02 |
| RN03 | Profissionais e ONGs podem enviar ofertas de serviço. Empresas podem enviar vagas de emprego. | RF09, RF10 |
| RN04 | O ofertante autenticado só pode acompanhar o status, editar ou inativar as próprias ofertas. Somente o administrador pode aprovar ou devolver para correção uma oferta ou edição submetida. | RF11, RF12, RNF02 |

## Apoio gratuito

| ID | Regra | Requisitos relacionados |
|---|---|---|
| RN05 | A área identifica cada item como **serviço ou programa gratuito** ou **canal oficial de suporte**. Cada item informa instituição responsável, tipo de atendimento, região atendida, critérios de participação, como acessar e contato ou link oficial. | RF02, RF03 |
| RN06 | Somente o administrador pode cadastrar, atualizar ou inativar itens de Apoio gratuito. Itens inativos ficam indisponíveis na área pública. | RF04, RNF02 |
| RN07 | A busca usa tipo de apoio e cidade. Um filtro de cidade mantém visíveis os canais oficiais de abrangência nacional. | RF02 |
| RN08 | O acesso a **Ver serviços de profissionais e ONGs** está disponível mesmo quando a busca de Apoio gratuito fica sem resultados. Na transição, a categoria e a cidade selecionadas são preservadas quando informadas. | RF05 |

## Serviços e vagas

| ID | Regra | Requisitos relacionados |
|---|---|---|
| RN09 | Uma oferta de serviço deve ter título, categoria, descrição, profissional ou ONG responsável, cidade/UF, modalidade e um canal de contato. O registro profissional é informado quando aplicável. Critérios de atendimento são opcionais. O contato pode ser WhatsApp, e-mail ou link externo. | RF07, RF10 |
| RN10 | Uma vaga deve ter cargo, empresa, descrição, cidade/UF ou indicação de trabalho remoto, requisitos da vaga e um canal externo de candidatura por link ou e-mail. | RF08, RF10 |
| RN11 | O catálogo de Serviços e vagas oferece filtros por categoria e cidade. Preços ficam fora dos campos públicos, dos filtros e dos detalhes. As páginas públicas mostram o canal autorizado pelo ofertante. | RF06, RF07, RF08, RNF03 |
| RN12 | Atendimento, contato e candidatura acontecem pelo canal externo informado. | RF01, RF07, RF08 |

## Publicação e revisão

| ID | Regra | Requisitos relacionados |
|---|---|---|
| RN13 | Toda nova oferta vai para revisão como **Pendente**. Ela só aparece no catálogo após a aprovação de um administrador. | RF10, RF12, RNF05 |
| RN14 | Ao enviar a edição de uma oferta publicada, o titular escolhe entre manter a versão já aprovada no ar durante a revisão ou suspender a exibição da oferta. A versão editada só fica pública após aprovação. | RF11, RF12, RNF05 |
| RN15 | Ao aprovar a edição, o administrador libera a versão revisada para substituir a versão anterior, inclusive quando o titular escolheu ocultar a oferta durante a análise. | RF11, RF12, RNF05 |
| RN16 | Ao devolver uma oferta ou edição para correção, o administrador registra um motivo que o titular pode consultar. A versão devolvida fica indisponível ao público. Depois de corrigir e reenviar, o conteúdo volta para a fila de revisão como **Pendente**. | RF11, RF12, RNF05 |
| RN17 | Quando o titular inativa uma oferta, ela sai do catálogo e o detalhe público fica indisponível. A listagem e o acesso por link direto seguem as mesmas regras de visibilidade. | RF11, RNF05 |

## Exemplos de visibilidade para homologação

| Cenário | Resultado esperado |
|---|---|
| Uma ONG envia um serviço novo. | A ONG acompanha o status **Pendente**. A visitante não encontra o serviço na busca nem abre o detalhe pelo link direto. |
| Uma empresa edita uma vaga e escolhe manter a versão aprovada. | A visitante abre a versão já aprovada. O administrador analisa a edição. Após aprovação, a versão revisada substitui a anterior. |
| Um profissional edita um serviço e escolhe suspender a exibição durante a revisão. | O serviço fica indisponível na listagem e no detalhe público enquanto a edição aguarda aprovação. Ao aprovar, a versão revisada passa a ser exibida. |
| O administrador devolve um envio para correção. | O titular vê o motivo. A versão devolvida fica fora do catálogo. Após o reenvio, o conteúdo retorna à fila. |
| O titular inativa uma oferta. | A oferta sai da busca e seu detalhe fica indisponível pelo link direto. |


