# Content Bot — Instagram Studio

Aplicação estática para criar conteúdo e organizar publicações para Instagram.

## Recursos
- Prompt livre com formato, duração, estilo e narração.
- Upload múltiplo de imagens e vídeos, pré-visualização e remoção.
- Gemini 2.5 Flash opcional: gera roteiro, legenda, hashtags e cenas; imagens selecionadas são enviadas para análise visual.
- Vídeo WebM montado no navegador usando a primeira mídia como fundo.
- Biblioteca local de publicações, com arquivos armazenados no IndexedDB do navegador.
- Exportação de roteiro e legenda em TXT.

## Publicar
GitHub Pages → Settings → Pages → Build and deployment → GitHub Actions.

## Limitações e privacidade
- A biblioteca fica no navegador/dispositivo atual; limpar dados do navegador pode apagá-la. Não há sincronização entre dispositivos.
- A chave Gemini é usada no cliente e não é persistida. Não use em computador compartilhado.
- Imagens são enviadas à Gemini quando a chave é informada. Vídeos são incorporados à edição/exportação, mas não são analisados automaticamente pela IA.
- O renderizador exporta WebM com a primeira mídia como fundo; não é um editor profissional multicamadas.
- O site não publica no Instagram. Publicação oficial requer backend seguro, OAuth e permissões da Meta; nunca coloque tokens no JavaScript público.
