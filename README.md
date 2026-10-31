# Alfajores Misky — gestão diária

App de gestão para a produção e venda de alfajores (negócio único, da socia do Renato).

## O que vai neste repositório (versão portátil, pronta hoje)

- `alfajores-misky-portable.html` — a app completa em um único arquivo (HTML/CSS/JavaScript). Abre em qualquer navegador, sem instalar nada, sem internet, dados salvos no próprio aparelho. É a versão que a socia já pode usar e mostrar.
- `ESPECIFICACAO-E-PROMPT.md` — especificação completa do negócio e da app (o mesmo prompt v2 com que se reconstrói a versão na nuvem).
- `DADOS-E-RECEITA.md` — receita real por fornada, compras iniciais e dados do negócio.
- `misky-logo.png` — logo oficial.

## Modelo de negócio (resumo, não adivinhar o resto)

- Receita por **fornada** (não por unidade): rendimento mínimo de **30 pacotes por fornada**, cada pacote = 3 alfajores.
- O material desconta por **fornada produzida** (normalmente 2 fornadas por vez).
- Vendas pelo **valor final do dia**: quantidade de pacotinhos vendidos + dinheiro arrecadado, dividido em **Pix, dinheiro e "falta pagar"**. Um lançamento por dia (salvar de novo atualiza, não duplica).
- Exportar/importar dados em `.json` para levar os dados a outro aparelho.

## Como abrir

Abra `alfajores-misky-portable.html` no navegador (celular ou computador). Não precisa de servidor nem de conta.

## GitHub Pages (link público, opcional)

Com este repositório publicado e o Pages ativado, o mesmo arquivo vira um link público para abrir no celular sem mandar arquivos. O Pages serve a versão portátil; não é a versão com login e banco de dados.

## Versão oficial na nuvem (separada, não misturar)

A versão externa em Lovable ("Misky Gestão Diária", React + Supabase, com login) terá o **seu próprio repositório** quando os créditos voltarem e o Lovable for conectado ao GitHub (botão Connect to GitHub). Esse é o repositório que o programador usará para continuar o desenvolvimento com banco de dados. Não substituir um pelo outro: portátil = uso imediato e demonstração; Lovable/GitHub = produto com login e dados na nuvem.

## Para o programador

Comece por `ESPECIFICACAO-E-PROMPT.md` e `DADOS-E-RECEITA.md`; depois abra o HTML e veja a lógica completa (vendas do dia, fornadas, desconto por receita, semáforos). Perguntas pendentes do dono do negócio (não decidir por ele): preço do pacote, custos de compra e o rótulo da meta acumulada.
