# Checkpoint 05 — Refatoração com Tailwind CSS 4.3

Refatoração da página de tênis: toda a estilização que estava em `css/styles.css` foi substituída por classes utilitárias do Tailwind CSS 4.3, mantendo o mesmo conteúdo, layout e comportamento.

## Como rodar

Pré-requisito: Node.js instalado.

```bash
npm install
npm run build
```

Depois, abra o `index.html` no navegador.

Durante o desenvolvimento, use `npm run watch` para recompilar o CSS automaticamente a cada alteração.

## Estrutura

| Arquivo | Função |
| --- | --- |
| `src/input.css` | Importa o Tailwind e define o tema (`@theme`): cores, fonte, tamanhos de texto, breakpoints e animação |
| `css/output.css` | CSS gerado pelo Tailwind (não editar manualmente) |
| `index.html` | Página com as classes utilitárias |
| `js/scroll.js` | Duplica a faixa de logos para o efeito de rolagem contínua |

## Observações

- As classes `logos` e `logos-slide` não aplicam estilo. Elas foram mantidas porque o `js/scroll.js` as usa como seletores.
- Os breakpoints `tablet` (681px) e `desktop` (1025px) reproduzem os limites das media queries originais (`width <= 680px` e `width <= 1024px`).
- Versão do Tailwind CSS: 4.3 (fixada no `package.json`).
