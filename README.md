# Simulador Pro Soluto

Aplicação web estática, responsiva e sem dependência de Excel. Pode ser publicada diretamente no GitHub Pages.

## Recursos

- Seleção de empreendimento com datas de obra.
- Políticas Diamante, Ouro, Prata, Bronze e Aço.
- Prazo limitado a 84 parcelas.
- Sinais automáticos em 30, 60 e 90 dias.
- Anuais com valor e data.
- Correção mensal de 0,5% durante a obra e 1,5% no pós-obra.
- Parcela uniforme calculada pelo valor presente com taxas variáveis, equivalente ao princípio da Tabela Price.
- Sugestão de sinal CC, mantendo sinais complementares e anuais zerados.
- Validação de comprometimento da parcela PS e comprometimento total.
- Impressão e exportação pelo navegador em PDF.

## Executar localmente

Abra `index.html` no navegador ou use um servidor local:

```bash
python3 -m http.server 8080
```

Acesse `http://localhost:8080`.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie `index.html`, `styles.css`, `app.js` e `README.md` para a raiz da branch `main`.
3. Abra **Settings > Pages**.
4. Em **Source**, escolha **Deploy from a branch**.
5. Selecione `main` e `/ (root)`.
6. Salve e aguarde a publicação.

## Configuração

Edite os arrays `projects` e `policies` no início do arquivo `app.js` para atualizar empreendimentos, datas e políticas.

## Premissas e validação

Esta versão trata **Aço** como o nome da faixa de 12%, conforme o simulador interno consultado. A sugestão do sinal CC busca reduzir o saldo residual do Pro Soluto ao percentual máximo da política. Sinais 1 a 3 e anuais são descontados do saldo antes do cálculo das mensais.

Antes de uso operacional, homologue os resultados com Gestão de Riscos e faça testes comparativos com propostas reais do simulador oficial. Datas dos empreendimentos devem ser revisadas sempre que houver atualização da curva de obra.
