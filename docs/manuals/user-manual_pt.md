# Manual do usuário do AUNotebot

## 1. Início
1. Abra o chat do bot.
2. Envie `/start`.
3. Na tela inicial: `Buscar`, `Tarefas`, `Notas`, `Lembretes`, `Rascunhos`, `Mais`.

## 2. Idioma
- Menu: `More -> Settings -> Idioma`.
- Idiomas suportados: English, Русский, Українська, Español, Português, Français.

## 2a. Pontos de IA e Telegram Stars
- As ações com IA usam seu saldo de pontos.
- Modelo padrão:
  - `1 ponto = 1 Telegram Star`
  - `50 pontos grátis` no primeiro uso
  - `5 pontos grátis` todos os dias às `00:00` no seu fuso local
  - `0,1 ponto = 1 ação de IA`
- Abra `More -> Points` para ver o saldo, consultar o custo atual, revisar suas últimas 5 operações de pontos, abrir o `Histórico completo de pontos` e recarregar com Telegram Stars.
- Se o saldo for insuficiente, a ação de IA é bloqueada, mas as funções sem IA continuam funcionando.

## 3. Criar uma nota
1. Envie texto/voz/vídeo/imagem.
2. O bot cria um rascunho.
3. Toque em `📝 Salvar como nota`.

## 4. Criar uma tarefa
- No rascunho: `🟧 Salvar como tarefa`.
- Ou na nota: `⬛ Make Task`.

## 5. Encaminhar mensagens
- Várias mensagens encaminhadas em uma única ação viram um rascunho só.
- O tempo de mesclagem é definido em `More -> Settings -> Tempo de fusão de múltiplas mensagens`.
- Hashtags enviados separadamente são adicionados como tags do rascunho.

## 6. Busca e Memória
- `🔎 Find` ativa modo interativo.
- Envie sua pergunta em texto livre.
- O bot retorna um resumo e botões com os itens mais relevantes.

## 7. Ações no item
### Nota
- `✏️ Edit`, `🏷️ Tags`, `⬛ Make Task`, `❌ Remove`, `⬅️ Back`

### Tarefa
- `✏️ Edit`, `✅ Done/🔄 Re-do`, `⏰ Reminder`, `🏷️ Tags`, `🔁 Make Note`, `🔀 Merge`, `👥 Assign`, `❌ Remove`, `⬅️ Back`

## 8. Tags e tópicos
- `Tags` abre as tags do item.
- Ao tocar em uma tag, abre a lista de itens relacionados.
- No menu de tópico: `Edit` e `Delete`.

## 9. Lembretes
- Em uma tarefa, toque `⏰ Reminder`.
- Digite data/hora em formato livre (ex.: «amanhã 9:00»).

## 10. Configurações
`More -> Settings`:
- Idioma
- Fuso horário
- Ao marcar como concluída
- Copiar texto para edição
- Resumo diário de tarefas
- Resumo da noite
- Tempo de fusão de múltiplas mensagens
- Nº de itens
- Mostrar menu inferior

## 11. Ajuda e legal
- `More -> Help` abre este manual na web.
- `More -> Legal` abre os Terms & Conditions no idioma atual.

## 12. Contato
- Ideias e feedback: `@aunotebot_support`

## Documentos relacionados
- Termos e Condições: [Legal docs repository](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Fluxo de telas: [Screenflow](/docs/Screenflow.md)
- Instalação: [Installation](/docs/installation.md)
