# Guia do usuário do Telenota

<!-- docs-toc:start -->
Sumário

- [1. Objetivo e recursos](#purpose)
- [2. Conceitos principais](#concepts)
- [3. Primeiros passos](#start)
- [4. Comandos e navegação](#commands)
- [5. Capturar e salvar](#capture)
- [6. Consultar e buscar](#find)
- [7. Gerenciar notas e tarefas](#items)
- [8. Configurar lembretes](#reminders)
- [9. Exportar para o calendário](#calendar)
- [10. Compartilhar e atribuir](#sharing)
- [11. Mesclar itens](#merge)
- [12. Comentários e conclusão](#comments)
- [13. Tags e itens fixados](#tags)
- [14. Pontos e IA](#points)
- [15. Configurações](#settings)
- [16. Privacidade, limites e ajuda](#help)
- [17. Histórico de alterações](#history)
<!-- docs-toc:end -->

<a name="purpose"></a>

## 1. Objetivo e recursos

O Telenota transforma mensagens, ideias e anexos do Telegram em notas e tarefas organizadas para você encontrar e usar depois. Tudo acontece na conversa com o bot, sem outro aplicativo de notas.

- Capture texto, encaminhamentos, links, voz, vídeos, imagens e documentos compatíveis.
- Revise rascunhos, salve notas ou tarefas, adicione comentários e organize com tags.
- Busque informações, programe lembretes, exporte eventos e compartilhe ou atribua itens.
- Escolha análise com IA, tradução ou voz gerada quando precisar. Essas ações podem consumir pontos; a captura e o salvamento manual continuam disponíveis sem IA.


<a name="concepts"></a>

## 2. Conceitos principais

**Nota**: informação salva que você deseja manter.

**Tarefa**: item salvo que pode ser concluído, atribuído ou agendado.

**Item**: uma nota ou tarefa que você salvou explicitamente. Salvar não compartilha o conteúdo com outras pessoas.

**Rascunho**: conteúdo capturado aguardando um salvamento explícito; ainda não é um item publicado.

**Lembrete**: tarefa com data e hora; não é uma exportação de calendário.

**Tag/tema**: marcador para organizar e encontrar itens.

**Comentário**: texto ou mídia adicionado a um item.

**Arquivo**: itens mantidos fora das listas ativas; arquivar é diferente de excluir.

<a name="start"></a>

## 3. Primeiros passos

1. Abra a conversa com o bot e envie `/start`.
2. Em Configurações, na tela Início, confira idioma e fuso horário.
3. Envie um texto curto ou encaminhe uma mensagem e revise o rascunho.
4. Salve como nota ou tarefa. Escolha uma ação de IA apenas se quiser uma análise paga.
5. Use os atalhos da confirmação para abrir o item ou a lista. Configure um lembrete quando necessário.

As boas-vindas guiadas concedem 10 pontos em três ações úteis: +2, +3 e +5. Os 10 pontos não são pagos de uma vez no primeiro acesso. Os botões do rascunho permanecem até você agir.

<a name="commands"></a>

## 4. Comandos e navegação

- `/start` — Abrir Início e recarregar preferências
- `/find` — Buscar notas e tarefas
- `/notes` — Abrir Notas
- `/tasks` — Abrir Tarefas
- `/drafts` — Abrir Rascunhos
- `/reminders` — Abrir Lembretes
- `/more` — Abrir Mais, com Ajuda e informações legais
- `/settings` — Abrir Configurações
- `/back` — Voltar à tela anterior

O menu de comandos reúne os atalhos principais; Configurações também fica em Início. Mais → Ajuda abre este guia no seu idioma. A busca permanece ativa até você sair. O texto enviado durante uma busca, um lembrete ou um comentário aberto explicitamente pertence àquela ação. Use Voltar antes de capturar um texto independente.

<a name="capture"></a>

## 5. Capturar e salvar

Os resultados de links na fila usam o idioma de interface salvo no momento do processamento. O título e a descrição públicos da página podem servir de alternativa se a análise falhar; páginas restritas podem continuar indisponíveis. O rascunho aparece sem esperar um título temporário separado de IA.

### Criar uma nota

1. Envie texto simples ao bot.
2. O bot mostra uma prévia do rascunho.
3. Toque em `📝 Salvar como nota`.
4. Use os atalhos da confirmação para abrir o item ou a lista.

### Criar uma tarefa

Opção A:
1. Envie texto.
2. Na prévia do rascunho, toque em `🟧 Salvar como tarefa`.
3. Use os atalhos da confirmação para abrir o item ou a lista.

Opção B:
1. Abra qualquer nota.
2. Toque em `⬛ Criar tarefa`.

### Encaminhar mensagens

1. Encaminhe uma ou mais mensagens para o bot.
2. O bot combina mensagens encaminhadas próximas no tempo em um único rascunho.
   - O tempo de combinação padrão é `30` segundos.
   - Você pode alterá-lo em `Início -> Configurações -> Tempo de combinação de mensagens`.
3. Se você adicionar texto simples logo após encaminhar, o bot o anexa como:
   - `💬 Encaminhado com comentário:`
   - `<seu texto>`
   antes da linha de fonte/rodapé.
4. Na visualização da nota/tarefa, fontes públicas de usuários do Telegram são mostradas como links clicáveis `@handle` em vez de URLs cruas `https://t.me/...`, é mantida exatamente uma linha em branco antes do rodapé final `Salvo via Telenota (...)`, e esse rodapé também inclui um link clicável `sua mensagem` para a mensagem exata do bot da qual o item foi criado quando o Telegram ainda a expõe.
5. Se uma mensagem encaminhada contiver um ou mais links web, o bot primeiro usa os metadados de prévia disponíveis de cada página e, quando eles não existem, tenta um fallback determinístico e seguro de título com base nos metadados da página.
   - Links redirecionados do Google Maps podem ser resolvidos para o título final da página quando a página de destino o expõe.
   - Se nenhum título seguro puder ser extraído, o bot mantém o fallback existente de salvamento com link de origem em vez de mostrar uma fonte falsa ou um erro bruto.
   - Em encaminhamentos combinados, a atualização em segundo plano do resumo do link substitui apenas o bloco de link pendente e mantém as outras mensagens encaminhadas.
6. A formatação do Telegram no texto encaminhado é preservada em notas/tarefas salvas quando o Telegram a expõe ao bot:
   - negrito, itálico estilo Markdown, links e blocos de citação são renderizados na visualização final do item.
   - links mantêm a URL de destino completa, incluindo parâmetros de consulta como `?g_st=...` ou `&foo=...`.
7. Se nenhum comentário separado for adicionado depois do encaminhamento, o bot salva o marcador explícito `Encaminhado sem comentários`; se um comentário for enviado logo após o encaminhamento, apenas esse comentário é salvo no bloco de comentário.
8. Mídias do Telegram anexadas à mensagem encaminhada são salvas com o rascunho e mostradas com a nota/tarefa salva. Se vários anexos tiverem um link de fonte salvo, a visualização do item os mostra como links compactos separados por vírgula e agrupados por tipo de mídia:
   - fotos/imagens permanecem anexadas quando o Telegram as fornece como mídia baixável pelo bot.
   - imagens de prévia de link geradas apenas por clientes Telegram podem não ser baixáveis pela Bot API; envie/encaminhe a foto real se precisar de retenção garantida da imagem.
   - se o Telegram expuser um vídeo ou uma animação encaminhados junto com uma foto de prévia do cliente, o bot mantém o vídeo ou a animação reais e suprime a imagem de prévia duplicada.
   - se o Telegram informar apenas um arquivo de mídia encaminhado grande demais durante o salvamento com IA, o bot salva o rascunho original sem análise de mídia por IA em vez de mostrar erro genérico.
9. Opcional: envie texto apenas com hashtags (exemplo: `#work #idea`) antes de salvar para adicionar tags.
10. Abra o rascunho e use:
   - linha 1: `📝 Salvar como nota`, `🟧 Salvar como tarefa`
   - linha adicional opcional: `⏰ Salvar como lembrete` aparece quando o texto do rascunho contém uma data/hora reconhecível
   - ações finais: `✏️ Editar`, `❌ Cancelar`
   - as ações com IA aparecem sempre, inclusive em rascunhos de texto puro; para imagens, o item mantém primeiro o conteúdo original e depois mostra o resumo de IA e o texto OCR, preservando listas numeradas e com marcadores legíveis
   - o resumo com IA é formatado em três partes curtas: introdução, parte principal e conclusão
   - `Editar` mostra apenas o texto limpo do item para cópia manual; fonte, tipo localizado do item e rodapé do bot continuam no modelo
11. Depois de tocar em salvar, o bot mostra imediatamente um status de salvamento e depois uma mensagem de sucesso com quatro atalhos inline: abrir o item criado e Notas na primeira linha, e depois Início e Rascunhos na segunda linha.
12. Se todos os rascunhos forem consumidos/salvos, abrir `Rascunhos` leva você de volta ao seletor Início.

Novos rascunhos recebem um título conciso gerado por IA no idioma de interface selecionado. A análise de vídeo por IA descreve primeiro a imagem, incluindo datas legíveis, e adiciona a transcrição de áudio quando disponível.

### Voz e vídeo

1. Envie uma mensagem de voz, arquivo de áudio (incluindo `.m4a` quando o Telegram o envia como áudio ou documento de áudio), vídeo ou nota de vídeo.
2. O bot mostra imediatamente uma mensagem de processamento quando a análise de áudio/vídeo começa.
3. O bot transcreve e prepara um rascunho. Transcrições de áudio/vídeo incluem timestamps no final de cada parágrafo quando dados de tempo estão disponíveis.
   - Se a transcrição falhar, o bot mostra `Tentar novamente`; toque para tentar de novo com o mesmo arquivo do Telegram sem reenviá-lo.
4. Quando a análise com IA é executada, o bot transcreve o arquivo e prepara o texto do rascunho ou item.
   - Depois de salvar, o bot mostra uma mensagem de sucesso com quatro atalhos inline: abrir o item criado e a lista correspondente na primeira linha, e depois Início e Rascunhos na segunda linha.
5. Se o rascunho contiver uma data/hora reconhecível, você pode tocar em `⏰ Salvar como lembrete`.
   - Isso salva o rascunho como tarefa e agenda o lembrete imediatamente.
6. Se um rascunho combinar várias mensagens encaminhadas/com legenda ou análise de mídia por IA, a nota/tarefa salva separa as seções com divisores horizontais visíveis. A formatação do texto original e do conteúdo gerado é preservada quando o Telegram a expõe ao bot.
7. Mensagens de voz, arquivos de áudio e vídeos do Telegram maiores que `20 MB` são rejeitados antes do processamento porque a Telegram Bot API não permite que este bot baixe arquivos maiores neste runtime.
8. Se sua gravação ou vídeo tiver mais de `20 MB`, divida ou comprima manualmente e envie as partes menores uma por uma.
9. Mensagens de erro temporárias são removidas automaticamente quando você envia a próxima mensagem, toca no próximo botão do bot ou após 30 segundos.
10. Falhas recuperáveis do Telegram, da IA ou por tempo esgotado mostram um código estável, como `E-TIMEOUT-001`. Encaminhe essa mensagem para `@telenota_chat` ao pedir ajuda; o código não expõe seu conteúdo.

O reconhecimento de fala usa GPT-Transcribe. A configuração atual não fornece marcações de tempo por parágrafo nem identifica pessoas pela voz. A formatação pode preservar turnos de diálogo sustentados pelo conteúdo, mas não determina quem falou a partir do áudio. Os títulos são gratuitos e uma análise conjunta pode ser reutilizada no resumo, no título e nos metadados.

Antes da análise de vídeo em várias etapas, o bot reserva o custo total. Se não puder entregar o resultado completo, devolve a reserva; se não houver áudio utilizável, devolve o valor da transcrição não utilizada. A análise visual ainda pode funcionar. Outros anexos ou etapas compatíveis podem ter cobranças separadas.

### Imagens e capturas de tela

1. Envie ou encaminhe uma imagem/captura de tela.
2. O bot executa OCR e resume o texto/conteúdo visível importante.
3. Um rascunho é criado; depois salve como nota ou tarefa.
4. Se você enviar um documento PDF com texto e escolher uma ação de salvamento com IA, o bot mantém o conteúdo original do rascunho, adiciona o texto extraído do PDF e depois acrescenta um breve resumo com IA de até `300` palavras no idioma de interface selecionado.
5. O texto extraído é mantido em parágrafos legíveis, e o resumo com IA é renderizado em três partes curtas: introdução, parte principal e conclusão.
6. PDFs digitalizados ou compostos apenas por imagens podem falhar na análise com IA até que exista suporte de OCR para PDF.
7. Se você salvar um PDF sem IA, o rascunho/elemento mantém uma linha simples `PDF <nome do arquivo>`. Se depois abrir o elemento salvo e tocar em `Análise com IA`, o mesmo fluxo de resumo do PDF será executado ali também.
8. A Telegram Bot API não fornece aos bots o arquivo de mídia de um Story encaminhado. O bot salva a referência e pede que você envie em seguida uma captura de tela, foto ou vídeo baixado; esse arquivo é anexado ao mesmo rascunho.
9. Na análise com IA de uma imagem, o item salvo mostra primeiro o resumo de IA e depois o texto OCR reconhecido. Listas numeradas e com marcadores da imagem mantêm o formato.

### Início guiado e rascunhos com IA

- As ações de nota e tarefa com IA analisam em conjunto o texto original disponível e os anexos compatíveis. Títulos de rascunhos e resumos usam o idioma da interface. Confira o resultado.
- Quando houver um seletor de tradução, vermelho mantém o idioma original e verde traduz para o idioma da interface ao salvar uma nota ou tarefa comum.
- Se um item ocupar várias mensagens do Telegram, os botões ficam na última.

<a name="find"></a>

## 6. Consultar e buscar

A busca local dá mais peso a palavras distintas e ignora palavras gramaticais comuns. Essa ordenação não chama a IA nem gera cobrança adicional.

### Navegar por notas e tarefas

- Use o menu de comandos do Telegram (hambúrguer):
  - `🏠 Início`
  - `🔎 Buscar`
  - `📝 Notas`
  - `🗂️ Rascunhos`
  - `🟧 Tarefas`
  - `⏰ Lembretes`
  - `📚 Mais`
- Se o menu inferior estiver ativado (`Início -> Configurações -> Mostrar menu inferior`):
  - linha 1: `📝 Notas` + nova linha + `(N)`, `⏰ Lembretes` + nova linha + `(N)`, `🟧 Tarefas` + nova linha + `(N)`
  - linha 2: `🗂️ Rascunhos` + nova linha + `(N)`, `🔎 Buscar`, `📚 Mais`
- Cabeçalhos de listas como `📝 Notas` e `🗂️ Rascunhos` são exibidos em uma única linha visível, sem espaçamento invisível.
- Quando você abre uma tarefa da página 2+ e depois a marca como concluída, exclui, converte ou define um lembrete, o bot volta para a mesma página da lista de tarefas ao mostrar a lista novamente.
  - quando ativado, o menu inferior permanece visível até que o usuário o desative nas configurações
  - esses botões abrem as mesmas telas que as ações do menu hambúrguer.
- Ou use os contadores inline na tela inicial:
  - linha 1: `📝 Notas (N)`, `🟧 Tarefas (N)`
  - linha 2: `🗂️ Rascunhos (N)`, `⏰ Lembretes (N)`
  - linha 3: `🔎 Buscar`, `⚙️ Configurações`
  - linha 4: `⬅️ Voltar`, `📚 Mais`

### Buscar (busca combinada + Recall)

1. Abra Buscar pela tela inicial ou envie `/find` e digite uma consulta.
2. A busca local, as variações de palavras, a navegação e a paginação são gratuitas. Itens arquivados podem aparecer; um número exato como `219` ou `#219` coloca o item em primeiro lugar, se ele existir.
3. Abra um resultado ou escolha **Responder com IA** para pedir uma resposta contextual por **5 pontos**. O botão não mostra o preço. Digitar uma consulta não solicita uma resposta paga.
4. A mesma resposta é reutilizada sem nova cobrança na sessão de busca se nada mudou; paginar e voltar aos resultados não chama a IA. Alterar consulta, contexto, idioma ou modelo pode exigir outra resposta.
5. Se a resposta falhar ou o saldo for insuficiente, os resultados locais continuam disponíveis e você pode tentar novamente de forma explícita. Voltar sai da busca e retorna à tela anterior.

<a name="items"></a>

## 7. Gerenciar notas e tarefas

### Ações de nota
- `✏️ Editar`
- `⬛ Transformar em tarefa`
- `❌ Remover`
- `📚 Mais`
- `⬅️ Voltar`
- `📚 Mais` abre:
  - linha 1: `🤖 Analisar com IA`, `🔊 Criar voz`
  - linha 2: `🔀 Mesclar`, `📤 Compartilhar`
  - linha 3: `📌 Fixar` / `📌 Desafixar`, `🏷️ Tags`
  - linha 4: `⬅️ Voltar`

### Ações de tarefa
- `✏️ Editar`
- `✅ Concluída` ou `🔄 Refazer`
- `⏰ Lembrete`
- `🔁 Criar nota`
- `❌ Remover`
- `📚 Mais`
- `⬅️ Voltar`
- `📚 Mais` abre:
  - linha 1: `🤖 Analisar com IA`, `🔊 Criar voz`
  - linha 2: `🔀 Mesclar`, `👥 Atribuir` ou `👥 Reatribuir`
  - linha 3: `📌 Fixar` / `📌 Desafixar`, `🏷️ Tags`
  - linha 4: `⬅️ Voltar`

### Criar voz (texto para fala)
1. Abra qualquer nota ou tarefa.
2. Toque em `🔊 Criar voz`.
3. O bot mostra imediatamente uma notificação do sistema informando que a geração de texto para voz começou.
4. O bot gera uma mensagem de voz usando OpenAI (voz `onyx`), envia ao chat e anexa ao item.

A leitura em voz alta mantém os links do autor e da fonte, inclusive ao converter uma nota em tarefa ou vice-versa. Links sem esquema, como Tambur.pub, abrem por HTTPS em vez de aparecerem como Markdown.

A duração do áudio gerado é medida e mantida ao reabrir o registro. Repetir a leitura do mesmo texto com a mesma voz e modelo reutiliza o arquivo salvo, sem nova cobrança de geração por IA nem anexo duplicado. Alterar o texto lido cria uma nova versão. Arquivos de áudio antigos de origem desconhecida não são excluídos automaticamente.

### Mídia para texto
1. Abra qualquer nota ou tarefa.
2. Abra `📚 Mais`.
3. Toque em `🤖 Analisar com IA`.
4. O mesmo botão agora também funciona para itens de texto normais e imagens anexadas, não apenas para áudio/vídeo/PDF.
5. O bot calcula o custo de acordo com o caminho real da análise:
   - enriquecimento de texto/links com IA usa a tarifa de análise de texto
   - imagens salvas usam a tarifa de análise de imagem
   - A duração é medida no arquivo real com ffprobe antes da reserva de pontos, sem estimativa por tamanho ou duração fictícia.
6. Se seu saldo for suficiente, o bot reserva os pontos necessários, executa a análise com IA, atualiza o item e só finaliza a cobrança após um processamento bem-sucedido.
   - A configuração atual não inclui marcações de tempo por parágrafo; algumas configurações antigas podem fornecê-las.
7. Se a análise com IA falhar, os pontos reservados são liberados e o item permanece inalterado.

### Editar uma nota

1. Abra nota/tarefa.
2. Toque em `✏️ Editar`.
3. Siga o prompt e envie o texto completo atualizado.
4. O bot salva a edição e adiciona timestamp de `última edição` no rodapé.

### Remover ou arquivar

1. Abra nota/tarefa.
2. Toque em `❌ Remover`.
3. Escolha:
   - `🗑️ Excluir`
   - `🗄️ Arquivar`
   - `⬅️ Voltar`
4. Se escolher `🗄️ Arquivar`, o bot pede um comentário opcional de arquivamento.
5. Envie o comentário ou toque em `✅ Sem comentários`.
6. O bot anexa a linha `Comentário de arquivamento: <comment>` ao final do item e depois o arquiva.
7. Se a nota/tarefa tinha anexos de mídia exibidos no chat, essas mensagens de anexos são removidas da tela após excluir/arquivar.

A sugestão de pessoas mencionadas tem uma só ação de retorno: Abrir item. Mencionar alguém nunca compartilha nem atribui automaticamente.

<a name="reminders"></a>

## 8. Configurar lembretes

Abra uma tarefa, escolha Lembrete e informe data e hora no fuso salvo. Datas futuras reconhecidas em novas tarefas também podem ser agendadas ao salvar. Uma data sem hora usa o horário do resumo diário de tarefas; se não houver horário configurado, informe um explicitamente.

Uma sugestão em uma nota não a transforma sozinha em tarefa: aceite o lembrete para converter e agendar. Uma hora sem data corresponde a hoje, a menos que você indique outra data. Confira a confirmação. Itens antigos não são reagendados automaticamente.

Concluir uma tarefa cancela seus lembretes agendados. Um lembrete só com data usa o horário do resumo; uma exportação de calendário só com data cria um evento de dia inteiro.

<a name="calendar"></a>

## 9. Exportar para o calendário

O link do Google abre um formulário: confira os dados e salve o evento. ICS continua disponível, e a nova entrada do Google não cobra novamente por uma exportação sem alterações. Não há criação automática nem nova conexão OAuth.

A exportação para o calendário aparece no registro quando uma data ou horário é detectado e fica sempre disponível em Mais. O nome do botão não mostra o preço; a exportação custa 0,10 ponto. Ao tocar, você recebe diretamente um arquivo de evento .ics, sem prévia intermediária no bot, e um link alternativo do Google Agenda. Abra o arquivo no calendário e confirme a importação; o Telegram ou o sistema pode pedir que você escolha um aplicativo. A abertura automática do calendário padrão não é garantida no iOS, Android ou computador.

Se o Telegram não confirmar o envio do ICS, o bot envia uma mensagem separada com o link preenchido do Google Agenda. A confirmação é um ID de mensagem e de arquivo retornado pelo Telegram, não o download ou a importação no dispositivo. O link não exige conectar o bot via OAuth.

Somente uma data cria um evento de dia inteiro; somente um horário usa o dia de hoje no fuso salvo, mesmo se o horário já passou. Data e horário usam o momento indicado. A duração padrão é de 60 minutos. O título começa com o ícone de nota/tarefa e usa o título do registro; a descrição contém um link para o registro no bot, sem o texto privado. Se a data estiver ausente, inválida ou ambígua, Mais pede uma única data/horário de início; Voltar cancela, e anexos ou encaminhamentos criam um novo rascunho.

Uma única entrega bem-sucedida do mesmo evento é cobrada por usuário. Obter novamente é grátis, inclusive após reiniciar o bot; falhas no envio são reembolsadas. Alterar título, data ou horário gera outro evento. O bot não confirma o salvamento no calendário. Reimportar pode duplicar eventos; alterações futuras não são sincronizadas. O arquivo some do chat ao fechar os anexos do registro. Não é necessário conectar uma conta de calendário nem usar análise de IA paga.

<a name="sharing"></a>

## 10. Compartilhar e atribuir

### Atribuição de tarefas com Contatos
1. Abra uma tarefa.
2. Toque em `👥 Atribuir` ou `👥 Reatribuir`.
3. O bot mostra:
   - seus contatos salvos como botões
   - opção de entrada manual (`@handle` ou telefone)
4. Se você digitar um novo `@handle`/telefone válido, ele será salvo automaticamente em seus Contatos.
5. Se o destinatário já iniciou o bot, a atribuição é enviada e a tarefa é vinculada a esse usuário.
6. Se o destinatário ainda não iniciou o bot e você selecionou um `@handle`, o bot cria uma mensagem de convite separada com o link escondido sob “Telenota”. Envie essa mensagem ao destinatário: quando ele iniciar o bot com esse link, a tarefa será entregue automaticamente se o handle do Telegram coincidir. Se outra conta abrir o link, o bot pedirá que você aprove ou recuse o acesso.
7. Você pode usar `↩️ Remover atribuição` no seletor de atribuição para remover a atribuição atual.

### Compartilhamento de notas com Contatos
1. Abra uma nota normal.
2. Toque em `📤 Compartilhar`.
3. O bot mostra:
   - seus contatos salvos como botões
   - opção de entrada manual (`@handle` ou telefone)
4. Se você digitar um novo `@handle`/telefone válido, ele será salvo automaticamente em seus Contatos.
5. Se o destinatário já iniciou o bot, a nota é compartilhada e entregue no chat dele, incluindo anexos.
6. Se o destinatário ainda não iniciou o bot e você selecionou um `@handle`, o bot cria uma mensagem de convite separada com o link escondido sob “Telenota”. Envie essa mensagem ao destinatário: quando ele iniciar o bot com esse link, a nota será entregue automaticamente se o handle do Telegram coincidir. Se outra conta abrir o link, o bot pedirá que você aprove ou recuse o acesso.

### Compartilhamento público e links de origem

- `Mais -> Compartilhar` agora funciona tanto para notas quanto para tarefas.
- No seletor de compartilhamento, você pode escolher um contato salvo ou tocar em `Compartilhar publicamente` para criar uma mensagem encaminhável com o link de início do bot.
- Itens longos em `Compartilhar publicamente` são divididos automaticamente em várias mensagens encaminháveis; cada mensagem termina com o rodapé normal `Salvo via Telenota (<data e hora locais>)`.
- Se alguém iniciar o bot pela primeira vez pelo seu link de convite ou pelo seu link privado de compartilhamento, você receberá uma notificação persistente do bot informando que essa pessoa entrou.
- Quando o Telegram fornece metadados suficientes, `Origem` abre a mensagem original exata do Telegram.
- Rascunhos, notas e tarefas mostram a data e a hora de salvamento no seu fuso horário.

### Gerenciar contatos

O gerenciamento de contatos está disponível em `Mais -> Contatos`:
- ver todos os contatos salvos para atribuições
- `➕ Adicionar contato` (digitar `@handle` ou telefone)
- `📱 Compartilhar meu telefone` (compartilhar seu próprio contato do Telegram com o bot)
- abrir contato -> `Editar` / `Excluir`
- editar atualiza o valor do contato usado nas sugestões de atribuição

<a name="merge"></a>

## 11. Mesclar itens

1. Abra um item e escolha Mais → Mesclar.
2. Escolha um destino sugerido ou digite o número. Os candidatos são seus itens ativos do mesmo tipo; tags em comum têm prioridade sobre a relevância do texto.
3. O destino mantém número e título. O texto completo é acrescentado sem reescrita por IA nem cortes; tags e anexos distintos são preservados.
4. Lembretes diferentes são mantidos sem duplicar o mesmo horário.
5. A origem é arquivada, não excluída. Seus comentários continuam no arquivo original.
6. O destino é aberto e as cópias já atribuídas recebem a atualização correspondente.

<a name="comments"></a>

## 12. Comentários e conclusão

Tarefas concluídas ficam fora da lista ativa de Tarefas e do contador. Se sua configuração de conclusão mantiver o item, o registro continua salvo; sair da lista ativa não significa exclusão.

### Tarefa concluída e comentários

1. Abra a tarefa.
2. Toque em `✅ Concluída`.
3. Digite um comentário opcional ou toque em `✅ Sem comentários`.
4. Todas as mensagens de anexos atualmente exibidas para essa tarefa são removidas do chat enquanto o prompt/lista de conclusão é mostrado; os anexos salvos permanecem no item.
5. O resultado segue suas Configurações:
   - Excluir
   - Arquivar
   - Manter

- Notas e tarefas agora aceitam comentários. Abra um item e toque em `Comentários (N)` para ver os comentários existentes como mensagens separadas do Telegram com botões `Comentar` / `Excluir`.
- Quando o modo de comentário está ativo, o próximo texto/mídia enviado ou encaminhado aparece primeiro como pré-visualização com `Comentar`, `Criar rascunho`, `Voltar` e `Início`; só depois da confirmação ele é salvo abaixo do item como `Comentário N`.

<a name="tags"></a>

## 13. Tags e itens fixados

### Tags

1. Abra uma nota.
2. Toque em `🏷️ Tags`.
3. Toque em uma tag para abrir notas com essa tag.
4. Para adicionar tags, envie mensagem com hashtags (exemplo: `#project #urgent`).
5. Nomes de pessoas detectados no texto da nota são adicionados automaticamente como tags com inicial maiúscula.

### Fixar itens

1. Abra uma nota ou tarefa.
2. Toque em `📚 Mais`.
3. Toque em `📌 Fixar` para manter o item no topo da lista.
4. Toque em `📌 Desafixar` para devolvê-lo à ordem cronológica normal.

<a name="points"></a>

## 14. Pontos e IA

Um dia local com atividade válida rende 0,50 ponto: crie um item ou comentário com mais de 100 caracteres visíveis, ou compartilhe/atribua um item a outra pessoa. Consultar, editar e receber cópias não conta. Os três dias inativos seguintes rendem 0,30, 0,15 e 0,05; a partir do quarto, os bônus param até uma nova atividade válida.

Se já houve um bônus por inatividade, a atividade completa o total do dia até 0,50, sem somar outros 0,50. Não há recuperação de dias perdidos nem recálculo de saldos antigos. Repetir a entrega de um aviso não repete o crédito; após uma interrupção, o mesmo aviso pode aparecer mais de uma vez.

A exportação para o calendário custa `0,10 ponto` pela entrega bem-sucedida do arquivo ou link alternativo, uma vez por usuário e evento sem alterações. Uma falha no ICS seguida da entrega do link Google é uma única operação. Se nenhum for entregue, a reserva é devolvida. Reexportar é grátis, inclusive após reiniciar o bot. O botão não mostra o preço.

1. Ações com IA usam seu saldo de pontos.
2. Modelo de cobrança padrão:
   - `1 ponto = 1 Telegram Star`
   - As boas-vindas guiadas concedem 10 pontos em três ações úteis: +2, +3 e +5. Os 10 pontos não são pagos de uma vez no primeiro acesso.
   - nenhuma recompensa automática de pontos por criar notas/tarefas
   - `1.5 ponto / minuto` para texto em voz
   - `1.0 ponto / minuto` para análise de áudio
   - `1.5 ponto / minuto` para transformar em texto áudio/vídeo já anexado a um item salvo
   - `0.5 ponto` por OCR de imagem
   - Resumo e etiquetas: `0.20 ponto`; tradução: `0.50 ponto`; resumo de áudio, análise de quadros de vídeo e resumo de PDF: `1 ponto` por etapa. Títulos são gratuitos; análise de links: `0.05 ponto`.
3. A duração real do arquivo é medida antes da reserva de pontos; ela não é estimada pelo tamanho do arquivo.
   - Exemplo: `125 segundos` custam `3.13 pontos`.
   - A cobrança é arredondada para cima para o `0.01 ponto` mais próximo.
   - Se não for possível medir a duração, a operação é interrompida sem cobrança.
   - Se seu saldo for insuficiente, a transcrição não começa e sua nota/tarefa existente não é alterada.
4. Abra `Mais -> Pontos` para:
   - ver seu saldo atual
   - ver suas últimas 5 operações de pontos
   - abrir o histórico completo de pontos
   - ver os preços atuais de IA
   - recarregar com Telegram Stars
5. Ao comprar pontos dentro do bot, recargas com Telegram Stars são precificadas diretamente em `XTR`.
6. Se seu saldo for insuficiente:
   - a funcionalidade de IA é bloqueada para essa ação
   - o bot mostra uma notificação
   - funcionalidades sem IA continuam funcionando
7. Ações típicas pagas com IA incluem:
   - resumos e tags
   - geração de respostas Recall/Find
   - tradução
   - interpretação livre de lembretes, fuso horário e horários de digest
   - transcrição e texto em voz

<a name="settings"></a>

## 15. Configurações

**Ocultar mensagens do sistema:** 5, 10 ou 30 segundos, 1 minuto ou Nunca; padrão de 30 segundos. Vale para novos avisos temporários. As ações de rascunhos pendentes continuam disponíveis. A limpeza da navegação e as atualizações técnicas do teclado são independentes.

### Idioma

1. No primeiro `/start`, o bot tenta detectar seu idioma pela localidade do Telegram.
2. O idioma padrão de fallback é inglês.
3. Para alterar o idioma manualmente:
   - abra `Início -> Configurações -> Idioma`
   - escolha um destes idiomas, nesta ordem: `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`, `العربية`
4. Todos os principais rótulos e botões da interface são traduzidos após a seleção.

Abra `⚙️ Configurações` para configurar:
- `🌐 Idioma` (primeiro item)
  - English / Español / Français / Português / Русский / Українська / 简体中文 / العربية
- `🕒 Fuso horário`
  - toque em `Fuso horário`
  - responda com cidade, código de fuso horário ou texto com a hora atual
  - o bot usa OpenAI para inferir e salvar seu fuso horário
  - o fuso salvo é mostrado como `UTC±HH:MM · City`
- `Marcar como concluída`
  - Excluir / Arquivar / Manter
- `Copiar texto para edições`
  - Copiar texto da nota / Não fazer nada
- `🗓️ Digest diário de tarefas`
  - `Definir horário` em texto livre como `todos os dias às 8`, `21:30`, `amanhã 7`
  - salvar um horário também ativa automaticamente o digest diário
  - `Ativar` / `Desativar`
  - em Configurações, o status é mostrado apenas com círculo verde/vermelho
  - o resumo de Configurações mostra o horário local sem sufixo de fuso horário
  - o digest é enviado uma vez por dia no horário local configurado do usuário
  - o digest inclui seções:
    - `Lembretes` ou `Sem lembretes até o próximo digest`
    - `Tarefas`
    - `Notas adicionadas desde o último digest`
  - itens em todas as seções são links; tocar abre a nota/tarefa relacionada no bot
  - a mensagem de digest inclui botões rápidos: `⏰ Lembretes`, `🟧 Tarefas`
  - o status é sincronizado entre o resumo de Configurações e a tela de detalhes do digest
- `🌙 Resumo da noite`
  - `Definir horário` com o mesmo parser de horário livre do digest da manhã
  - salvar um horário também ativa automaticamente o resumo da noite
  - `Ativar` / `Desativar`
  - em Configurações, o status é mostrado apenas com círculo verde/vermelho
  - o resumo de Configurações mostra o horário local sem sufixo de fuso horário
  - o digest da noite inclui:
    - `Tarefas -> Tarefas que concluí hoje`
    - `Tarefas -> Tarefas que criei hoje`
    - `Notas que adicionei hoje`
  - após o digest, o bot pergunta:
    - `E como VOCÊ sente que foi seu dia hoje?`
    - responda a esse prompt específico com texto/voz/vídeo
    - o bot salva sua resposta como nota com a tag `daily`
- `⏱️ Tempo de combinação de mensagens`
  - toque no botão
  - envie um número de segundos, por exemplo `30`, `45`, `120`
  - mensagens enviadas dentro desse intervalo são combinadas em um rascunho
  - se o intervalo for `30` segundos ou mais (com a configuração padrão), um novo rascunho é criado
- `📱 Mostrar menu inferior`
  - o status é mostrado apenas com círculo verde/vermelho
  - padrão: ativado
  - quando ativado, o teclado inferior persistente é mostrado para este usuário
  - quando desativado, o teclado inferior persistente fica oculto para este usuário
  - alterar essa configuração é silencioso, sem mensagens de sistema sobre visibilidade
- `📚 Nº de itens`
  - controla quantos itens são mostrados por página nas telas de lista

<a name="help"></a>

## 16. Privacidade, limites e ajuda

Os erros oferecem Voltar e Início. Se um link falhar, guarde o código para o suporte e volte à navegação; uma página restrita pode continuar indisponível. A demora intermitente nas imagens segue em investigação; as fotos mantêm a apresentação e a qualidade.

`Início -> Configurações` também inclui uma zona de perigo para excluir os dados da sua conta Telenota.

Excluir todos os dados remove permanentemente suas notas, tarefas, rascunhos, lembretes, contatos, configurações, histórico de pontos e registros de conta vinculados pertencentes ao bot.

A IA pode errar: confira resumos, datas e traduções. Recursos de IA enviam o conteúdo pertinente ao provedor. O corpo é criptografado ao ser salvo; títulos, tags e outros metadados não são todos criptografados.

O transporte Telegram utilizado limita downloads a 20 MB por arquivo de mídia. A aceitação pelo Telegram não comprova o fim do download no dispositivo. Atrasos intermitentes de imagens continuam em aberto. Importar eventos não sincroniza calendários e o Google OAuth não está ativado.

Se uma tela travar, tente /start, Voltar e reiniciar o Telegram. Apagar a conversa não é um passo comum de diagnóstico: você pode perder histórico útil. Não publique segredos ou conteúdo privado ao relatar erros.

### Como relatar bem um bug

Ao relatar um bug, inclua:
- botão/ação exata em que você tocou
- data/hora e fuso horário exatos
- captura de tela ou gravação curta da tela
- resposta exata do bot ou que não houve resposta
- se `/start` ainda funciona enquanto outros botões não funcionam

[Suporte e sugestões](https://t.me/telenota_chat) · [Termos de uso](https://raw.githubusercontent.com/panslav/aunotebot_public/main/docs/legal/terms-and-conditions_pt.md)

<a name="history"></a>

## 17. Histórico de alterações

As notas abaixo descrevem versões anteriores. Para o funcionamento atual, siga as instruções acima; alguns comportamentos históricos mudaram.

### 0.25

Nota de manutenção (esclarecimento do limite de áudio v0.25): para áudio enviado pelo Telegram, este bot aplica o limite de download da Telegram Bot API.

### Versão 0.35.0.4

- Os títulos com IA usam o texto disponível, o resumo do link e a análise dos anexos compatíveis. Um rascunho que contém apenas um anexo mantém um título pelo tipo de mídia até ser analisado.
- A análise com IA de um item salvo combina o texto atual com o texto extraído de todos os anexos compatíveis antes de acrescentar o resultado.
- Em encaminhamentos agrupados, cada segmento mostra o autor antes do texto. A sugestão de lembrete desaparece após qualquer ação; `Pular` apenas ignora o lembrete.

### Versão 0.35.0.5

- Num elemento combinado, cada autor aparece antes do texto da sua mensagem encaminhada.
- O resumo da IA aparece antes do texto OCR ou extraído dos anexos.
- As configurações usam um título localizado e curto; o Telegram controla o alinhamento dos botões.
- Apenas uma resposta explícita ao pedido de reflexão noturna é guardada como reflexão. Um texto, link ou ficheiro enviado separadamente após o resumo cria um rascunho normal e não fica preso num modo de entrada antigo.

### Versão 0.35.0.9

Ao definir um lembrete, você volta a uma única tela de tarefas, sem listas duplicadas. Fechar um item remove seus anexos exibidos do chat; reabrir o mesmo item reutiliza os arquivos já exibidos.

Os IDs nos resultados de busca abrem o item correspondente, e cada linha usa o ícone do cabeçalho desse item.

Mensagens encaminhadas agrupadas mantêm o remetente de cada trecho. A IA gera um resumo único do texto, do OCR e do conteúdo dos anexos compatíveis, incluindo informações visuais. Parágrafos e listas são preservados.

O Telegram controla o download no dispositivo; a prévia pode continuar desfocada durante o download. Arquivos incompatíveis ou grandes demais não podem ser analisados integralmente.

Este guia explica como usar o Telenota pelo Telegram.

### Últimas atualizações (0.35.2)

- Fotos e vídeos consecutivos do mesmo lote capturado agora são mostrados como álbum do Telegram quando o Telegram permite esse formato.
- A pré-visualização do rascunho preserva melhor tanto os contadores agrupados de anexos quanto o texto original, sem repetir várias vezes o mesmo segmento combinado.
- Em notas, tarefas e rascunhos, o rodapé ficou mais compacto: autor e fonte aparecem em uma única linha localizada, e o horário salvo mostra apenas a data e hora locais.
- Ao abrir uma nota ou rascunho pesado, não é mais necessário esperar o carregamento completo de todos os anexos para usar o cartão principal; a mídia continua carregando em segundo plano.
- As telas de Contatos, Temas e Histórico de pontos agora têm uma última linha explícita com `Voltar` / `Início`, e os grandes seletores de páginas navegam por janelas em vez de uma única grade enorme.
- As linhas do Histórico de pontos agora podem mostrar a Nota/Tarefa relacionada e um deep link para o item quando o movimento está vinculado a um item salvo que ainda existe.

### Últimas atualizações (0.36)

- Notas e tarefas agora aceitam comentários. Abra um item e toque em `Comentários (N)` para ver os comentários existentes como mensagens separadas do Telegram com botões `Comentar` / `Excluir`.
- Quando o modo de comentário está ativo, o próximo texto/mídia enviado ou encaminhado aparece primeiro como pré-visualização com `Comentar`, `Criar rascunho`, `Voltar` e `Início`; só depois da confirmação ele é salvo abaixo do item como `Comentário N`.
- Rascunhos e itens salvos mantêm as linhas de serviço do encaminhamento mais compactas: `Encaminhado sem comentários`, autor/origem e horário salvo ficam juntos sem linhas em branco extras.
- As prévias de rascunho mostram os contadores de anexos perto do fim do cartão, acima dos metadados de encaminhamento/origem, e preservam o formato do Telegram quando possível.
- Executar `Análise com IA` numa nota ou tarefa já guardada agora acrescenta o resultado abaixo do conteúdo existente, sob `Resultados da análise com IA:`, em vez de substituir o conteúdo guardado.
- Marcar uma tarefa como concluída agora cancela os lembretes agendados, e as sugestões de lembrete usam a língua de interface guardada para reconhecer meses e dias localizados.
- `Mais` não inclui mais um botão duplicado de `Configurações`; abra Configurações pela tela inicial.
- `Pontos` inclui um link direto para a documentação pública de pontos.
- As sugestões de `Combinar` agora priorizam itens com etiquetas parecidas sem IA; o ranqueamento semântico com IA não fica ativo por padrão porque adicionaria custo e latência.

### Versão 0.36.0.0

O bônus diário é creditado na primeira ação válida, não à meia-noite. Um novo item ou comentário, inclusive ao concluir uma tarefa, deve ter mais de 100 caracteres visíveis; compartilhar ou atribuir a outra pessoa não exige tamanho mínimo. O bônus não se repete no mesmo dia local nem recalcula saldos anteriores. As recompensas de boas-vindas e de compartilhamento mantêm suas regras.

A busca mostra todos os resultados por relevância, com paginação padrão. Voltar de um item restaura a consulta e a página anteriores sem cobrar outro resumo de IA.

O áudio AAC é empacotado localmente em M4A sem recodificação antes da transcrição. O anexo original não muda. Um rascunho sem texto com um arquivo Markdown mostra uma descrição clara e a quantidade de documentos.

Os botões de um rascunho pendente ficam no cartão principal até serem usados, mesmo após abrir outro rascunho. Salvar, fechar ou excluir um item remove as cópias dos anexos exibidas pelo bot, inclusive durante o envio; as mensagens originais são mantidas.

As fontes de sites não se repetem, e os links do texto são preservados. Cada trecho encaminhado mostra «autor: mensagem», com link para a mensagem original quando o Telegram o fornece; encaminhamentos privados ou ocultos podem não expor esse link. Os links de parágrafos numerados são preservados. Rascunhos antigos não são reescritos em massa.

### Versão 0.36.0.1

Anexos e mensagens encaminhadas criam um novo rascunho, em vez de serem interpretados como uma data de lembrete, mesmo quando o resumo da noite aguarda resposta. Uma sugestão de lembrete não ativa a digitação de datas; abra Lembrete explicitamente para digitar uma data.

As ações Nota com IA e Tarefa com IA aparecem sempre em rascunhos novos e reabertos, inclusive os de texto puro. O acesso à IA e o saldo são verificados ao tocar; o salvamento comum continua disponível.

Na sugestão de enviar ou atribuir um registro às pessoas mencionadas, Voltar fecha apenas a sugestão, mantendo a tela, a página e os anexos anteriores. Voltar ao registro continua sendo uma ação separada.

### Últimas atualizações (0.36.2.phase4-5)

- A prévia do rascunho pode mostrar um seletor de tradução vermelho/verde antes de salvar. Vermelho mantém o idioma original; verde traduz o rascunho para o idioma da sua interface ao salvar uma nota ou tarefa normal.
- Os resumos de IA de notas e tarefas agora usam o idioma de interface escolhido, mesmo quando o texto de origem está em outro idioma.
- Mensagens encaminhadas rapidamente são mescladas na ordem de chegada.
- Telas de mesclagem abertas a partir de mensagens com mídia agora usam fallback seguro em vez de mostrar erro de edição do Telegram.
- Álbuns encaminhados agora são salvos de forma serializada para preservar cada imagem, vídeo e legenda na ordem original. Enquetes encaminhadas salvam uma cópia textual das opções e dos resultados disponíveis; sem resultados, uma nota pede que você vote na enquete original.
- Para linhas de endereço explícitas, o bot pode sugerir correspondências exatas do OpenStreetMap. Elas só são adicionadas como comentários de localização após confirmação ao salvar a nota ou tarefa.

### Atualizações mais recentes (0.36.4)

- Os comentários preservam a formatação do Telegram e usam `Salvar`, `❌ Excluir` e `Voltar`; voltar ou excluir também remove a tela antiga de comentários.
- Os instantâneos de enquetes mostram os votos por opção e o total somente quando o Telegram fornece esses dados. Caso contrário, a Telenota informa claramente que os resultados são desconhecidos e nunca inventa votos zero.
- Endereços claros são detectados em mensagens diretas e encaminhadas, inclusive com abreviações de rua em vários idiomas. Apenas o endereço candidato extraído é enviado ao OpenStreetMap, e correspondências ambíguas não são adicionadas.
- Nos blocos de contato, `Контакты: av. Aragon nº4-bis` é extraído como `Avenida Aragon, 4-bis`. Abreviações de vias e indicadores espanhóis de número são normalizados sem perder `-bis` ou sufixos de letras. Telefones, e-mails e links próximos não entram na consulta. Uma cidade informada é mantida; o bot não inventa a cidade nem uma localização aproximada.

### Versão 0.37.0.0

A exportação para o calendário aparece no registro quando uma data ou horário é detectado e fica sempre disponível em Mais. O nome do botão não mostra o preço; a exportação custa 0,10 ponto. Ao tocar, você recebe diretamente um arquivo de evento .ics, sem prévia intermediária no bot, e um link alternativo do Google Agenda. Abra o arquivo no calendário e confirme a importação; o Telegram ou o sistema pode pedir que você escolha um aplicativo. A abertura automática do calendário padrão não é garantida no iOS, Android ou computador.

Se o Telegram não confirmar o envio do ICS, o bot envia uma mensagem separada com o link preenchido do Google Agenda. A confirmação é um ID de mensagem e de arquivo retornado pelo Telegram, não o download ou a importação no dispositivo. O link não exige conectar o bot via OAuth.

Somente uma data cria um evento de dia inteiro; somente um horário usa o dia de hoje no fuso salvo, mesmo se o horário já passou. Data e horário usam o momento indicado. A duração padrão é de 60 minutos. O título começa com o ícone de nota/tarefa e usa o título do registro; a descrição contém um link para o registro no bot, sem o texto privado. Se a data estiver ausente, inválida ou ambígua, Mais pede uma única data/horário de início; Voltar cancela, e anexos ou encaminhamentos criam um novo rascunho.

Uma única entrega bem-sucedida do mesmo evento é cobrada por usuário. Obter novamente é grátis, inclusive após reiniciar o bot; falhas no envio são reembolsadas. Alterar título, data ou horário gera outro evento. O bot não confirma o salvamento no calendário. Reimportar pode duplicar eventos; alterações futuras não são sincronizadas. O arquivo some do chat ao fechar os anexos do registro. Não é necessário conectar uma conta de calendário nem usar análise de IA paga.

A leitura em voz alta mantém os links do autor e da fonte, inclusive ao converter uma nota em tarefa ou vice-versa. Links sem esquema, como Tambur.pub, abrem por HTTPS em vez de aparecerem como Markdown.

A duração do áudio gerado é medida e mantida ao reabrir o registro. Repetir a leitura do mesmo texto com a mesma voz e modelo reutiliza o arquivo salvo, sem nova cobrança de geração por IA nem anexo duplicado. Alterar o texto lido cria uma nova versão. Arquivos de áudio antigos de origem desconhecida não são excluídos automaticamente.

### Versão 0.37.0.1

Os botões do calendário agora respondem corretamente e não mostram o preço. Se o envio do ICS não for confirmado, o bot oferece um link separado do Google Agenda na mesma exportação de 0,10 ponto. Endereços como `av. Aragon nº4-bis` preservam o número do imóvel; telefone e e-mail ficam fora da consulta. Não é necessário conectar uma conta do Google.

### Versão 0.37.0.3 — bônus e mensagens do sistema

Um dia local ativo rende 0,50 ponto; os três dias seguintes sem atividade válida rendem 0,30, 0,15 e 0,05. No quarto dia, os bônus param com um aviso. Vale criar um registro ou comentário com mais de 100 caracteres visíveis, compartilhar ou atribuir um registro a outra pessoa; visualizar, editar e receber cópias não conta. Após um bônus de inatividade, a atividade apenas completa o total diário até 0,50. Não há créditos retroativos nem recálculo de saldos. O processamento ocorre na primeira hora local; falhas podem atrasar ou impedir o aviso nesse dia.

Configurações → Ocultar mensagens do sistema: 5, 10 ou 30 segundos, 1 minuto ou Nunca; padrão de 30 segundos. Vale para novos avisos temporários, não para limpeza de navegação nem sincronização técnica do teclado. Botões de rascunhos pendentes ficam até uma ação. Google OAuth foi adiado; ICS e links Google continuam por 0,10 ponto, sem preço no botão.

### Correções da versão 0.37.0.3

As confirmações de criação usam espaços comuns, sem quebras de linha forçadas. O Telegram e o sistema operacional controlam a aparência final da notificação.

Na sugestão de compartilhar uma nota, Compartilhar e Abrir nota aparecem na mesma linha; Voltar fica separado e fecha apenas a sugestão. Comentários e Calendário compartilham uma linha quando o calendário está disponível.

O rascunho preserva o link original antes da conclusão do resumo. Salvar um resumo alternativo mantém sua fonte. Novas cobranças de enriquecimento por IA e comprovantes de exportação guardam a referência da nota para os links do histórico; referências antigas ausentes não são adivinhadas nem reescritas.

Expressões como «сегодня в 19» incluem um horário, não apenas uma data. Um link de videochamada compatível é exportado como local no ICS e no Google. A convenção regional configurável CET/CEST usa Europe/Madrid com horário de verão, não um deslocamento fixo UTC+01:00. Vários locais diferentes exigem esclarecimento.

### Versão 0.38.0.0 — lembretes e mesclagem confiáveis

Datas como “28.10” são reconhecidas separadamente do resumo, com um lembrete opcional em UTC. Tarefas com data e hora futuras reconhecidas recebem um lembrete; quando há apenas a data, é usado o horário salvo do resumo diário de tarefas. Se não estiver configurado, escolha o horário. Itens antigos não são reagendados automaticamente.

As sugestões de mesclagem priorizam assuntos em comum e depois a relevância do texto, excluindo itens arquivados. O ID e o título do destino são mantidos, e os textos completos são concatenados sem reescrita por IA. Anexos distintos e lembretes agendados são preservados. O original é arquivado para recuperação; os comentários originais permanecem nele.

Os títulos das seções de resumo e texto extraído ficam em negrito; seções de análise idênticas são omitidas. O título da nota breve não mostra mais o limite de palavras. Sublinhados em nomes de usuário são preservados. A sugestão de compartilhamento oferece uma única ação para abrir o item, sem controles de retorno duplicados. Avisos de criação não incluem preenchimento invisível; a quebra da notificação nativa depende do dispositivo.

Os valores dos bônus não mudam. As tentativas de entrega persistem sem novo crédito no saldo. O OAuth do Google continua adiado. A confirmação de envio pelo Telegram não comprova o download no dispositivo; os atrasos das imagens continuam em investigação.

### 0.39.0.0

Busca local, paginação e retorno aos resultados são gratuitos. Responder com IA solicita explicitamente uma resposta paga, sem preço no botão. Respostas inalteradas são reutilizadas na mesma sessão.

GPT-Transcribe reconhece a fala. Uma etapa de formatação preserva turnos de diálogo apenas quando há evidências explícitas; não identifica pessoas pela voz. Resumo, título e metadados reutilizam uma análise conjunta.

Antes de analisar um vídeo em várias etapas, o bot reserva o custo total. Se não puder entregar o resultado completo, a reserva será devolvida; um vídeo sem áudio utilizável pode ser analisado visualmente sem cobrança pela transcrição que falhou.

### 0.39.0.1

A exportação ICS continua disponível; o link do Google usa a entrada testada no celular e no computador. Confirme e salve o evento no calendário. A busca local pondera palavras-chave sem IA nem cobrança adicional. As listas ativas excluem tarefas concluídas sem excluir os registros mantidos. Os erros oferecem Voltar e Início. Os resultados de links na fila usam o idioma da interface salvo atualmente; o título e a descrição disponíveis servem como alternativa, mas páginas restritas podem continuar inacessíveis. A lentidão no carregamento de fotos continua em investigação; as fotos não são convertidas em arquivos nem recomprimidas.
