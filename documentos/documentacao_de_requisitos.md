# Atores do Sistema
Esta seção descreve os atores do sistemas, suas atribuições e seus papéis no sistema.

## Papel dos atores
### Administrador (Admin)
|  Descrição | Papel  | Insumos ao sistema  |
|---|---|---|
|  O admin é o ator que deverá cadastrar novas Instituições e serviços de acolhimento sempre que necessário verificando a integridade dos mesmos. |  Para que o sistema possa cumprir seu objetivo e resolver o problema proposto é necessário que o admin mantenha sempre atualizada a lista de instituições e serviços cadastrados. | Manter Instituições e serviços de Acolhimento  |

### Visitante
|  Descrição | Papel  | Insumos ao sistema  |
|---|---|---|
|  O visitante é o ator que deverá visualizar as Instituições e serviços apresentados pelo Acolhe+. |  Para possibilitar que o sistema realize seu objetivo é necessário que o visitante visualize as Instituições e serviços, e caso escolha algum de sua preferência, o selecione e será direcionado a plataforma do mesmo por meio de links ou formas de contato. | Visualizar lista de Instituições e Serviços  |

### Sistema
|  Descrição | Papel  | Insumos ao sistema  |
|---|---|---|
|  É o próprio sistema e suas funcionalidades. |  Exibe as informações necessárias e realiza o direcionamento as outras plataformas. | Exibição das informações necessárias. Direcionamento a plataformas cadastradas no sistema.|

# Requisitos Gerais do Sistema
Tomando por base o contexto do sistema, esta seção descreve os requisitos que foram identificados.

## Requisitos Funcionais
|ID|Descrição|Prioridade|Requisitos Relacionados|
|:---:|---|---|:---:|
|RF001|O sistema deve listar plataformas de acolhimento ou grupos de apoio previamente cadastradas.|Essencial||
|RF002|O sistema deve permitir que o visitante selecione plataformas e grupos.|Importante|RF001|
|RF003|O sistema deve exibir informações detalhadas da plataforma selecionada. (Como funciona, meios para contato, como utilizar o serviço)|Importante|RF001, RF002|
|RF004|O sistema pode aceitar sugestões de novas plataformas. (pré-cadastros que devem passar pela aprovação de um administrador)|Desejável|
|RF005|O sistema deve permitir que o administrador visualize todas as sugestões de plataformas.|Desejável|RF004|
|RF006|O sistema deve permitir que o admin cadastre novas instituições na base de dados do sistema.|Importante||
|RF007|O sistema deve permitir que o visitante adicione comentários.|Desejável|RF002|
|RF008|O sistema deve exibir comentários adicionados por visitantes.|Desejável|RF002, RF007|

## Requisitos Não Funcionais
|ID|Descrição|Categoria|Prioridade|
|:---:|---|---|:---:|
|RNF001| O sistema deve utilizar React, React Native e NodeJS.|Requisisto de Implementação|Importante
|RNF002| Apenas o usuário com privilégio de acesso admin poderá visualizar e excluir sugestões de visitantes.|Requisisto de Segurança|Essencial
|RNF003| O sistema deve se comunicar entre Web, Mobile e API Rest.| Requisito de Interoperabilidade|Essencial
|RNF004| O login de admin deverá estar oculto no sistema.| Requisisto de Segurança|Importante
|RNF005| As telas devem ter um padrão de interface.| Requisito de Usabilidade| Importante

## Regras de Negócio
|ID|Descrição|Prioridade|Requisitos Relacionados|
|:---:|---|---|:---:|
|RN001|O sistema não terá contato com as instituições, o objetivo é juntar informações, portanto, não se responsabiliza pela demora, ou qualidade do atendimento.|Essencial||
|RN002|O sistema não apresentará aos visitantes quaisquer dados de cunho privado.|Importante||
|RN003|O sistema não deve registrar dados de usuários visitantes.|Essencial||
|RN004|O comentário realizado pelo visitante deve estar atrelado a uma instituição (plataforma).|Importante|RF008|