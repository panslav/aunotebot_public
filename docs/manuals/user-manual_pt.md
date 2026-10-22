# Manual do usuário

## 0.39.0.0

Busca local, paginação e retorno aos resultados são gratuitos. Responder com IA solicita explicitamente uma resposta paga, sem preço no botão. Respostas inalteradas são reutilizadas na mesma sessão.

GPT-Transcribe reconhece a fala. Uma etapa de formatação preserva turnos de diálogo apenas quando há evidências explícitas; não identifica pessoas pela voz. Resumo, título e metadados reutilizam uma análise conjunta.

Antes de analisar um vídeo em várias etapas, o bot reserva o custo total. Se não puder entregar o resultado completo, a reserva será devolvida; um vídeo sem áudio utilizável pode ser analisado visualmente sem cobrança pela transcrição que falhou.

## Versão 0.38.0.0 — lembretes e mesclagem confiáveis

Datas como “28.10” são reconhecidas separadamente do resumo, com um lembrete opcional em UTC. Tarefas com data e hora futuras reconhecidas recebem um lembrete; quando há apenas a data, é usado o horário salvo do resumo diário de tarefas. Se não estiver configurado, escolha o horário. Itens antigos não são reagendados automaticamente.

As sugestões de mesclagem priorizam assuntos em comum e depois a relevância do texto, excluindo itens arquivados. O ID e o título do destino são mantidos, e os textos completos são concatenados sem reescrita por IA. Anexos distintos e lembretes agendados são preservados. O original é arquivado para recuperação; os comentários originais permanecem nele.

Os títulos das seções de resumo e texto extraído ficam em negrito; seções de análise idênticas são omitidas. O título da nota breve não mostra mais o limite de palavras. Sublinhados em nomes de usuário são preservados. A sugestão de compartilhamento oferece uma única ação para abrir o item, sem controles de retorno duplicados. Avisos de criação não incluem preenchimento invisível; a quebra da notificação nativa depende do dispositivo.

Os valores dos bônus não mudam. As tentativas de entrega persistem sem novo crédito no saldo. O OAuth do Google continua adiado. A confirmação de envio pelo Telegram não comprova o download no dispositivo; os atrasos das imagens continuam em investigação.

## Versão 0.37.0.3 — bônus e mensagens do sistema

Um dia local ativo rende 0,50 ponto; os três dias seguintes sem atividade válida rendem 0,30, 0,15 e 0,05. No quarto dia, os bônus param com um aviso. Vale criar um registro ou comentário com mais de 100 caracteres visíveis, compartilhar ou atribuir um registro a outra pessoa; visualizar, editar e receber cópias não conta. Após um bônus de inatividade, a atividade apenas completa o total diário até 0,50. Não há créditos retroativos nem recálculo de saldos. O processamento ocorre na primeira hora local; falhas podem atrasar ou impedir o aviso nesse dia.

Configurações → Ocultar mensagens do sistema: 5, 10 ou 30 segundos, 1 minuto ou Nunca; padrão de 30 segundos. Vale para novos avisos temporários, não para limpeza de navegação nem sincronização técnica do teclado. Botões de rascunhos pendentes ficam até uma ação. Google OAuth foi adiado; ICS e links Google continuam por 0,10 ponto, sem preço no botão.

## Correções da versão 0.37.0.3

As confirmações de criação usam espaços comuns, sem quebras de linha forçadas. O Telegram e o sistema operacional controlam a aparência final da notificação.

Na sugestão de compartilhar uma nota, Compartilhar e Abrir nota aparecem na mesma linha; Voltar fica separado e fecha apenas a sugestão. Comentários e Calendário compartilham uma linha quando o calendário está disponível.

O rascunho preserva o link original antes da conclusão do resumo. Salvar um resumo alternativo mantém sua fonte. Novas cobranças de enriquecimento por IA e comprovantes de exportação guardam a referência da nota para os links do histórico; referências antigas ausentes não são adivinhadas nem reescritas.

Expressões como «сегодня в 19» incluem um horário, não apenas uma data. Um link de videochamada compatível é exportado como local no ICS e no Google. A convenção regional configurável CET/CEST usa Europe/Madrid com horário de verão, não um deslocamento fixo UTC+01:00. Vários locais diferentes exigem esclarecimento.

## Versão 0.37.0.1

Os botões do calendário agora respondem corretamente e não mostram o preço. Se o envio do ICS não for confirmado, o bot oferece um link separado do Google Agenda na mesma exportação de 0,10 ponto. Endereços como `av. Aragon nº4-bis` preservam o número do imóvel; telefone e e-mail ficam fora da consulta. Não é necessário conectar uma conta do Google.

