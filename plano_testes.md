# Plano de Testes - Projeto "Devs do RN" - 08-08-2026

## Módulo Cadastro de associados
## CASO DE TESTE 1 - CADASTRO PADRÃO

- Descrição: validação do cadastro básico pelo gerente. <br>
1. Dados utilizados: <br>
Nome: João Silva Oliveira <br>
E-mail: joaosilvaoliveira@gmail.com <br>
CPF: 12345678910 <br>
Data de filiação: 08/08/2000 <br><br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso
- no banco de dados o registro do associado deverá ser criado com sucesso

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 2 - OBRIGATORIEDADE DOS CAMPOS
- Descrição: validação da obrigatoriedade dos campos na hora do cadastro. <br>
1. Dados utilizados: <br>
Nome: sem preencher <br>
E-mail: sem preencher <br>
CPF: sem preencher <br>
Data de filiação: sem preencher <br><br>
3. Resultados esperados:
- o sistema não deverá aceitar o cadastro sem o preenchimento dos campos
- sem mudanças no banco de dados

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO


## CASO DE TESTE 3 - DUPLICIDADE DOS CAMPOS
- Descrição: validação da duplicidade dos campos na hora do cadastro. <br>
1. Etapas: <br>
- Associado já cadastrado no sistema;
- Utilizar os mesmos dados de CPF e e-mail do associado já criado.
3. Resultados esperados:
- o sistema não deverá aceitar o cadastro com duplicidade de CPF e e-mail;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 4 - FORMATAÇÃO DO CAMPO CPF
- Descrição: validação formatação (11 dígitos) do campo CPF. <br>
1. Etapas: <br>
- testar com menos de 11 dígitos;
- testar com mais de 11 dígitos;
- testar com caracteres especiais (@#$%&*);
- testar com letras.
3. Resultado esperado:
- o sistema não deverá aceitar o cadastro;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 5 - DATA DE FILIAÇÃO POSTERIOR
- Descrição: validação do campo data de filiação diferente de anterior ou dia atual. <br>
1. Etapas: <br>
- acrescentar um dia a mais em relação ao dia da execução desse caso de teste.
3. Resultado esperado:
- o sistema não deverá aceitar o cadastro de dataposterior;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## Módulo Cadastro de anuidades
## CASO DE TESTE 6 - CADASTRO DE ANUIDADES PADRÃO

- Descrição: validação do cadastro básico pelo gerente. <br>
1. Dados utilizados: <br>
Ano: 2026 <br>
Valor: 150 <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro da anuidade deverá ser criada com sucesso.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 7 - EDIÇÃO DO VALOR

- Descrição: validação da edição pelo gerente. <br>
1. Etapas: <br>
- Entrar na edição de um ano já cadastrado <br>
- Editar o valor para o ano em questão <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro para o ano em questão deverá ser atualizado com o novo valor preenchido.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 8 - CADASTRO DE ANUIDADE PARA ANO EXISTENTE

- Descrição: validação do cadastro de anuidade para um ano já existente no sistema. <br>
1. Etapas: <br>
- Realizar o cadastro de anuidade para um ano já existente, exemplo: 2020 <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de erro pois não poderá cadastrar um ano de exercício que já existe;
- para uma atualização do valor deverá usar a edição do ano em questão.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 9 - CADASTRO DE VALORES NEGATIVOS

- Descrição: validação do cadastro de valores e ano com o sinal de negativo (-). <br>
1. Etapas: <br>
- Seguir o fluxo de cadastro de ano e valor;
- Usar o símbolo de negativo (-) em ambos os campos. <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de erro pois não poderá aceitar dados negativos para esse fluxo.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## Módulo Cobrança das anuidades do associado
## CASO DE TESTE 10 - ASSOCIADO FILIADO NO INÍCIO DO ANO ATUAL (2026)

- Descrição: validação do reconhecimento do ano corrente para afiliado que entrou no sistema no início do ano de 2026. <br>
1. Etapas: <br>
Associado: X <br>
Data de filiação: 01/01/2026 <br>
2. Resultado esperado:
- o sistema deverá reconhecer o ano corrente para anuidade somente de 2026.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 11 - ASSOCIADO FILIADO NO ANO PASSADO (2025)

- Descrição: validação do reconhecimento do ano corrente para afiliado que entrou no sistema no meio do ano de 2025. <br>
1. Etapas: <br>
Associado: Y <br>
Data de filiação: 10/07/2025 <br>
2. Resultado esperado:
- o sistema deverá reconhecer os anos de 2025 e 2026 para as anuidades.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 12 - ASSOCIADO FILIADO RECENTEMENTE

- Descrição: validação do reconhecimento do ano corrente para afiliado que entrou no sistema no meio do ano de 2025. <br>
1. Etapas: <br>
Associado: z <br>
Data de filiação: 08/08/2026 <br>
2. Resultado esperado:
- o sistema deverá reconhecer o ano de 2026 para a anuidade mas deve considerar um exercício em atraso 90 dias após a data de filiação.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## Módulo "Pagamento"/"Checkout"
## CASO DE TESTE 13 - COBRANÇA UM DIA ANTES DO VENCIMENTO DA ANUIDADE

- Descrição: validação do comportamento da cobrança caso a data de vencimento seja um dia após o atual. <br>
1. Etapas: <br>
Criar ou editar um vencimento para 07/08/2026 <br>
Data atual no exemplo: 06/08/2026 <br>
2. Resultados esperados:
- não deverá considerar a anuidade como vencida;
- não haverá cobrança de juros;
- sem categorizar o associado como inadimplente.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 14 - COBRANÇA UM DIA ANTES DO VENCIMENTO DA ANUIDADE

- Descrição: validação do comportamento da cobrança caso a data de vencimento seja um dia após o atual. <br>
1. Etapas: <br>
Criar ou editar um vencimento para 07/08/2026 <br>
Data atual no exemplo: 06/08/2026 <br>
2. Resultados esperados:
- não deverá considerar a anuidade como vencida;
- não haverá cobrança de juros;
- sem categorizar o associado como inadimplente.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 15 - COBRANÇA NO DIA DO VENCIMENTO DA ANUIDADE

- Descrição: validação do comportamento da cobrança seja no dia do vencimento. <br>
1. Etapas: <br>
Criar ou editar um vencimento para 07/08/2026 <br>
Data atual no exemplo: 07/08/2026 <br>
2. Resultados esperados:
- não deverá considerar a anuidade como vencida;
- não haverá cobrança de juros;
- sem categorizar o associado como inadimplente.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 17 - COBRANÇA UM DIA APÓS O VENCIMENTO DA ANUIDADE

- Descrição: validação do comportamento da cobrança caso ela seja após o dia do vencimento. <br>
1. Etapas: <br>
Criar ou editar um vencimento para 05/08/2026 <br>
Data atual no exemplo: 06/08/2026 <br>
2. Resultados esperados:
- deverá considerar a anuidade como vencida;
- haverá cobrança de juros;
- categorizar o associado como inadimplente.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 18 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE SEM ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela não esteja em atraso. <br>
1. Etapa: <br>
Criar ou editar um associado sem anuidade em atraso <br>
2. Resultados esperados:
- deverá considerar somente a anuidade;
- não haverá cobrança de juros;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 19 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM UM MÊS DE ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 1 mês. <br>
1. Etapa: <br>
Criar ou editar um associado com anuidade em atraso por 1 mês (anuidade a R$100,00). <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- haverá cobrança de juros de R$1,00;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 20 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM 5 MESES DE ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 5 meses (anuidade a R$100,00). <br>
1. Etapa: <br>
Criar ou editar um associado com anuidade em atraso por 5 meses. <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- haverá cobrança de juros de R$5,00;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 21 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM 5 MESES DE ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 5 meses. <br>
1. Etapa: <br>
Criar ou editar um associado com anuidade em atraso por 5 meses. <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- haverá cobrança de juros de R$5,00;

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO
