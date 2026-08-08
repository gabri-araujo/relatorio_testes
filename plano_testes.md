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

## CASO DE TESTE 7 - EDIÇÃO DO VALOR

- Descrição: validação da edição pelo gerente. <br>
1. Etapas <br>
- Entrar na edição de um ano já cadastrado <br>
- Editar o valor para o ano em questão <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro para o ano em questão deverá ser atualizado com o novo valor preenchido.

















## Módulo Cobrança das anuidades do associado

## Módulo "Pagamento" da anuidade de um associado

## Estrutura do Banco de Dados
