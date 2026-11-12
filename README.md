
Não há dependências, bundler, `npm install` ou build step. Basta publicar os arquivos estáticos.

---

## Tecnologias utilizadas

- HTML5 — estrutura semântica e atributos `aria-*` para acessibilidade.
- CSS3 — Grid Layout, Flexbox, Custom Properties, media queries, scrollbar customizada.
- JavaScript (ES2020+) — Canvas 2D API, ImageData, createImageBitmap (para EXIF), Pointer Events, Blob e FileReader, createPattern, toBlob, toDataURL e requestAnimationFrame.

Sem bibliotecas externas. Sem CDN. Sem chamadas de rede após o carregamento.

---

## Compatibilidade

- Google Chrome — suporte completo.
- Microsoft Edge — suporte completo.
- Firefox — suporte completo.
- Safari (macOS e iOS) — a maioria dos recursos. O `ctx.filter` pode estar ausente em versões antigas; nesse caso, ajustes baseados em filtro não serão aplicados na prévia.
- Navegadores móveis modernos — suporte completo.

Recomendação: use navegador atualizado e, se possível, um dispositivo com pelo menos 4 GB de RAM — imagens grandes consomem memória proporcionalmente.

---

## Licença

Nenhuma licença específica foi definida no arquivo fornecido. Antes de distribuir ou publicar o projeto, inclua uma licença compatível com a finalidade pretendida e verifique as licenças das bibliotecas externas utilizadas.

Sugestões comuns para projetos como este:

- MIT — permissiva, boa para uso pessoal e comercial.
- GPL-3.0 — obriga que trabalhos derivados também sejam abertos.
- CC BY-NC 4.0 — uso não comercial com atribuição.

Adicione um arquivo `LICENSE` na raiz do repositório com o texto da licença escolhida.

---

## Aviso

Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.

---

Feito com ✦ para aprender, experimentar e se divertir com Canvas no navegador.