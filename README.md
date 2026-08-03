# Página de vendas

Site estático de uma página só. Sem framework, sem instalação, sem complicação.

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | **A página inteira.** É o único arquivo que você edita. |
| `README.md` | Este guia. |
| `.gitignore` | Diz ao Git quais pastas ignorar. Não precisa mexer. |

## Como editar

Abra o `index.html` em qualquer editor de texto (Bloco de Notas serve).

Procure pela palavra **`SUBSTITUA`** — ela marca todo lugar que precisa do seu texto.
Use `Ctrl + F` para achar uma por uma. Quando não sobrar nenhuma, a página está pronta.

O que mais importa trocar:

1. **`<title>` e `<meta name="description">`** — aparecem no Google e na prévia do WhatsApp
2. **A headline (`<h1>`)** — é o que mais decide se a pessoa continua lendo
3. **Os links dos botões** — procure por `href="#"` e coloque o link do seu checkout
4. **O rodapé** — nome, CNPJ e e-mail de contato

## Como ver antes de publicar

Dê dois cliques no `index.html`. Ele abre no navegador direto do seu computador.
Nada disso vai pro ar até você publicar.

Para testar como fica no celular: no navegador aperte `F12` e clique no ícone de celular.

## Como publicar as alterações

Salve o arquivo e rode estes três comandos:

```bash
git add .
git commit -m "descreva o que você mudou"
git push
```

O Vercel percebe o envio e atualiza o site sozinho em cerca de 30 segundos.

## Duas coisas importantes

**Depoimentos precisam ser reais.** Depoimento inventado é propaganda enganosa pelo
Código de Defesa do Consumidor e é um dos motivos mais comuns de anúncio reprovado no Meta.
Se você ainda não tem nenhum cliente, apague a seção de depoimentos por enquanto.

**A garantia de 7 dias não é favor seu.** O artigo 49 do Código de Defesa do Consumidor
já garante o direito de arrependimento em compras online. Como você vai ter que cumprir
de qualquer forma, melhor usar isso como argumento de venda.

## Quando for rodar anúncio

Dentro do `index.html`, no topo, existe um bloco do **Pixel do Meta** comentado.
Descomente e troque `SEU_PIXEL_ID` pelo número do seu pixel. Sem isso o Meta não
consegue otimizar a campanha nem medir quem comprou.
