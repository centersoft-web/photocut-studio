# ✦ Studio Retrato FX

Um editor de imagens e retratos moderno, rápido e totalmente executado no navegador (client-side), construído com HTML5 Canvas, CSS3 e JavaScript puro (Vanilla JS). Não requer dependências externas ou envio de imagens para servidores, garantindo total privacidade durante a edição.

---

## ✨ Funcionalidades

### 🖼️ Carregamento e Gerenciamento de Projetos
* **Múltiplos Formatos:** Suporte para carregamento de imagens **JPG, PNG, WEBP e BMP** via seletor de arquivos ou arrastar e soltar (*Drag & Drop*).
* **Otimização Automática:** Redimensionamento inteligente de imagens muito grandes (limite máximo de `2400px` no maior lado) mantendo a orientação original (EXIF).
* **Salvar e Abrir Projetos:** Exporte o estado atual da sua edição (imagem base, ajustes, rotação e espelhamento) em um arquivo `.json` e retome o trabalho a qualquer momento.
* **Histórico Completo:** Sistema de Desfazer (`Ctrl+Z`) e Refazer (`Ctrl+Y` / `Ctrl+Shift+Z`) com até 15 estados armazenados, além de suporte para copiar e colar imagens na área de transferência interna.

### 🎨 Estilos e Filtros Predefinidos (Presets)
Aplique transformações visuais instantâneas com um clique:
* **Clássicos & Fotográficos:** Original, Envelhecido, Noir, Vintage, Dramático.
* **Artísticos & Ilustração:** Cartoon, HQ vibrante, Esboço, Aquarela, Pôster, Craquelê.
* **Modernos & Efeitos:** Cyber, Duotone, Glow.

### 🎛️ Ajustes Finos e Efeitos Especiais
* **Controles de Cor e Luz:** Brilho, Contraste, Saturação, Sépia, Tons de Cinza, Matiz (*Hue*) e Inversão de cores.
* **Texturas e Lente:** Desfoque (*Blur*), Granulação (*Grain* procedural), Craquelê e Vinheta.
* **Motor Cartoon Artístico:** Algoritmo dedicado com detecção de bordas (filtro Sobel), quantização de cores e suavização, com pré-visualização rápida e renderização em qualidade máxima na exportação.

### 🛠️ Ferramentas de Edição e Pintura
* **Remoção de Fundo (Varinha Mágica):** Clique em áreas uniformes (como fundos brancos, verdes ou céu) com ajuste de tolerância para torná-las transparentes.
* **Transformação e Recorte:** Rotação em 90° (esquerda/direita), espelhamento horizontal, ajuste automático à tela (*Fit*), zoom interativo com o scroll do mouse e ferramenta de corte (*Crop*) com grade da regra dos terços.
* **Kit de Pintura:** Lápis, Pincel, Borracha, Balde de tinta (com controle de tolerância), Linha reta e Conta-gotas (com exibição e cópia de código Hexadecimal).

### 💾 Exportação Flexível
* Exporte a imagem finalizada nos formatos **PNG, JPG, WEBP ou BMP** (com gerador de arquivo BMP nativo em 24-bit).
* Controle de qualidade de compressão (Máxima, Alta, Média) e preenchimento automático de fundo branco ao exportar transparências para JPG.

---

## ⌨️ Atalhos de Teclado

| Atalho | Ação |
| :--- | :--- |
| `Ctrl` + `Z` | Desfazer última ação |
| `Ctrl` + `Y` ou `Ctrl` + `Shift` + `Z` | Refazer ação |
| `Ctrl` + `S` | Baixar/Exportar imagem finalizada |
| `Ctrl` + `Shift` + `S` | Salvar arquivo de projeto (`.json`) |
| `Ctrl` + `O` | Abrir arquivo de projeto |
| `Esc` | Cancelar recorte ou desativar ferramenta ativa |
| `Scroll do Mouse` | Aplicar zoom na área de visualização |

---

## 🚀 Como Instalar e Usar (PWA)

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

## Licença

Nenhuma licença específica foi definida no arquivo fornecido. Antes de distribuir ou publicar o projeto, inclua uma licença compatível com a finalidade pretendida e verifique as licenças das bibliotecas externas utilizadas.


## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.