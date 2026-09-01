MailBridge

Extensão local para apoiar a comunicação após migrações de ramais para o Teams Phone. A extensão lê a descrição de chamados abertos no Cervello, identifica nome, ramal e e-mail, permite revisão e prepara mensagens no cliente de e-mail padrão.

Funcionalidades:
- Popup dinâmico.
- Captura da página atual do Cervello.
- Leitura de formatos “ramal nome e-mail” e “nome ramal e-mail”.
- Colagem manual do texto do chamado.
- Edição de e-mails não encontrados.
- Seleção de uma, várias ou todas as pessoas.
- Tema claro e escuro.
- Mensagem institucional padrão e modelos personalizados.
- Edição de assunto e mensagem.
- Variáveis `{{nome}}` e `{{ramal}}` no modo individual.
- Registro dos nomes dos anexos para conferência manual.
- Revisão final.
- Modo individual, recomendado, com um e-mail por usuário.
- Modo CCO para mensagem única sem expor os destinatários.
- Histórico armazenado localmente no Edge.

Uso:
1. Abra um chamado no Cervello.
2. Clique no ícone da extensão.
3. Clique em Capturar e preparar. A extensão lê a descrição, salva o texto e abre o painel automaticamente.
4. Revise nomes, ramais e e-mails no painel.
5. Selecione os destinatários.
6. Escolha o método, edite a mensagem e revise os anexos.
7. Clique em Preparar no cliente de e-mail.

Limitações:
- A extensão prepara o e-mail por mailto, e não envia automaticamente.
- O envio depende do cliente de e-mail padrão do Windows.
- Por segurança do navegador, anexos locais não são adicionados automaticamente por mailto. A tela lista os arquivos que devem ser anexados manualmente.
- No modo individual, a extensão abre um destinatário por vez para evitar várias janelas simultâneas.
- Dados e histórico ficam no armazenamento local do perfil do Edge.
- A empresa pode bloquear o modo do desenvolvedor por política.

Segurança:
A extensão não solicita senha, não armazena credenciais e não contém segredo de aplicação. Para envio automático com anexos seria necessário um backend autorizado ou integração corporativa.

=======================================================================================================================================================

Versão 1.1
- Popup redesenhado com identidade visual própria.
- Exibição do número do chamado detectado.
- Captura executada diretamente pela API de scripting do Edge.
- O botão principal copia o texto do chamado e abre o painel de preparação automaticamente.


Versão 1.2
- Remoção do espaço e da borda excedente do popup.
- Leitura reforçada para o formato RAMAL NOME E-MAIL usado pelo Cervello.
- Fallback de leitura do texto completo da página.
- Captura salva o texto e abre o painel automaticamente.


Versão 1.3
- Removida a faixa/borda excedente do lado direito do popup.
- Largura do documento e do corpo do popup fixadas no mesmo valor.
- Rolagem horizontal e sombras externas do popup desativadas.


Versão 1.4
- Cabeçalho do painel simplificado, sem o subtítulo “Comunicação pós-migração”.
- Nova apresentação visual do título e identificação de extensão local.
- Seção de importação reorganizada com hierarquia visual mais clara.
- Caixa de texto aumentada para 350 px e com redimensionamento vertical.
- Informações de privacidade e orientação adicionadas ao editor.


Versão 1.5
- Preferências movidas para uma página exclusiva.
- Configuração de nome, cargo, letra do turno e tema padrão.
- Nome e cargo do usuário exibidos na navbar do painel.
- Botão Histórico substituído por Relatório no popup.
- Nova página de relatório diário com chamado, ramal, nome, e-mail e método.
- Opções para copiar, imprimir, salvar em PDF e limpar o relatório do dia.


Versão 1.6
- Exemplos alterados para Mario Candido e Analista.
- JavaScript do painel refeito e validado.
- Tema, identificação, revisão, mensagens prontas e anexos corrigidos.
- Botões e carregamento do relatório corrigidos.
- Fundo claro e escuro aplicado à página inteira.


Versão 1.7
- Cores de “Mailer” e do número do chamado restauradas no popup.
- Atalhos para Relatório e Preferências adicionados ao final do painel.
- Leitura reforçada para considerar prioritariamente a seção final de migração.
- Dados cadastrais do solicitante são ignorados quando existe um bloco de ramais a migrar.
- O solicitante só entra na seleção quando também aparece explicitamente no bloco final de migração.


Versão 1.9
- Adicionada a remoção de mensagens prontas personalizadas.
- O modelo institucional padrão continua protegido.
- Ao remover o modelo em uso, a aplicação retorna ao modelo padrão.
