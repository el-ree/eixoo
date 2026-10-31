# Master Prompt v2 — Alfajores Misky (colar no Lovable) — versão externa

> v2 (26/10/2026): substitui a v1. Mudanças do modelo real do negócio: produção por FORNADA com rendimento variável (mínimo 30 pacotes), desconto de material só na produção (nunca na venda), e vendas lançadas UMA vez por dia pelo VALOR FINAL do dia (pacotinhos vendidos + dinheiro dividido em Pix / dinheiro / falta pagar). Receita e compras reais incluídas.

```
Crie um aplicativo web completo e funcional, mobile-first (uso principal no celular, como PWA instalável na tela inicial), em português brasileiro, para UM único negócio chamado "Alfajores Misky". É uma ferramenta interna de gestão diária — não é loja para clientes. Moeda: real brasileiro (R$, formato pt-BR). Fuso horário: America/Sao_Paulo. Use banco de dados real e persistente (Supabase) com login simples de um único usuário/dono; nada de dados apenas em memória. Visual limpo, rápido, fácil de usar com uma mão, cores quentes (caramelo, marrom e bege), botões grandes.

O app tem TRÊS fluxos conectados: MATERIAIS → PRODUÇÃO (fornada) → VENDAS (valor final do dia).

=== MÓDULO 1: MATERIAIS / ESTOQUE ===
- Cadastro de materiais: nome, unidade (g, kg, un, cm), estoque atual, estoque mínimo e custo por unidade.
- Movimentações: entrada (compra) e saída/ajuste manual, com data, quantidade e motivo, com histórico.
- Arqueo (conferência) de estoque: o usuário digita a quantidade real contada; o sistema mostra o teórico, a diferença e ajusta o estoque para o real.
- ALERTA automático com semáforo (verde ok, amarelo perto do mínimo, vermelho abaixo): o estoque mínimo de cada material deve ser o consumo de 1 fornada, assim o alerta avisa quando não dá mais uma fornada inteira.

=== MÓDULO 2: PRODUÇÃO (por FORNADA) ===
- Existe UM produto: "Pacote de alfajores (3 un)" — cada pacote tem 3 alfajores (6 tapinhas).
- A receita é POR FORNADA (lote), não por unidade. Itens fixos por fornada: Açúcar 100 g · Amido de milho 300 g · Farinha de trigo 350 g · Margarina 50% lipídios 400 g · Ovo 1 un · Doce de leite 600 g · Coco ralado 100 g. Itens POR PACOTE produzido: Saquinho plástico 1 un · Fitilho 10 cm.
- Tela "Produção": o usuário informa a DATA e a QUANTIDADE DE PACOTES PRODUZIDOS naquela fornada (campo livre e obrigatório; rendimento de referência: pelo menos 30 pacotes, sem máximo fixo; avisar se ficar abaixo de 30). Ao confirmar: (a) baixar do estoque os itens fixos da fornada + saquinho e fitilho multiplicados pelos pacotes produzidos; (b) somar os pacotes produzidos ao estoque de "pacotes prontos". Se faltar material, avisar mas permitir registrar, deixando o alerta visível. Permitir excluir uma produção, revertendo todas as baixas e os pacotes prontos.
- A VENDA NUNCA baixa materiais. Material só baixa na produção (unidade de desconto = fornada).

=== MÓDULO 3: VENDAS — VALOR FINAL DO DIA ===
- NÃO existe PDV de venda por venda. A tela "Vendas" registra UMA vez por dia o fechamento de vendas do dia, com 2 dados:
  1) QUANTIDADE DE PACOTINHOS VENDIDOS no dia → baixa o estoque de pacotes prontos (avisar se vender mais do que há prontos, mas permitir).
  2) DINHEIRO ARRECADADO no dia, dividido em 3 campos: Pix (R$), Dinheiro (R$), e Falta pagar (R$ — vendido mas ainda não pago, fica como "a receber", separado do dinheiro em caixa).
- Total vendido do dia = Pix + Dinheiro + Falta pagar. Dinheiro em caixa do dia = Pix + Dinheiro.
- Permitir editar/excluir o lançamento do dia (excluir devolve os pacotinhos ao estoque de prontos).
- Despesas do dia: descrição e valor.
- FECHAMENTO do dia: total vendido, Pix, dinheiro, falta pagar (a receber), despesas, esperado em caixa (Pix + dinheiro − despesas), valor contado pelo usuário e diferença. Ao fechar, o dia salva e só edita reabrindo.

=== METAS E RELATÓRIOS ===
- Meta diária configurável em R$ e em pacotinhos vendidos (com opção de meta por dia da semana).
- INÍCIO: vendido hoje (R$) e pacotinhos vendidos hoje vs. metas, com barras de progresso, % e quanto falta; pacotes prontos disponíveis; pacotes produzidos hoje; alertas de material. Semáforo da meta: vermelho < 70%, amarelo 70–99%, verde ≥ 100%.
- Relatórios semana (seg–dom) e mês: meta acumulada vs. real (R$ e pacotinhos), gráfico de barras por dia, total de falta pagar (a receber) no período, ticket médio por pacotinho (total vendido ÷ pacotinhos), % de dias que bateram a meta.

=== TELAS ===
1. Início (metas do dia, pacotes prontos, alertas). 2. Produção (registrar fornada). 3. Vendas (valor final do dia). 4. Materiais (semáforo, entradas, arqueo). 5. Produto e Receita da fornada (editável). 6. Fechamento e Relatórios. 7. Configurações (metas).

=== DADOS INICIAIS REAIS (já cadastrar, tudo editável) ===
Materiais com estoque das compras: Açúcar 1000 g (mín. 100 g) · Amido de milho 1000 g (mín. 300 g) · Farinha de trigo 1000 g (mín. 350 g) · Margarina 50% lipídios 1000 g (mín. 400 g) · Ovo 12 un (mín. 1 un) · Doce de leite 5000 g (mín. 600 g) · Coco ralado 120 g (mín. 100 g) · Saquinho plástico 100 un (mín. 30 un) · Fitilho 3000 cm (mín. 300 cm). Produto "Pacote de alfajores (3 un)" com a receita da fornada acima; preço de venda do pacote fica R$ 0 para o dono definir depois. Custos das compras ficam R$ 0, editáveis.

=== REGRAS FINAIS ===
Toda exclusão pede confirmação. Valores em R$ com 2 casas. Datas em pt-BR. Entregue o MVP completo funcionando de ponta a ponta; se precisar escolher um detalhe não especificado, escolha o mais simples e siga sem perguntar.
```

## Como usar
1. Colar tudo que está dentro do bloco no Lovable, de uma vez.
2. Testar nesta ordem: conferir os materiais carregados → registrar uma produção (ex.: 32 pacotes) e conferir as baixas → lançar as vendas do dia (pacotinhos + Pix/dinheiro/falta pagar) e conferir pacotes prontos e totais → fazer o fechamento.
3. Correções: uma por vez, descrevendo só o erro.
