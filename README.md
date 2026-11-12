# ✦ Studio Retrato FX

Editor de fotografias completo que roda inteiramente no navegador, sem upload para servidores, sem dependências externas e sem build. Um único arquivo `index.html` com tudo o que é necessário para carregar, editar, aplicar efeitos artísticos, remover fundo, pintar, salvar projetos e exportar imagens em alta qualidade.

---

## Sobre o projeto

O Studio Retrato FX é um editor de imagens feito como projeto de estudo de HTML, CSS e JavaScript puro, sem frameworks, sem bibliotecas externas e sem nenhuma requisição de rede durante o uso — toda a edição acontece localmente no seu navegador.

Basta abrir o `index.html` ou acessar a versão publicada e começar a editar.

---

## Funcionalidades

### Edição e ajustes

- 11 ajustes por slider: brilho, contraste, saturação, sépia, cinza, desfoque, granulação, craquelê, vinheta, matiz e inversão.
- 14 presets artísticos prontos: Original, Envelhecido, Cartoon, HQ Vibrante, Noir, Vintage, Esboço, Cyber, Craquelê, Aquarela, Pôster, Duotone, Glow e Dramático.
- Modo cartoon artístico com controles de contornos, quantidade de cores e suavização.

### Ferramentas

- Cortar com área arrastável e aplicação instantânea.
- Girar 90° para esquerda/direita e espelhar horizontalmente.
- Remover fundo por ponto clicado (flood-fill com tolerância ajustável) — gera transparência real.
- Pintura livre: lápis, pincel, borracha, balde de tinta, linha e conta-gotas para copiar cor.
- Copiar e colar imagens dentro do editor.
- Zoom de 5% a 800%, com atalho no cursor (roda do mouse).
- Desfazer e refazer com histórico de até 15 estados.

### Arquivos

- Carregar: JPG, PNG, WEBP e BMP — com respeito à orientação EXIF de fotos de celular.
- Arrastar e soltar imagens diretamente na janela.
- Exportar em PNG, JPG, WEBP ou BMP, com qualidade ajustável. JPG compõe fundo branco automaticamente quando há transparência.
- Salvar projeto em arquivo `.json`: guarda a imagem de trabalho, ajustes, rotação e orientação — permite retomar exatamente de onde parou.
- Abrir projeto em `.json`: restaura tudo de uma vez, inclusive por drag & drop.

---

## Como usar

1. Abra o `index.html` no navegador ou acesse a versão publicada no GitHub Pages.
2. Clique em "Carregar fotografia" ou arraste uma imagem para a janela.
3. Use os painéis laterais para aplicar ajustes, presets, recortes, pinturas ou remover o fundo.
4. Ao terminar, clique em "Baixar imagem" para exportar no formato desejado — ou em "Salvar projeto" para guardar o estado editável.

Tudo é processado localmente. Nenhuma imagem é enviada a servidores externos.

---

## Atalhos de teclado

- Ctrl/Cmd + Z — Desfazer
- Ctrl/Cmd + Shift + Z ou Ctrl/Cmd + Y — Refazer
- Ctrl/Cmd + S — Baixar imagem editada
- Ctrl/Cmd + Shift + S — Salvar projeto em `.json`
- Ctrl/Cmd + O — Abrir projeto em `.json`
- Esc — Cancelar ferramenta ativa ou cancelar recorte
- Roda do mouse — Zoom centralizado no cursor

---

## Formato de projeto

O arquivo salvo é um JSON com assinatura que contém:

- `app`: identificador fixo "StudioRetratoFX".
- `version`: versão do formato (atualmente 1).
- `name`: nome original da imagem.
- `savedAt`: data e hora do salvamento em ISO 8601.
- `originalDataUrl`: imagem de trabalho embutida em PNG base64 (preserva transparência).
- `state`: todos os sliders e ajustes aplicados.
- `rotation`: rotação atual em graus.
- `flip`: orientação horizontal (1 ou -1).

O campo `app` impede que JSONs de outras origens sejam aceitos por engano. O campo `version` permite evoluir o formato no futuro sem quebrar projetos antigos.

---

## Instalação no computador

### No Google Chrome ou Microsoft Edge:

1. Abra o endereço publicado do projeto.
2. Aguarde o carregamento completo da página.
3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

---

## Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

---

## Observações sobre instalação como PWA

- A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
- Abrir somente o arquivo `index.html` pelo computador não garante a instalação como PWA.
- O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
- O funcionamento offline depende da configuração do `service-worker.js` e dos arquivos adicionados ao cache.
- Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

Importante: esta versão do projeto é apenas o `index.html` e funciona 100% online após o carregamento. Para que a instalação como PWA funcione conforme descrito acima, é necessário adicionar ao repositório:

- Um `manifest.json` com `name`, `short_name`, `icons`, `start_url`, `display: "standalone"` e `theme_color`.
- Um `service-worker.js` que faça o cache dos arquivos estáticos.
- O registro do service worker dentro do `index.html` via `navigator.serviceWorker.register(...)`.
- Ícones `.png` em pelo menos 192×192 e 512×512 pixels.

---

## Estrutura do projeto
