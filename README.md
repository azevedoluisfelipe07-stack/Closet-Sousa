# Closet Sousa PWA

Projeto PWA pronto para publicação em hospedagem HTTPS, incluindo GitHub Pages.

## Publicar no GitHub Pages

1. Crie um repositório e envie todos os arquivos desta pasta para a raiz (ou configure o Pages para a pasta escolhida).
2. Em **Settings > Pages**, selecione a branch e a pasta publicada.
3. Aguarde a URL HTTPS ficar ativa e abra-a no Safari do iPhone.

Se for publicado em subpasta, os caminhos relativos já usados pelo projeto permitem que ele funcione sob essa subpasta.

## Instalar no iPhone

1. Abra o endereço HTTPS no **Safari**.
2. Toque em **Compartilhar**.
3. Selecione **Adicionar à Tela de Início** e confirme.
4. Abra o ícone criado para usar em modo standalone.

A instalação final é feita pelo usuário no próprio iPhone; este projeto não instala aplicativos diretamente no aparelho.

## Recursos incluídos

- Cores preferidas selecionáveis na ficha da cliente.
- Filtros de roupas por tamanho e cor em cada ficha.
- Numeração editável das roupas, preenchida automaticamente com o próximo número.

## Atualizações e uso offline

O service worker guarda o shell do app após a primeira visita. Nas próximas visitas online, uma nova versão do HTML é obtida pela rede; quando publicada, incremente a versão em `CACHE_NAME` em `service-worker.js` (atualmente `v3`) para ativar uma instalação de cache nova e remover a antiga com segurança. Após o primeiro carregamento, o app shell permanece disponível offline. Os dados continuam no armazenamento local do navegador/aparelho, conforme o HTML original.
