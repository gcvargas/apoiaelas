O MVP terá **Apoio gratuito** e **Serviços e vagas**, ambos acessíveis sem login. A jornada termina quando a pessoa abre o canal externo de atendimento ou candidatura.

## Requisitos funcionais

| ID | Requisito | Critério de aceite |
|---|---|---|
| **RF01** | Permitir acesso público às duas áreas. | Uma visitante consegue pesquisar, abrir detalhes e acessar os canais externos sem criar conta. |
| **RF02** | Permitir buscar serviços e programas gratuitos por tipo de apoio e cidade. | A área distingue programas gratuitos de canais oficiais de suporte. Os canais de abrangência nacional continuam visíveis com o filtro de cidade aplicado. |
| **RF03** | Exibir as condições de acesso ao apoio gratuito. | Cada item mostra instituição, tipo de atendimento, região atendida, critérios de participação, como acessar e contato ou link oficial. |
| **RF04** | Permitir que a equipe mantenha a lista de apoio gratuito. | Um administrador consegue cadastrar, atualizar e inativar itens. Itens inativos deixam de aparecer na área pública. |
| **RF05** | Permitir que a visitante navegue de **Apoio gratuito** para o catálogo de serviços. | O botão **Ver serviços de profissionais e ONGs** mantém a categoria e a cidade selecionadas, quando houver. Ele também fica disponível quando a busca não retorna resultados. |
| **RF06** | Permitir buscar serviços e vagas no catálogo. | A visitante consegue filtrar por categoria e cidade, abrir os resultados e limpar os filtros. O catálogo não tem filtro nem campo público de preço. |
| **RF07** | Exibir os detalhes de um serviço e seu canal de contato. | O detalhe mostra título, categoria, descrição, profissional ou ONG, cidade/UF, modalidade, registro profissional quando aplicável e um canal de contato. Critérios de atendimento aparecem quando informados. O canal pode ser WhatsApp, e-mail ou link externo. |
| **RF08** | Exibir os detalhes de uma vaga e seu canal de candidatura. | O detalhe mostra cargo, empresa, descrição, cidade/UF ou indicação de trabalho remoto, requisitos e um canal de candidatura por link ou e-mail. |
| **RF09** | Permitir cadastro, login e saída de ofertantes. | Profissionais, ONGs e empresas conseguem criar conta, entrar e sair. O perfil administrativo é atribuído pela equipe fora do cadastro público. |
| **RF10** | Permitir que ofertantes enviem ofertas para aprovação. | Profissionais e ONGs conseguem enviar serviços. Empresas conseguem enviar vagas. Toda oferta nova fica pendente até a aprovação. |
| **RF11** | Permitir que ofertantes acompanhem, editem e inativem as próprias ofertas. | O ofertante vê o status em sua área. Uma edição fica pendente e seu conteúdo só aparece após aprovação. Ao inativar, a oferta deixa de aparecer publicamente. Ofertante decide se a versão anterior continua no catálogo enquanto a edição aguarda aprovação ou se a oferta inteira sai do ar |
| **RF12** | Permitir que administradores revisem novas ofertas e edições. | O administrador consegue consultar a fila, abrir o conteúdo enviado e aprovar ou devolver para correção. Uma versão devolvida fica fora da publicação, e o ofertante consegue consultar o motivo. |

## Requisitos não funcionais

| ID | Requisito | Como verificar |
|---|---|---|
| **RNF01** | **Segurança da autenticação.** Usar HTTPS no ambiente publicado, armazenar senhas com hash e invalidar a sessão após a saída. | Conferir a conexão HTTPS e testar o acesso a uma rota privada após sair da conta. |
| **RNF02** | **Controle de acesso.** A API verifica o perfil e a titularidade nas operações privadas. | Um ofertante não consegue editar a oferta de outra conta nem aprovar uma publicação, mesmo fazendo a requisição diretamente à API. |
| **RNF03** | **Privacidade.** A busca pública dispensa dados pessoais da visitante. A API pública retorna apenas dados da oferta e contatos autorizados para divulgação. | Percorrer a jornada sem preencher dados pessoais e conferir que e-mails de login e informações internas ficam fora das respostas públicas. |
| **RNF04** | **Usabilidade e acessibilidade.** As jornadas principais funcionam em celular e computador, com controles rotulados e foco visível ao navegar por teclado. | Testar busca, filtros, detalhes e contato nos dois tamanhos de tela e percorrer os principais controles usando o teclado. |
| **RNF05** | **Consistência da publicação.** A listagem e o detalhe público aplicam as mesmas regras de visibilidade. | Tentar abrir pelo link direto uma oferta nova pendente, uma versão não aprovada e uma oferta inativada. Nenhuma delas deve ser exibida. |
| **RNF06** | **Execução reproduzível.** Os repositórios documentam a instalação, o uso do Docker e as variáveis de ambiente. Credenciais ficam fora do Git. | Um integrante consegue subir o projeto a partir de clones limpos seguindo a documentação. |

**Condição da entrega inicial:** a demonstração usa dados fictícios. Confirmação de e-mail e recuperação de senha ficam para depois do MVP.
