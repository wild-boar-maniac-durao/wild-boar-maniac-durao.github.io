# publico

O que vai para o repositório publicado. Nada aqui é escrito à mão exceto
`index.html` e `javali.svg`.

| arquivo | origem |
|---|---|
| `index.html` | a página. Estática, sem dependência externa |
| `javali.svg` | a arte (também embutida no HTML, para a página ser um arquivo só) |
| `doacoes.csv` | gerado pelo agente a partir do livro local, já anonimizado |
| `heartbeat.json` | reescrito pelo agente a cada 2 min |

A página lê os dois arquivos de dados por `fetch` no navegador — o HTML não tem
número nenhum embutido. Trocar o CSV atualiza a página sem regerar nada.

**Não abra o `index.html` com dois cliques**: `fetch` é bloqueado em `file://`
e a página avisa isso. Use `python -m agente servir --abrir`. Em Pages funciona
direto.
