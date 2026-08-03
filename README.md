# Página de vendas — Recetario Airfryer (LATAM / espanhol)

Site estático de uma página. HTML e CSS puros, sem framework, sem instalação.

## O que fazer, na ordem

### 1. Colocar o link do Kiwify

Abra o `index.html`, procure por `LINK_CHECKOUT` (fica logo no começo) e cole o link entre as aspas:

```js
const LINK_CHECKOUT = "https://pay.kiwify.com.br/SEU-LINK";
```

Só isso. **Os 5 botões da página se atualizam sozinhos.** Enquanto estiver vazio, aparece uma
tarja vermelha no topo avisando — é proposital, pra você não publicar sem querer com os botões mortos.

### 2. Trocar os textos marcados

Procure pela palavra **`REEMPLAZA`** com `Ctrl + F`. Cada ocorrência é um texto que precisa do seu conteúdo.
Quando não sobrar nenhuma, a página está pronta.

### 3. Colocar as imagens

Os retângulos tracejados são marcadores. Crie uma pasta `imagenes/` ao lado do `index.html`,
coloque as fotos lá e troque cada marcador por uma imagem:

```html
<!-- antes -->
<div class="foto">FOTO 1<br><small>Plato terminado</small></div>

<!-- depois -->
<img src="imagenes/plato-1.jpg" alt="Pollo crujiente en freidora de aire">
```

Comprima as fotos antes (use squoosh.app). Imagem pesada derruba a conversão no celular.

## Como ver antes de publicar

Dê dois cliques no `index.html` — abre no navegador direto do seu computador.
Para ver como fica no celular: `F12` e clique no ícone de celular.

## Como publicar as alterações

```bash
git add .
git commit -m "descreva o que mudou"
git push
```

O Vercel percebe e atualiza o site sozinho em uns 30 segundos.

---

## Três avisos que valem dinheiro

**Depoimentos precisam ser reais.** Estão como `REEMPLAZA` de propósito. Inventar depoimento é
publicidade enganosa e é uma das causas mais comuns de conta de anúncio bloqueada no Meta.
Se você ainda não tem cliente, **apague a seção inteira** e coloque depois.

**O contador regressivo conta até a meia-noite e reinicia todo dia.** É o padrão do mercado, mas
saiba o que está fazendo: anunciar "só hoje" numa oferta permanente é considerado prática enganosa
em vários países. Se te incomodar, é só apagar o bloco `<div class="contador">`.

**A garantia de 7 dias não é um favor.** No Brasil o CDC (art. 49) já obriga, e a maioria dos países
da América Latina tem regra parecida. Como você vai ter que cumprir de qualquer jeito, melhor usar
como argumento de venda — que é o que a página faz.

## Quando for anunciar

No topo do `index.html` tem o bloco do **Pixel do Meta** comentado. Descomente e troque
`TU_PIXEL_ID` pelo número do seu pixel. Sem isso o Meta não consegue otimizar a campanha
nem saber quem comprou.