## Versão 0.37.0.0

A exportação para o calendário aparece no registro quando uma data ou horário é detectado e fica sempre disponível em Mais. O nome do botão não mostra o preço; a exportação custa 0,10 ponto. Ao tocar, você recebe diretamente um arquivo de evento .ics, sem prévia intermediária no bot, e um link alternativo do Google Agenda. Abra o arquivo no calendário e confirme a importação; o Telegram ou o sistema pode pedir que você escolha um aplicativo. A abertura automática do calendário padrão não é garantida no iOS, Android ou computador.

Se o Telegram não confirmar o envio do ICS, o bot envia uma mensagem separada com o link preenchido do Google Agenda. A confirmação é um ID de mensagem e de arquivo retornado pelo Telegram, não o download ou a importação no dispositivo. O link não exige conectar o bot via OAuth.

Somente uma data cria um evento de dia inteiro; somente um horário usa o dia de hoje no fuso salvo, mesmo se o horário já passou. Data e horário usam o momento indicado. A duração padrão é de 60 minutos. O título começa com o ícone de nota/tarefa e usa o título do registro; a descrição contém um link para o registro no bot, sem o texto privado. Se a data estiver ausente, inválida ou ambígua, Mais pede uma única data/horário de início; Voltar cancela, e anexos ou encaminhamentos criam um novo rascunho.

Uma única entrega bem-sucedida do mesmo evento é cobrada por usuário. Obter novamente é grátis, inclusive após reiniciar o bot; falhas no envio são reembolsadas. Alterar título, data ou horário gera outro evento. O bot não confirma o salvamento no calendário. Reimportar pode duplicar eventos; alterações futuras não são sincronizadas. O arquivo some do chat ao fechar os anexos do registro. Não é necessário conectar uma conta de calendário nem usar análise de IA paga.

A leitura em voz alta mantém os links do autor e da fonte, inclusive ao converter uma nota em tarefa ou vice-versa. Links sem esquema, como Tambur.pub, abrem por HTTPS em vez de aparecerem como Markdown.

A duração do áudio gerado é medida e mantida ao reabrir o registro. Repetir a leitura do mesmo texto com a mesma voz e modelo reutiliza o arquivo salvo, sem nova cobrança de geração por IA nem anexo duplicado. Alterar o texto lido cria uma nova versão. Arquivos de áudio antigos de origem desconhecida não são excluídos automaticamente.

## Versão 0.36.0.1

Anexos e mensagens encaminhadas criam um novo rascunho, em vez de serem interpretados como uma data de lembrete, mesmo quando o resumo da noite aguarda resposta. Uma sugestão de lembrete não ativa a digitação de datas; abra Lembrete explicitamente para digitar uma data.

As ações Nota com IA e Tarefa com IA aparecem sempre em rascunhos novos e reabertos, inclusive os de texto puro. O acesso à IA e o saldo são verificados ao tocar; o salvamento comum continua disponível.

Na sugestão de enviar ou atribuir um registro às pessoas mencionadas, Voltar fecha apenas a sugestão, mantendo a tela, a página e os anexos anteriores. Voltar ao registro continua sendo uma ação separada.

## Versão 0.36.0.0

O bônus diário é creditado na primeira ação válida, não à meia-noite. Um novo item ou comentário, inclusive ao concluir uma tarefa, deve ter mais de 100 caracteres visíveis; compartilhar ou atribuir a outra pessoa não exige tamanho mínimo. O bônus não se repete no mesmo dia local nem recalcula saldos anteriores. As recompensas de boas-vindas e de compartilhamento mantêm suas regras.

A busca mostra todos os resultados por relevância, com paginação padrão. Voltar de um item restaura a consulta e a página anteriores sem cobrar outro resumo de IA.

O áudio AAC é empacotado localmente em M4A sem recodificação antes da transcrição. O anexo original não muda. Um rascunho sem texto com um arquivo Markdown mostra uma descrição clara e a quantidade de documentos.

Os botões de um rascunho pendente ficam no cartão principal até serem usados, mesmo após abrir outro rascunho. Salvar, fechar ou excluir um item remove as cópias dos anexos exibidas pelo bot, inclusive durante o envio; as mensagens originais são mantidas.

As fontes de sites não se repetem, e os links do texto são preservados. Cada trecho encaminhado mostra «autor: mensagem», com link para a mensagem original quando o Telegram o fornece; encaminhamentos privados ou ocultos podem não expor esse link. Os links de parágrafos numerados são preservados. Rascunhos antigos não são reescritos em massa.

## Versão 0.35.0.9

Ao definir um lembrete, você volta a uma única tela de tarefas, sem listas duplicadas. Fechar um item remove seus anexos exibidos do chat; reabrir o mesmo item reutiliza os arquivos já exibidos.

