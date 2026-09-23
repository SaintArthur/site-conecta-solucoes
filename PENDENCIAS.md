# Pendências — site institucional da Conecta

Levantado em 23/09/2026. Números conferidos por contagem no `index.html` desta data.

> Este arquivo está no `exclude` do `_config.yml`. O GitHub Pages serve todo arquivo
> do repositório — sem essa exclusão, estas anotações ficariam públicas em
> `conectasolucoes.ia.br/PENDENCIAS.md`.

---

## 1. Os três "15 dias" — e um deles NÃO é implantação

Esta é a pendência que exige decisão antes de qualquer edição. O trial dos produtos
passou de 15 para 7 dias. Aqui aparecem três menções a 15 dias, e elas **não são a
mesma coisa**:

| Linha | Texto | O que é |
|---|---|---|
| 290 | "**15 dias** de implantação guiada" | implantação |
| 326 | "Implantação em **15 dias**" | implantação |
| 445 | "você começa os **15 dias de teste** com a implantação acompanhada" | **teste** |

A linha 445 fala de teste, não de implantação — ela está errada hoje e deve virar
7 dias junto com os outros sites.

As linhas 290 e 326 são prazo de implantação, que é outra coisa. **Decidir:** a
implantação também passou a 7 dias, ou continua 15?

## 2. Sem aviso de privacidade (LGPD)

O formulário coleta nome e WhatsApp e não há nenhuma menção a privacidade ou LGPD
no arquivo (0 ocorrências de "LGPD" ou "privacidade"). Vale para os três sites.

## 3. Conferir o número de WhatsApp

São 4 links para `wa.me/5527999073651`. Nos sites do Barber e do Bella o número é
outro — `5527999941710` — anotado por lá como número pessoal do Matheus, a ser
trocado pelo comercial. **Confirmar** se o daqui é o comercial correto.

---

## Nos outros repositórios

- **site-cs-bella** — 23 ocorrências ainda dizendo 15 dias, e a contradição do "grátis".
- **site-cs-barber** — trial já corrigido; sobra a contradição do "grátis".

Cada um tem o próprio `PENDENCIAS.md` com o detalhe.

## Publicação

Este site publica pelo **GitHub Pages**: `git push` na `main` já coloca no ar.
Os outros dois publicam por **AWS** (`./publicar.sh`), que precisa de credencial
`aws` e agora de **Node** — a ferramenta de limpeza deixou de ser Python.
