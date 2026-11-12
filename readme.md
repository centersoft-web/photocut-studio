# ✦ Studio Retrato FX

Editor de fotografias completo que roda inteiramente no navegador, sem upload para servidores, sem dependências externas e sem build. Um único arquivo `index.html` com tudo o que é necessário para carregar, editar, aplicar efeitos artísticos, remover fundo, pintar, salvar projetos e exportar imagens em alta qualidade.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/license-a%20definir-lightgrey)

---

## 📋 Índice

- [Sobre o projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Como usar](#como-usar)
- [Atalhos de teclado](#atalhos-de-teclado)
- [Formato de projeto](#formato-de-projeto)
- [Instalação no computador](#instalacao-no-computador)
- [Instalação no celular ou tablet](#instalacao-no-celular-ou-tablet)
- [Observações sobre instalação como PWA](#observacoes-pwa)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Tecnologias utilizadas](#tecnologias-utilizadas)
- [Compatibilidade](#compatibilidade)
- [Licença](#licenca)
- [Aviso](#aviso)

---

<a id="sobre-o-projeto"></a>
## ✨ Sobre o projeto

O **Studio Retrato FX** é um editor de imagens feito como projeto de estudo de **HTML, CSS e JavaScript puro**, sem frameworks, sem bibliotecas externas e sem nenhuma requisição de rede durante o uso — toda a edição acontece localmente no seu navegador.

Basta abrir o `index.html` (ou acessar a versão publicada) e começar a editar.

---

<a id="funcionalidades"></a>
## 🎨 Funcionalidades

### Edição e ajustes
- **11 ajustes por slider**: brilho, contraste, saturação, sépia, cinza, desfoque, granulação, craquelê, vinheta, matiz e inversão.
- **14 presets artísticos** prontos: Original, Envelhecido, Cartoon, HQ Vibrante, Noir, Vintage, Esboço, Cyber, Craquelê, Aquarela, Pôster, Duotone, Glow e Dramático.
- **Modo cartoon artístico** com controles de contornos, quantidade de cores e suavização.

### Ferramentas
- **Cortar** com área arrastável e aplicação instantânea.
- **Girar** 90° para esquerda/direita e **espelhar** horizontalmente.
- **Remover fundo** por ponto clicado (flood-fill com tolerância ajustável) — gera transparência real.
- **Pintura livre**: lápis, pincel, borracha, balde de tinta, linha e conta-gotas para copiar cor.
- **Copiar / colar** imagens dentro do editor.
- **Zoom** de 5% a 800%, com atalho no cursor (roda do mouse).
- **Desfazer / Refazer** com histórico de até 15 estados.

### Arquivos
- **Carregar**: JPG, PNG, WEBP e BMP — com respeito à orientação EXIF de fotos de celular.
- **Arrastar e soltar** imagens diretamente na janela.
- **Exportar** em PNG, JPG, WEBP ou BMP, com qualidade ajustável (JPG compõe fundo branco automaticamente quando há transparência).
- **Salvar projeto** (`.json`): guarda a imagem de trabalho, ajustes, rotação e orientação — permite retomar exatamente de onde parou.
- **Abrir projeto** (`.json`): restaura tudo de uma vez, inclusive por drag & drop.

---

<a id="como-usar"></a>
## 🚀 Como usar

1. Abra o `index.html` no navegador **ou** acesse a versão publicada no GitHub Pages.
2. Clique em **"Carregar fotografia"** ou arraste uma imagem para a janela.
3. Use os painéis laterais para aplicar ajustes, presets, recortes, pinturas ou remover o fundo.
4. Ao terminar, clique em **"Baixar imagem"** para exportar no formato desejado — ou em **"Salvar projeto"** para guardar o estado editável.

> Tudo é processado localmente. Nenhuma imagem é enviada a servidores externos.

---

<a id="atalhos-de-teclado"></a>
## ⌨️ Atalhos de teclado

| Atalho | Ação |
|---|---|
| `Ctrl/Cmd + Z` | Desfazer |
| `Ctrl/Cmd + Shift + Z` ou `Ctrl/Cmd + Y` | Refazer |
| `Ctrl/Cmd + S` | Baixar imagem editada |
| `Ctrl/Cmd + Shift + S` | Salvar projeto (`.json`) |
| `Ctrl/Cmd + O` | Abrir projeto (`.json`) |
| `Esc` | Cancelar ferramenta ativa / cancelar recorte |
| Roda do mouse | Zoom centralizado no cursor |

---

<a id="formato-de-projeto"></a>
## 💾 Formato de projeto

O arquivo salvo é um **JSON com assinatura** que contém:

```json
{
  "app": "StudioRetratoFX",
  "version": 1,
  "name": "minha-foto",
  "savedAt": "2026-01-01T12:00:00.000Z",
  "originalDataUrl": "data:image/png;base64,...",
  "state": { "brightness": 100, "contrast": 100, "cartoon": false, "...": "..." },
  "rotation": 0,
  "flip": 1
}