Os IDs nos resultados de busca abrem o item correspondente, e cada linha usa o ícone do cabeçalho desse item.

Mensagens encaminhadas agrupadas mantêm o remetente de cada trecho. A IA gera um resumo único do texto, do OCR e do conteúdo dos anexos compatíveis, incluindo informações visuais. Parágrafos e listas são preservados.

O Telegram controla o download no dispositivo; a prévia pode continuar desfocada durante o download. Arquivos incompatíveis ou grandes demais não podem ser analisados integralmente.

Este guia explica como usar o AUNotebot pelo Telegram.

Nota de manutenção (esclarecimento do limite de áudio v1.0): para áudio enviado pelo Telegram, este bot aplica o limite de download da Telegram Bot API.

## 1. Início
1. Abra o chat com o bot.
2. Envie `/start`.
3. `/start` sempre recarrega e reaplica suas configurações salvas, especialmente Idioma e visibilidade do menu inferior.
4. Você verá:
   - mensagem de boas-vindas:
     - `Bem-vindo ao bot Telenota.`
     -
     - `📝🗣️🎥🌃➡️🧠✅`
     - `Faça anotações onde sua vida acontece.`
     - `Registre ideias, pensamentos e tarefas, e não se esqueça de mais nada.`
     -
     - `1️⃣ Escreva para mim, envie uma mensagem de voz, uma imagem, uma nota de vídeo ou um vídeo comum.`
     - `2️⃣ Vou salvar isso e criar uma nota ou tarefa. Minha IA vai analisar e fazer um breve resumo.`
     - `3️⃣ Deixe como nota ou transforme em tarefa para compartilhar ou definir um lembrete.`
     -
     - `⚖️ Ao usar o bot, você concorda com os Termos de Uso (clique em Mais -> Legal).`
     - `❓ Clique em Mais -> Ajuda para abrir o guia do usuário.`
     - `✉️ Ideias ou sugestões: @telenota_chat.`
   - versão atual na última linha da mensagem de boas-vindas
   - contadores e atalhos inline:
     - linha 1: `Notas`, `Tarefas`
     - linha 2: `Rascunhos`, `Lembretes`
     - linha 3: `Buscar`, `Mais`
     - linha 5: botão opcional `Seguir novidades do Telenota` no idioma atual da interface
   - menu de comandos do Telegram (menu hambúrguer) com atalhos
5. Abrir `/start` ou qualquer lista oculta telas antigas de listas/início para que apenas a tela solicitada permaneça visível.
6. Listas abertas por atalhos mostram um título compacto acima dos botões em vez de uma mensagem vazia de marcador.
7. Se houver um canal de novidades configurado para o idioma da sua interface, `/start` também mostra um botão opcional com notícias, dicas e exemplos do Telenota nesse idioma. Segui-lo é opcional e não afeta o uso do bot.

