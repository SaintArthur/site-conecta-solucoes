# Pendências — site institucional da Conecta

Levantado em 23/09/2026. Números conferidos por contagem no `index.html` desta data.
Itens 1 a 3 **resolvidos em 23/09/2026**.

> Este arquivo está no `exclude` do `_config.yml`. O GitHub Pages serve todo arquivo
> do repositório — sem essa exclusão, estas anotações ficariam públicas em
> `conectasolucoes.ia.br/PENDENCIAS.md`.

---

## 1. Os "15 dias" — teste e implantação → 7 dias ✅ RESOLVIDO

O trial dos produtos passou de 15 para 7 dias. Havia **4** menções (não 3 — a linha
405 não estava no levantamento original) e todas foram trocadas para 7 dias.

**Decisão (23/09/2026):** a implantação também passou a 7 dias, junto com o teste.

| Linha | Antes | Depois | O que é |
|---|---|---|---|
| 290 | "15 dias de implantação guiada" | 7 dias | implantação |
| 326 | "Implantação em 15 dias" | 7 dias | implantação |
| 405 | "Os 15 primeiros dias são guiados" | 7 primeiros dias | implantação |
| 445 | "os 15 dias de teste" | 7 dias de teste | teste |

Obs.: "15 barbearias já rodando" (hero) é contagem de clientes, não prazo — mantido.

## 2. Aviso de privacidade (LGPD) ✅ RESOLVIDO

Adicionado aviso no rodapé do formulário. O texto reflete a implementação real: o
form não guarda dados em servidor — ele só monta a mensagem e abre o `wa.me`. Vale
rever o mesmo texto nos outros dois sites (lá o envio pode ser diferente).

## 3. Número de WhatsApp ✅ CONFIRMADO

Os 4 links usam `wa.me/5527999073651`. **Confirmado como o comercial correto** da
Conecta (23/09/2026) — mantido, e agora é também o dos sites do Barber e do Bella
(o `5527999941710`, pessoal do Matheus, saiu de lá).

---

## Formulário (23/09/2026)

Testado ao vivo com saídas interceptadas e corrigido: WhatsApp colado ou
autopreenchido com +55 ou 0 chegava como outro número (agora normaliza; número
de fora do Brasil com "+" e código de país é aceito — o site cita clientes em
Portugal); DDD 55 (RS) com um dígito a mais não vira outro número; segmento sem
escolha sai como "Tenho um negócio" em vez de "barbearia"; campos com 16px
(zoom do iPhone); botão desabilitado sem JavaScript e o formulário visível sem
ele; fallback quando o pop-up é bloqueado; trava contra envio duplicado; aviso
de LGPD reescrito (os dados vão ao WhatsApp, serviço da Meta).

## Nos outros repositórios

**site-cs-barber** e **site-cs-bella**: resolvidos trial de 7 dias, WhatsApp
comercial da Conecta (`5527999073651`), CNPJ fora do rodapé, aviso de LGPD e as
mesmas correções de formulário. "Grátis" fica, por decisão do dono. Detalhe no
`PENDENCIAS.md` de cada um — e lá o push não publica: é preciso rodar o
`./publicar.sh` (AWS).

## Publicação

Este site publica pelo **GitHub Pages**: `git push` na `main` já coloca no ar.
Os outros dois publicam por **AWS** (`./publicar.sh`), que precisa de credencial
`aws` e agora de **Node** — a ferramenta de limpeza deixou de ser Python.
