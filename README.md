# Caderno do aporte

A conta da aula é direta. O salário de exemplo é R$ 2.000, então 30% daria R$ 600 por mês. Só que eu não consigo investir 600. Consigo investir 200. A planilha existe pra mostrar essa diferença, sem eu ficar refazendo conta na mão.

Arquivo: `planilha/caderno-fii.xlsx`. Abre no Excel e no LibreOffice. O salário não é o meu.

## Onde está cada resposta

Tudo na aba **Caderno**. Célula branca eu digito. Célula cinza a planilha calcula.

No bloco verde, **Investimento mensal**, ficam as cinco perguntas:

- quanto por mês: R$ 200
- por quantos anos: 10
- taxa ao mês: 1,08%
- patrimônio: R$ 48.691,53
- dividendo no mês: R$ 292,15

Embaixo eu abri o patrimônio em duas linhas, porque o número sozinho engana. Entrou de fato R$ 24.000 (200 vezes 120 meses). O resto, R$ 24.691,53, é juro. A taxa nominal, sem inflação.

O bloco **Cenários** repete isso em 2, 5, 10, 20 e 30 anos. Do lado tem a mesma conta com os R$ 600. Aí fica visível o que eu deixo na mesa quando aporto 200 em vez da sugestão.

O bloco amarelo **Divisão por perfil** reparte esses 200 entre seis tipos de FII. Troco o perfil na lista e a divisão muda. Se a soma não der 100%, ou o valor não bater com o aporte, a conferência marca `quebra`. No exemplo, marca `fecha`.

## Como a conta foi feita

O patrimônio é a função `VF`. No arquivo ela está salva como `FV`, que é o nome interno do Excel. No LibreOffice em português aparece `VF`. Eu passei a taxa mensal, os anos vezes 12, e o aporte negativo. Sem valor presente. O dividendo não entra nessa fórmula: é o patrimônio vezes o rendimento da carteira, 0,60% no exemplo.

Pra não perder a taxa quando eu arrasto o cenário pros outros anos, troquei a célula por nome: `salario`, `rendimento_carteira`, `sugestao_investimento`, `aporte`, `qtd_anos`, `taxa_mensal` e `patrimonio`. O nome fica preso na célula. Arrastar não leva ele junto.

A divisão usa `PROCV` na aba **alocacao**. Cada linha é um par perfil e tipo, com uma chave tipo `Moderado-TIJOLO`. A tela monta a mesma chave e busca o percentual. O último argumento é falso, pra casar a chave inteira.

A régua eu montei, não copiei a do Felipão, e não é recomendação. Fui do mais previsível pro mais cíclico.

Conservador fica em papel 45%, tijolo 35%, híbridos 10%, FOFs 10%. Desenvolvimento e hotelaria ficam zerados.

Moderado abre um pouco: papel 25%, tijolo 30%, híbridos 15%, FOFs 10%, desenvolvimento 12%, hotelaria 8%.

Agressivo joga o peso no fim: papel 10%, tijolo 15%, híbridos 10%, FOFs 10%, desenvolvimento 30%, hotelaria 25%.

Os três fecham em 100%.

## O que eu mudei na planilha da aula

A tela responde as mesmas perguntas e o exemplo é o da aula (200 por mês, 10 anos, 1,08%). O resto eu fiz do meu jeito: o nome é Caderno do aporte, aparece principal e juro, os cenários comparam 200 com 600, a tabela de percentual é outra, e tem a célula de conferência.

## Prints

A mesma simulação, só muda o perfil.

![Moderado](docs/prints/perfil-moderado.png)

![Conservador](docs/prints/perfil-conservador.png)