Documentos públicos de termos:
- [Repositório de documentos legais](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Abra `Mais -> Legal` para abrir a página de termos no idioma atual da sua interface.
- Políticas de Uso da OpenAI (base das funções de IA):
  - https://openai.com/en-GB/policies/usage-policies/
  - recursos de IA podem ser limitados ou desativados se uma solicitação violar essas políticas.
- Nota de acompanhamento administrativo:
  - o bot armazena registros de auditoria de ações (`moment`, `action_type`) e relações de compartilhamento (`source`, `target`, `action_type`) para operações e análise de grafo.

Manuais públicos do usuário:
- [Repositório de manuais públicos](https://github.com/panslav/aunotebot_public/tree/main/docs/manuals)
- Abra `Mais -> Ajuda` para abrir o manual no idioma atual da sua interface.

## 2. Idioma
1. No primeiro `/start`, o bot tenta detectar seu idioma pela localidade do Telegram.
2. O idioma padrão de fallback é inglês.
3. Para alterar o idioma manualmente:
   - abra `Mais -> Configurações -> Idioma`
   - escolha um destes idiomas, nesta ordem: `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`, `العربية`
4. Todos os principais rótulos e botões da interface são traduzidos após a seleção.

## 2a. Pontos de IA e Telegram Stars
A exportação para o calendário custa `0,10 ponto` pela entrega bem-sucedida do arquivo ou link alternativo, uma vez por usuário e evento sem alterações. Uma falha no ICS seguida da entrega do link Google é uma única operação. Se nenhum for entregue, a reserva é devolvida. Reexportar é grátis, inclusive após reiniciar o bot. O botão não mostra o preço.

1. Ações com IA usam seu saldo de pontos.
2. Modelo de cobrança padrão:
   - `1 ponto = 1 Telegram Star`
   - `10 pontos gratuitos` uma vez quando você começa a usar o bot
   - `0,50 ponto` por dia local ativo; depois `0,30`, `0,15`, `0,05` em três dias inativos. No quarto dia, os bônus param até uma nova atividade válida. Visualizações, edições e cópias recebidas não contam.
   - nenhuma recompensa automática de pontos por criar notas/tarefas
   - `1.5 ponto / minuto` para texto em voz
   - `1.0 ponto / minuto` para análise de áudio
   - `1.5 ponto / minuto` para transformar em texto áudio/vídeo já anexado a um item salvo
   - `0.5 ponto` por OCR de imagem
   - Resumo e etiquetas: `0.20 ponto`; tradução: `0.50 ponto`; resumo de áudio, análise de quadros de vídeo e resumo de PDF: `1 ponto` por etapa. Títulos são gratuitos; análise de links: `0.05 ponto`.
3. A duração é medida no arquivo real com ffprobe antes da reserva de pontos, sem estimativa por tamanho ou duração fictícia.
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
5. Você pode compartilhar seu próprio número de telefone em `Mais -> Configurações -> Contatos -> Compartilhar meu telefone`.
6. `Mais -> Configurações` também inclui uma zona de perigo para excluir os dados da sua conta AUNotebot.
7. Excluir todos os dados remove permanentemente suas notas, tarefas, rascunhos, lembretes, contatos, configurações, histórico de pontos e registros de conta vinculados pertencentes ao bot.
8. Ao comprar pontos dentro do bot, recargas com Telegram Stars são precificadas diretamente em `XTR`.
9. Se seu saldo for insuficiente:
   - a funcionalidade de IA é bloqueada para essa ação
   - o bot mostra uma notificação
   - funcionalidades sem IA continuam funcionando
10. Ações típicas pagas com IA incluem:
   - resumos e tags
   - geração de respostas Recall/Find
   - tradução
   - interpretação livre de lembretes, fuso horário e horários de digest
   - transcrição e texto em voz

## 3. Criar uma nota
1. Envie texto simples ao bot.
2. O bot mostra uma prévia do rascunho.
3. Toque em `📝 Salvar como nota`.
4. A lista de notas é aberta.

## 4. Criar uma tarefa
Opção A:
1. Envie texto.
2. Na prévia do rascunho, toque em `🟧 Salvar como tarefa`.
3. A lista de tarefas é aberta.

Opção B:
1. Abra qualquer nota.
2. Toque em `⬛ Criar tarefa`.

## 5. Encaminhar mensagens
1. Encaminhe uma ou mais mensagens para o bot.
2. O bot combina mensagens encaminhadas próximas no tempo em um único rascunho.
   - O tempo de combinação padrão é `30` segundos.
   - Você pode alterá-lo em `Mais -> Configurações -> Tempo de combinação de mensagens`.
3. Se você adicionar texto simples logo após encaminhar, o bot o anexa como:
   - `💬 Encaminhado com comentário:`
   - `<seu texto>`
   antes da linha de fonte/rodapé.
4. Na visualização da nota/tarefa, fontes públicas de usuários do Telegram são mostradas como links clicáveis `@handle` em vez de URLs cruas `https://t.me/...`, é mantida exatamente uma linha em branco antes do rodapé final `Salvo via Telenota (...)`, e esse rodapé também inclui um link clicável `sua mensagem` para a mensagem exata do bot da qual o item foi criado quando o Telegram ainda a expõe.
5. Se uma mensagem encaminhada contiver um ou mais links web, o bot primeiro usa os metadados de prévia disponíveis de cada página e, quando eles não existem, tenta um fallback determinístico e seguro de título com base nos metadados da página (`og:title`, `twitter:title` ou HTML `<title>`).
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

## 6. Voz e vídeo
1. Envie uma mensagem de voz, arquivo de áudio (incluindo `.m4a` quando o Telegram o envia como áudio ou documento de áudio), vídeo ou nota de vídeo.
2. O bot mostra imediatamente uma mensagem de processamento quando a análise de áudio/vídeo começa.
3. O bot transcreve e prepara um rascunho. Transcrições de áudio/vídeo incluem timestamps no final de cada parágrafo quando dados de tempo estão disponíveis.
   - Se a transcrição falhar, o bot mostra `Tentar novamente`; toque para tentar de novo com o mesmo arquivo do Telegram sem reenviá-lo.
4. Toque em `📝 Salvar como nota` ou `🟧 Salvar como tarefa`.
   - Depois de salvar, o bot mostra uma mensagem de sucesso com quatro atalhos inline: abrir o item criado e a lista correspondente na primeira linha, e depois Início e Rascunhos na segunda linha.
5. Se o rascunho contiver uma data/hora reconhecível, você pode tocar em `⏰ Salvar como lembrete`.
   - Isso salva o rascunho como tarefa e agenda o lembrete imediatamente.
6. Se um rascunho combinar várias mensagens encaminhadas/com legenda ou análise de mídia por IA, a nota/tarefa salva separa as seções com divisores horizontais visíveis. A formatação do texto original e do conteúdo gerado é preservada quando o Telegram a expõe ao bot.
7. Mensagens de voz, arquivos de áudio e vídeos do Telegram maiores que `20 MB` são rejeitados antes do processamento porque a Telegram Bot API não permite que este bot baixe arquivos maiores neste runtime.
8. Se sua gravação ou vídeo tiver mais de `20 MB`, divida ou comprima manualmente e envie as partes menores uma por uma.
9. Mensagens de erro temporárias são removidas automaticamente quando você envia a próxima mensagem, toca no próximo botão do bot ou após 30 segundos.
10. Falhas recuperáveis do Telegram, da IA ou por tempo esgotado mostram um código estável, como `E-TIMEOUT-001`. Encaminhe essa mensagem para `@telenota_chat` ao pedir ajuda; o código não expõe seu conteúdo.

## 7. Imagens e capturas de tela
1. Envie ou encaminhe uma imagem/captura de tela.
2. O bot executa OCR e resume o texto/conteúdo visível importante.
3. Um rascunho é criado; depois salve como nota ou tarefa.
4. Se você enviar um documento PDF com texto e escolher uma ação de salvamento com IA, o bot mantém o conteúdo original do rascunho, adiciona o texto extraído do PDF e depois acrescenta um breve resumo com IA de até `300` palavras no idioma de interface selecionado.
5. O texto extraído é mantido em parágrafos legíveis, e o resumo com IA é renderizado em três partes curtas: introdução, parte principal e conclusão.
6. PDFs digitalizados ou compostos apenas por imagens podem falhar na análise com IA até que exista suporte de OCR para PDF.
7. Se você salvar um PDF sem IA, o rascunho/elemento mantém uma linha simples `PDF <nome do arquivo>`. Se depois abrir o elemento salvo e tocar em `Análise com IA`, o mesmo fluxo de resumo do PDF será executado ali também.
8. A Telegram Bot API não fornece aos bots o arquivo de mídia de um Story encaminhado. O bot salva a referência e pede que você envie em seguida uma captura de tela, foto ou vídeo baixado; esse arquivo é anexado ao mesmo rascunho.
9. Na análise com IA de uma imagem, o item salvo mostra primeiro o resumo de IA e depois o texto OCR reconhecido. Listas numeradas e com marcadores da imagem mantêm o formato.

## 8. Navegar por notas e tarefas
- Use o menu de comandos do Telegram (hambúrguer):
  - `🏠 Início`
  - `🔎 Buscar`
  - `📝 Notas`
  - `🗂️ Rascunhos`
  - `🟧 Tarefas`
  - `⏰ Lembretes`
  - `📚 Mais`
- Se o menu inferior estiver ativado (`Mais -> Configurações -> Mostrar menu inferior`):
  - linha 1: `📝 Notas` + nova linha + `(N)`, `⏰ Lembretes` + nova linha + `(N)`, `🟧 Tarefas` + nova linha + `(N)`
  - linha 2: `🗂️ Rascunhos` + nova linha + `(N)`, `🔎 Buscar`, `📚 Mais`
- Cabeçalhos de listas como `📝 Notas` e `🗂️ Rascunhos` são exibidos em uma única linha visível, sem espaçamento invisível.
- Quando você abre uma tarefa da página 2+ e depois a marca como concluída, exclui, converte ou define um lembrete, o bot volta para a mesma página da lista de tarefas ao mostrar a lista novamente.
  - quando ativado, o menu inferior permanece visível até que o usuário o desative nas configurações
  - esses botões abrem as mesmas telas que as ações do menu hambúrguer.
- Ou use os contadores inline na tela inicial:
  - linha 1: `📝 Notas (N)`, `🟧 Tarefas (N)`
  - linha 2: `🗂️ Rascunhos (N)`, `⏰ Lembretes (N)`
  - linha 3: `🔎 Buscar`, `📚 Mais`

## 9. Buscar (busca combinada + Recall)
1. Toque em `🔎 Buscar` (tela inicial, menu hambúrguer ou `/find`).
2. O bot entra no modo Buscar interativo e mostra:
   - `🔎 Pergunte qualquer coisa! Meu cérebro de IA vai encontrar e resumir informações para você.`
3. Envie qualquer pergunta/consulta em formato livre.
4. O bot faz ambos:
   - ranqueamento determinístico em notas e tarefas, incluindo itens arquivados
   - correspondência sensível a flexões para variações das palavras da consulta (por exemplo terminações)
   - resumo por IA dos resultados relevantes
5. Formato da resposta quando itens são encontrados:
   - texto de resumo
   - `Aqui estão os itens mais relevantes para sua solicitação:`
   - botões dos itens relevantes, mais relevantes primeiro
   - `⬅️ Voltar`
6. Se sua consulta de busca for um ID exato de item (por exemplo `219` ou `#219`) e esse item existir, ele é fixado como resultado nº 1.
7. Para sair do modo Buscar, toque em `⬅️ Voltar`.
8. `⬅️ Voltar` retorna à tela em que você estava antes do modo Buscar.
9. Se o resumo opcional por IA estiver indisponível, as correspondências locais e os botões de resultado continuam disponíveis com um resumo alternativo neutro.

## 9a. Sugestões de lembrete
1. Se uma nova nota ou tarefa contiver uma frase provável de data/hora, o bot propõe um lembrete automaticamente.
2. Se apenas uma data for detectada, o bot oferece `Manhã`, `Meio-dia`, `Noite`, além de `Definir lembrete` e `Ignorar`.
3. Enquanto essa tela estiver aberta, você pode digitar sua própria data/hora diretamente; não existe mais um botão separado de entrada manual.
4. Se apenas um horário for detectado, o bot assume a data de hoje, a menos que você digite outra data.
5. Se o item ainda for uma nota normal e você escolher `Definir lembrete`, o bot primeiro a converte em tarefa e depois agenda o lembrete.
6. Após criar o lembrete, o bot confirma o horário no seu idioma.
7. Se você abrir a configuração do lembrete a partir de um callback de mídia, o bot usa um caminho de edição seguro e ainda mostra o aviso de lembrete.

## 10. Ações de notas e tarefas

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

### Criar voz (texto para fala)
1. Abra qualquer nota ou tarefa.
2. Toque em `🔊 Criar voz`.
3. O bot mostra imediatamente uma notificação do sistema informando que a geração de texto para voz começou.
4. O bot gera uma mensagem de voz usando OpenAI (voz `onyx`), envia ao chat e anexa ao item.

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
   - Transcrições de áudio/vídeo anexadas incluem timestamps ao final de cada parágrafo quando dados de tempo estão disponíveis.
7. Se a análise com IA falhar, os pontos reservados são liberados e o item permanece inalterado.

## 11. Mesclar itens (nota/tarefa)
1. Abra um item.
2. Toque em `🔗 Mesclar`.
3. O bot mostra até 5 itens do mesmo tipo abertos recentemente.
4. Selecione o item de destino ou envie o ID do item de destino como texto.
5. O texto do item de origem é anexado ao texto do item de destino.
6. O item de origem é removido e o item de destino é aberto.
7. O aviso de mesclagem bem-sucedida aparece dentro da tela do item de destino aberto, não como mensagem separada no chat.

## 11.1 Fixar itens
1. Abra uma nota ou tarefa.
2. Toque em `📚 Mais`.
3. Toque em `📌 Fixar` para manter o item no topo da lista.
4. Toque em `📌 Desafixar` para devolvê-lo à ordem cronológica normal.

## 12. Tags
1. Abra uma nota.
2. Toque em `🏷️ Tags`.
3. Toque em uma tag para abrir notas com essa tag.
4. Para adicionar tags, envie mensagem com hashtags (exemplo: `#project #urgent`).
5. Nomes de pessoas detectados no texto da nota são adicionados automaticamente como tags com inicial maiúscula.

## 13. Editar uma nota
1. Abra nota/tarefa.
2. Toque em `✏️ Editar`.
3. Siga o prompt e envie o texto completo atualizado.
4. O bot salva a edição e adiciona timestamp de `última edição` no rodapé.

## 14. Remover ou arquivar
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

## 15. Tarefa concluída e comentários
1. Abra a tarefa.
2. Toque em `✅ Concluída`.
3. Digite um comentário opcional ou toque em `✅ Sem comentários`.
4. Todas as mensagens de anexos atualmente exibidas para essa tarefa são removidas do chat enquanto o prompt/lista de conclusão é mostrado; os anexos salvos permanecem no item.
5. O resultado segue suas Configurações:
   - Excluir
   - Arquivar
   - Manter

## 16. Lembretes
1. Abra a tarefa.
2. Toque em `⏰ Lembrete`.
3. Envie data/hora em formato livre:
   - `amanhã no mesmo horário`
   - `em 2 horas`
   - `2026-02-20 14:30`

## 17. Configurações
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

O gerenciamento de contatos está disponível em `Mais -> Configurações -> Contatos`:
- ver todos os contatos salvos para atribuições
- `➕ Adicionar contato` (digitar `@handle` ou telefone)
- `📱 Compartilhar meu telefone` (compartilhar seu próprio contato do Telegram com o bot)
- abrir contato -> `Editar` / `Excluir`
- editar atualiza o valor do contato usado nas sugestões de atribuição

## 18. Dicas
- Se uma lista for longa, use os botões de paginação.
- Use o menu de comandos (`/start`, `Notas`, `Tarefas` etc.) para navegação rápida.
- `Arquivar` oculta o item das listas normais de notas/tarefas, mas mantém os dados.

## 19. Se algo parecer quebrado no cliente
Se ações parecerem travadas (por exemplo, tocar em um botão envia sua mensagem, mas o bot não responde), tente:
- enviar `/start`
- tocar em um botão inline na tela de boas-vindas
- tocar/enviar `⬅️ Voltar` ou `/back`
- fechar e reabrir o app Telegram
- se ainda estiver travado, limpar o histórico do chat e abrir o chat com o bot novamente

## 20. Como relatar bem um bug
Ao relatar um bug, inclua:
- botão/ação exata em que você tocou
- data/hora e fuso horário exatos
- captura de tela ou gravação curta da tela
- resposta exata do bot ou que não houve resposta
- se `/start` ainda funciona enquanto outros botões não funcionam

## Documentos relacionados
- Termos de Uso: [repositório de documentos legais](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Fluxo de telas: [Fluxo de telas](/docs/Screenflow.md)
- Instalação: [Instalação](/docs/installation.md)
- Índice da documentação: [Início da documentação](/docs/README.md)

## 21. Atualizações de compartilhamento e origem
- `Mais -> Compartilhar` agora funciona tanto para notas quanto para tarefas.
- No seletor de compartilhamento, você pode escolher um contato salvo ou tocar em `Compartilhar publicamente` para criar uma mensagem encaminhável com o link de início do bot.
- Itens longos em `Compartilhar publicamente` são divididos automaticamente em várias mensagens encaminháveis; cada mensagem termina com o rodapé normal `Salvo via Telenota (<data e hora locais>)`.
- Se alguém iniciar o bot pela primeira vez pelo seu link de convite ou pelo seu link privado de compartilhamento, você receberá uma notificação persistente do bot informando que essa pessoa entrou.
- Quando o Telegram fornece metadados suficientes, `Origem` abre a mensagem original exata do Telegram.
- Rascunhos, notas e tarefas mostram a data e a hora de salvamento no seu fuso horário.

## Início guiado e rascunhos com IA
- No primeiro início, conclua três ações úteis e receba o bônus de boas-vindas em partes: `+2`, `+3` e `+5` pontos.
- `Nota com IA` e `Tarefa com IA` preservam o texto original, convertem todos os anexos compatíveis em texto na ordem e adicionam um resumo legível em três parágrafos.
- Cada anexo extraído é identificado pelo tipo e pela ordem original; o texto completo aparece antes do resumo.
- Menções nunca atribuem nem compartilham automaticamente: a Telenota pede que você escolha a ação.
- `Voltar` percorre o histórico de telas e `Início` retorna diretamente à tela principal.
- Se um item ocupar várias mensagens do Telegram, os botões aparecem abaixo da última mensagem.

## Últimas atualizações (0.35.2)
- Fotos e vídeos consecutivos do mesmo lote capturado agora são mostrados como álbum do Telegram quando o Telegram permite esse formato.
- A pré-visualização do rascunho preserva melhor tanto os contadores agrupados de anexos quanto o texto original, sem repetir várias vezes o mesmo segmento combinado.
- Em notas, tarefas e rascunhos, o rodapé ficou mais compacto: autor e fonte aparecem em uma única linha localizada, e o horário salvo mostra apenas a data e hora locais.
- Ao abrir uma nota ou rascunho pesado, não é mais necessário esperar o carregamento completo de todos os anexos para usar o cartão principal; a mídia continua carregando em segundo plano.
- As telas de Contatos, Temas e Histórico de pontos agora têm uma última linha explícita com `Voltar` / `Início`, e os grandes seletores de páginas navegam por janelas em vez de uma única grade enorme.
- As linhas do Histórico de pontos agora podem mostrar a Nota/Tarefa relacionada e um deep link para o item quando o movimento está vinculado a um item salvo que ainda existe.

## Últimas atualizações (0.36)
- Notas e tarefas agora aceitam comentários. Abra um item e toque em `Comentários (N)` para ver os comentários existentes como mensagens separadas do Telegram com botões `Comentar` / `Excluir`.
- Quando o modo de comentário está ativo, o próximo texto/mídia enviado ou encaminhado aparece primeiro como pré-visualização com `Comentar`, `Criar rascunho`, `Voltar` e `Início`; só depois da confirmação ele é salvo abaixo do item como `Comentário N`.
- Rascunhos e itens salvos mantêm as linhas de serviço do encaminhamento mais compactas: `Encaminhado sem comentários`, autor/origem e horário salvo ficam juntos sem linhas em branco extras.
- As prévias de rascunho mostram os contadores de anexos perto do fim do cartão, acima dos metadados de encaminhamento/origem, e preservam o formato do Telegram quando possível.
- Executar `Análise com IA` numa nota ou tarefa já guardada agora acrescenta o resultado abaixo do conteúdo existente, sob `Resultados da análise com IA:`, em vez de substituir o conteúdo guardado.
- Marcar uma tarefa como concluída agora cancela os lembretes agendados, e as sugestões de lembrete usam a língua de interface guardada para reconhecer meses e dias localizados.
- `Mais` não inclui mais um botão duplicado de `Configurações`; abra Configurações pela tela inicial.
- `Pontos` inclui um link direto para a documentação pública de pontos.
- As sugestões de `Combinar` agora priorizam itens com etiquetas parecidas sem IA; o ranqueamento semântico com IA não fica ativo por padrão porque adicionaria custo e latência.

## Últimas atualizações (0.36.2.phase4-5)
- A prévia do rascunho pode mostrar um seletor de tradução vermelho/verde antes de salvar. Vermelho mantém o idioma original; verde traduz o rascunho para o idioma da sua interface ao salvar uma nota ou tarefa normal.
- Os resumos de IA de notas e tarefas agora usam o idioma de interface escolhido, mesmo quando o texto de origem está em outro idioma.
- Mensagens encaminhadas rapidamente são mescladas na ordem de chegada.
- Telas de mesclagem abertas a partir de mensagens com mídia agora usam fallback seguro em vez de mostrar erro de edição do Telegram.
- Álbuns encaminhados agora são salvos de forma serializada para preservar cada imagem, vídeo e legenda na ordem original. Enquetes encaminhadas salvam uma cópia textual das opções e dos resultados disponíveis; sem resultados, uma nota pede que você vote na enquete original.
- Para linhas de endereço explícitas, o bot pode sugerir correspondências exatas do OpenStreetMap. Elas só são adicionadas como comentários de localização após confirmação ao salvar a nota ou tarefa.

## Atualizações mais recentes (0.36.4)
- Os comentários preservam a formatação do Telegram e usam `Salvar`, `❌ Excluir` e `Voltar`; voltar ou excluir também remove a tela antiga de comentários.
- Os instantâneos de enquetes mostram os votos por opção e o total somente quando o Telegram fornece esses dados. Caso contrário, a Telenota informa claramente que os resultados são desconhecidos e nunca inventa votos zero.
- Endereços claros são detectados em mensagens diretas e encaminhadas, inclusive com abreviações de rua em vários idiomas. Apenas o endereço candidato extraído é enviado ao OpenStreetMap, e correspondências ambíguas não são adicionadas.
- Nos blocos de contato, `Контакты: av. Aragon nº4-bis` é extraído como `Avenida Aragon, 4-bis`. Abreviações de vias e indicadores espanhóis de número são normalizados sem perder `-bis` ou sufixos de letras. Telefones, e-mails e links próximos não entram na consulta. Uma cidade informada é mantida; o bot não inventa a cidade nem uma localização aproximada.

## Versão 0.35.0.4
- Os títulos com IA usam o texto disponível, o resumo do link e a análise dos anexos compatíveis. Um rascunho que contém apenas um anexo mantém um título pelo tipo de mídia até ser analisado.
- A análise com IA de um item salvo combina o texto atual com o texto extraído de todos os anexos compatíveis antes de acrescentar o resultado.
- Em encaminhamentos agrupados, cada segmento mostra o autor antes do texto. A sugestão de lembrete desaparece após qualquer ação; `Pular` apenas ignora o lembrete.

## Versão 0.35.0.5
- Num elemento combinado, cada autor aparece antes do texto da sua mensagem encaminhada.
- O resumo da IA aparece antes do texto OCR ou extraído dos anexos.
- As configurações usam um título localizado e curto; o Telegram controla o alinhamento dos botões.
- Apenas uma resposta explícita ao pedido de reflexão noturna é guardada como reflexão. Um texto, link ou ficheiro enviado separadamente após o resumo cria um rascunho normal e não fica preso num modo de entrada antigo.
