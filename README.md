# Content Bot — Instagram Studio

Aplicação estática para GitHub Pages que transforma temas fornecidos pelo usuário em pacotes de conteúdo para Instagram.

## Recursos
- Geração de roteiro, legenda, hashtags e ideias de cenas.
- Geração assistida pelo Gemini 2.5 Flash com chave informada pelo usuário no navegador.
- Modo local sem chave de API.
- Pré-visualização vertical 9:16.
- Exportação do roteiro em TXT.
- Renderização de vídeo vertical WebM no navegador usando Canvas + MediaRecorder.

## Publicar no GitHub Pages
1. Abra **Settings → Pages** no repositório.
2. Em **Build and deployment**, selecione **GitHub Actions**.
3. O workflow `.github/workflows/pages.yml` fará o deploy ao enviar alterações para `main`.
4. Acesse a URL do Pages exibida nas configurações.

## Usar
1. Abra o site publicado.
2. Digite o tema e escolha formato, duração e estilo.
3. Opcionalmente, crie uma chave no [Google AI Studio](https://aistudio.google.com/apikey) e informe-a no campo de chave Gemini.
4. Gere o conteúdo, revise roteiro e legenda.
5. Renderize o vídeo e baixe o arquivo WebM.

## Limitações importantes
- GitHub Pages é hospedagem estática: não executa Python/servidor, tarefas agendadas ou processos em segundo plano.
- A chave Gemini é enviada diretamente do navegador à API do Google e não é armazenada pelo site; evite usar em computadores compartilhados. Para produção, mova a chamada de IA para um backend com segredo protegido.
- O vídeo gerado nesta primeira versão usa cenas tipográficas animadas, não gera filmagens realistas, imagens generativas ou narração de áudio.
- A publicação automática no Instagram ainda não está habilitada. Ela requer backend seguro, conta profissional Instagram vinculada à Meta, permissões e tokens OAuth. Nunca coloque tokens de publicação no JavaScript do Pages.
- O arquivo exportado é WebM. Para compatibilidade mais ampla com Reels, converta para MP4/H.264 antes de publicar.

## Segurança
Não commite chaves de API, tokens do Instagram, arquivos `.env` ou credenciais.
