# Relatório de Teste - Projeto "Devs do RN" - 11-08-2026

## Módulo Cadastro de associados
## CASO DE TESTE 1 - CADASTRO PADRÃO

- Descrição: validação do cadastro básico pelo gerente. <br>
1. Dados utilizados: <br>
Nome: João Silva Oliveira <br>
E-mail: joaosilvaoliveira@gmail.com <br>
CPF: 12345678910 <br>
Data de filiação: 08/08/2000 <br><br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro do associado deverá ser criado com sucesso.

Status final: <br>
✅APROVADO

Evidência:

<img width="1919" height="1047" alt="image" src="https://github.com/user-attachments/assets/7f6fd414-39b5-447c-8d7a-264163ad7fa8" />


## CASO DE TESTE 2 - OBRIGATORIEDADE DOS CAMPOS
- Descrição: validação da obrigatoriedade dos campos na hora do cadastro. <br>
1. Dados utilizados: <br>
Nome: sem preencher <br>
E-mail: sem preencher <br>
CPF: sem preencher <br>
Data de filiação: sem preencher <br><br>
2. Resultados esperados:
- o sistema não deverá aceitar o cadastro sem o preenchimento dos campos;
- sem mudanças no banco de dados.

Status final: <br>
✅APROVADO

Evidência:

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/e6196ce2-49e6-44e1-bdab-6b2ef10ea506" />

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/87695f1a-1791-4092-88d9-80f96a456068" />

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/19a846d2-8aad-470f-a61d-05eb5084f7ad" />

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/6dafa006-a871-43dc-97b8-a7886b55b8e7" />


## CASO DE TESTE 3 - DUPLICIDADE DOS CAMPOS
- Descrição: validação da duplicidade dos campos na hora do cadastro. <br>
1. Etapas: <br>
- Associado já cadastrado no sistema;
- Utilizar os mesmos dados de CPF e e-mail do associado já criado.
2. Resultados esperados:
- o sistema não deverá aceitar o cadastro com duplicidade de CPF e e-mail.

Status final: <br>
✅APROVADO

Evidência:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/b5305793-2f1c-44fb-8b0b-7fdf5f005921" />


## CASO DE TESTE 4 - FORMATAÇÃO DO CAMPO CPF
- Descrição: validação formatação (11 dígitos) do campo CPF. <br>
1. Etapas: <br>
- testar com menos de 11 dígitos;
- testar com mais de 11 dígitos;
- testar com caracteres especiais (@#$%&*);
- testar com letras.
2. Resultado esperado:
- o sistema não deverá aceitar o cadastro.

Status final: <br>
❌NÃO APROVADO

Motivo: não aceita caracteres especiais, letras, mais de 11 dígitos mas aceita menos de 11 dígitos

Evidência:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/1ce0b5cf-5a18-47aa-b535-7259bb4ac025" />

## CASO DE TESTE 5 - DATA DE FILIAÇÃO POSTERIOR
- Descrição: validação do campo data de filiação diferente de anterior ou dia atual. <br>
1. Etapa: <br>
- acrescentar um dia a mais em relação ao dia da execução desse caso de teste.
2. Resultado esperado:
- o sistema não deverá aceitar o cadastro de data posterior.

Status final: <br>
❌NÃO APROVADO

Motivo: o campo aceita data posterior em relação a data atual.

Evidência:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/5acc478a-64cb-4b07-bc8a-7261ea183cbc" />

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/3da7c850-eb30-412e-a76f-839829276ca6" />



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
Associado: Z <br>
Data de filiação: 08/08/2026 <br>
2. Resultado esperado:
- o sistema deverá reconhecer o ano de 2026 para a anuidade mas deve considerar um exercício em atraso 90 dias após a data de filiação.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## Módulo "Pagamento"/"Checkout"
## CASO DE TESTE 13 - COBRANÇA UM DIA APÓS DO VENCIMENTO DA ANUIDADE

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

- Descrição: validação do comportamento da cobrança caso a data de vencimento seja um dia anos o atual. <br>
1. Etapas: <br>
Criar ou editar um vencimento para 06/08/2026 <br>
Data atual no exemplo: 07/08/2026 <br>
2. Resultados esperados:
- deverá considerar a anuidade como vencida;
- haverá cobrança de juros;
- categorizar o associado como inadimplente.

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

## CASO DE TESTE 16 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE SEM ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela não esteja em atraso. <br>
1. Etapa: <br>
Criar ou editar um associado sem anuidade em atraso <br>
2. Resultados esperados:
- deverá considerar somente a anuidade;
- não haverá cobrança de juros.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 17 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM UM MÊS DE ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 1 mês. <br>
1. Etapa: <br>
Criar ou editar um associado com anuidade em atraso por 1 mês (anuidade a R$100,00). <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- haverá cobrança de juros de R$1,00.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 18 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM 5 MESES DE ATRASO

- Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 5 meses (anuidade a R$100,00). <br>
1. Etapa: <br>
Criar ou editar um associado com anuidade em atraso por 5 meses. <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- haverá cobrança de juros de R$5,00.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 19 - CONFERÊNCIA DO CHECKOUT DE ASSOCIADO INADIMPLENTE 

- Descrição: validação do comportamento do checkout para associado inadimplente que nunca pagou. <br>
1. Etapa: <br>
Criar ou editar um associado com anuidades nunca pagas, por exemplo desde o ano corrente de 2023. <br>
2. Resultados esperados:
- o checkout deverá retornar as anuidades referentes aos anos 2024, 2025 e 2026;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- o checkout assim deve retornar o total devido.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 20 - CONFERÊNCIA DO CHECKOUT DE ASSOCIADO COM ANUIDADE PAGA 

- Descrição: validação do comportamento do checkout para associado que pagou uma anuidade. <br>
1. Etapa: <br>
Criar ou editar um associado com uma anuidade paga, por exemplo do ano corrente de 2024 estando em 2026. <br>
2. Resultados esperados:
- o checkout deverá retornar as anuidades referentes aos anos 2025 e 2026;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- o checkout assim deve retornar o total devido.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

## CASO DE TESTE 21 - CONFERÊNCIA DO CHECKOUT DE ASSOCIADO COM ANUIDADE PAGA PARCIALMENTE

- Descrição: validação do comportamento do checkout para associado que pagou uma parte da anuidade. <br>
1. Etapa: <br>
Criar ou editar um associado com uma anuidade paga parcialmente, por exemplo do ano corrente de 2026. <br>
2. Resultado esperado:
- o checkout deverá retornar a pendência do resultado restante devido;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros.

Status final: <br>
✅APROVADO <br> ou <br>
❌NÃO APROVADO

------------------------------------------------------------------------------------------------------------

# Melhorias
## Módulo Cadastro de associados
Botão de Limpar


## Módulo Cadastro de anuidades
asdadas
## Módulo Cobrança das anuidades do associado
asdasda
## Módulo "Pagamento"/"Checkout"
