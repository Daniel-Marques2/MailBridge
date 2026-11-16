# MailBridge

> **Da informação à comunicação, com menos trabalho manual.**

O **MailBridge** é uma extensão local para Microsoft Edge criada para agilizar a preparação de mensagens para múltiplos destinatários.

A extensão captura informações disponíveis em chamados e planilhas, identifica nomes, ramais e endereços de e-mail e organiza os dados em um painel de revisão. A partir dele, o usuário pode corrigir informações, selecionar destinatários, personalizar mensagens e preparar comunicações individuais ou em CCO.

Todo o processamento acontece localmente no navegador, sem armazenamento de senhas ou credenciais corporativas.

---

## Funcionalidades

### Captura de dados

- Captura informações diretamente da página aberta no navegador.
- Reconhece dados em chamados e planilhas.
- Identifica nomes, ramais e endereços de e-mail.
- Reconhece colunas em diferentes ordens quando existem cabeçalhos compatíveis.
- Permite colar manualmente o conteúdo de uma solicitação.
- Possibilita revisar o texto antes da identificação.
- Registra o chamado ou o nome da planilha como origem dos dados.
- Permite usar uma seleção copiada da planilha como alternativa de captura.

### Organização dos destinatários

- Seleção individual, múltipla ou total.
- Cadastro manual de destinatários.
- Edição de nome, ramal e e-mail.
- Exclusão de registros incorretos.
- Busca por nome, ramal ou endereço de e-mail.
- Identificação de registros incompletos.
- Validação básica de e-mails e ramais.
- Prevenção de registros duplicados.

### Formatação dos ramais

O formato do ramal pode ser definido diretamente no painel para cada operação.

#### Somente ramal

```text
7074
```

#### 98 + DDD + ramal

```text
98117074
```

O DDD é informado no momento da identificação, permitindo trabalhar com dados de localidades diferentes sem alterar uma configuração global.

### Preparação de mensagens

- Edição do assunto e do conteúdo.
- Mensagem institucional padrão.
- Criação de modelos personalizados.
- Acesso rápido às mensagens prontas.
- Remoção de modelos personalizados.
- Proteção do modelo padrão contra exclusão.
- Personalização por meio das variáveis:

```text
{{nome}}
{{ramal}}
```

No modo individual, as variáveis são substituídas automaticamente pelos dados de cada destinatário.

### Material por link

Nas Preferências, é possível configurar um material hospedado no OneDrive ou SharePoint:

- Nome do material;
- Link de acesso;
- Inclusão automática na mensagem;
- Validação básica do endereço configurado.

Quando a opção estiver ativada, o link será acrescentado automaticamente ao corpo de cada mensagem.

### Métodos de preparação

#### Individual

Prepara uma mensagem separada para cada destinatário.

Esse método é recomendado para comunicações personalizadas e para situações em que os destinatários não devem visualizar os endereços das outras pessoas.

#### CCO

Prepara uma única mensagem com os destinatários em cópia oculta.

Esse método é indicado para comunicados genéricos que não exigem personalização individual.

### Abertura em lotes

No modo individual, o usuário pode escolher quantas mensagens serão abertas por vez.

```text
E-mails por lote
[ 10 ]
```

Controles disponíveis:

- Mínimo de 1 mensagem por lote;
- Máximo de 15 mensagens por lote;
- Validação automática da quantidade;
- Pequeno intervalo entre as aberturas;
- Exibição do progresso;
- Possibilidade de interromper o lote;
- Preservação dos destinatários restantes;
- Processamento somente de registros válidos, selecionados e ainda não processados.

### Revisão final

Antes de abrir as mensagens, o MailBridge apresenta:

- Método selecionado;
- Quantidade total de destinatários;
- Quantidade do lote atual;
- Quantidade restante;
- Lista de destinatários;
- Assunto;
- Conteúdo da mensagem;
- Material configurado.

O usuário pode retornar ao painel e editar qualquer informação antes de continuar.

### Relatório diário

O MailBridge mantém um relatório local dos registros processados no dia, contendo:

- Horário;
- Origem dos dados;
- Nome;
- Ramal;
- E-mail;
- Método de preparação.

A página de relatório também permite:

- Pesquisar registros;
- Copiar o relatório;
- Imprimir;
- Salvar como PDF;
- Limpar os registros do dia.

### Preferências locais

O usuário pode configurar:

- Nome;
- Cargo;
- Letra do turno;
- Tema padrão;
- Endereço usado no campo **Para** no modo CCO;
- Domínio corporativo;
- Material compartilhado.

As configurações ficam armazenadas no perfil local do Microsoft Edge.

### Aparência

- Tema claro e escuro;
- Identidade visual própria;
- Interface responsiva;
- Popup para captura rápida;
- Painel de preparação;
- Páginas separadas para Preferências e Relatório;
- Ícones internos e externos adaptados ao contexto de exibição.

---

## Fluxo de uso

1. Abra no navegador o chamado ou a planilha que contém os destinatários.
2. Clique no ícone do MailBridge.
3. Clique em **Capturar e preparar**.
4. Revise os registros identificados no painel.
5. Corrija ou complete nomes, ramais e e-mails, se necessário.
6. Adicione destinatários manualmente, quando necessário.
7. Escolha o formato do ramal e informe o DDD da operação.
8. Selecione os destinatários.
9. Escolha entre o método individual ou CCO.
10. Defina a quantidade de mensagens por lote.
11. Escolha uma mensagem pronta ou edite o conteúdo.
12. Revise as informações.
13. Abra as mensagens no cliente de e-mail configurado.

---

## Captura de planilhas

Para obter melhores resultados, utilize planilhas com cabeçalhos claros:

```text
Nome
Ramal
E-mail
```

A planilha também pode conter outras colunas:

```text
Número completo
Localidade
Matrícula
Empresa
Ação
```

O MailBridge tenta separar essas informações e utilizar somente os dados necessários para formar os destinatários.

### Captura por seleção

Se a captura automática não localizar corretamente as células:

1. Selecione na planilha as linhas com os dados.
2. Pressione `Ctrl + C`.
3. Abra o MailBridge.
4. Clique em **Capturar e preparar**.

O conteúdo copiado será usado como alternativa de leitura.

---

## Instalação

1. Acesse a seção **Releases** deste repositório.
2. Baixe a versão desejada do MailBridge.
3. Extraia o arquivo ZIP para uma pasta permanente.
4. Abra o Microsoft Edge.
5. Acesse:

```text
edge://extensions
```

6. Ative o **Modo do desenvolvedor**.
7. Clique em **Carregar sem compactação**.
8. Selecione a pasta `mailBridge`, que contém o arquivo `manifest.json`.
9. Fixe o ícone da extensão na barra do navegador.

### Atualização

Para instalar uma nova versão:

1. Remova ou desative a versão anterior.
2. Extraia o novo arquivo ZIP em uma pasta diferente.
3. Utilize novamente a opção **Carregar sem compactação**.
4. Confirme o número da versão em `edge://extensions`.

---

## Privacidade dos destinatários

No modo individual, cada pessoa recebe uma mensagem separada. Dessa forma, os destinatários não visualizam os endereços das demais pessoas.

No modo CCO, os destinatários ficam ocultos em uma única mensagem, mas o conteúdo não possui a mesma personalização individual.

---

## Armazenamento local

O MailBridge pode armazenar localmente:

- Preferências do usuário;
- Tema selecionado;
- Mensagens prontas;
- Material configurado;
- Registros processados;
- Relatório diário.

Os dados ficam no armazenamento local do perfil do Microsoft Edge e não são enviados para um servidor externo pelo MailBridge.

A remoção da extensão ou a limpeza dos dados do navegador pode apagar essas informações.

---

## Limitações atuais

- O MailBridge prepara as mensagens, mas não confirma o envio ou a entrega.
- O funcionamento depende do cliente de e-mail padrão configurado no sistema.
- A maneira como as mensagens são abertas pode variar entre diferentes versões do Outlook e outros clientes de e-mail.
- Arquivos locais não podem ser anexados automaticamente pelo protocolo `mailto:`.
- Para materiais recorrentes, recomenda-se usar um link corporativo do OneDrive ou SharePoint.
- A captura de planilhas depende das informações disponibilizadas pela página ao navegador.
- Algumas planilhas podem exigir a seleção das células e o uso de `Ctrl + C`.
- A instalação pelo modo do desenvolvedor pode ser bloqueada por políticas corporativas.
- O relatório registra que a mensagem foi aberta para preparação, não que ela foi efetivamente enviada.

---

## Segurança

O MailBridge funciona localmente e não armazena:

- Senhas;
- Tokens de acesso;
- Segredos de aplicação;
- Credenciais corporativas;
- Credenciais do Microsoft 365.

Para realizar envios automáticos, anexar arquivos diretamente ou confirmar a entrega das mensagens, seria necessária uma integração corporativa autorizada, como um backend interno ou uma aplicação registrada no Microsoft Entra ID.

---

## Boas práticas

- Revise os destinatários antes de preparar as mensagens.
- Confira os registros capturados de planilhas sem cabeçalhos.
- Utilize o modo individual para mensagens personalizadas.
- Mantenha os lotes em uma quantidade adequada ao cliente de e-mail.
- Utilize links do SharePoint ou OneDrive com permissão somente de visualização.
- Prefira arquivos pertencentes à equipe ou à organização.
- Verifique as políticas internas antes de instalar ou distribuir a extensão.

---

## Histórico de alterações

As novidades, correções e arquivos de cada versão estão disponíveis na seção **Releases** deste repositório.
