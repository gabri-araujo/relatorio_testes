# Relatório de Teste - Projeto "Devs do RN" - 11-08-2026

## Módulo Cadastro de associados
## CASO DE TESTE 1 - CADASTRO PADRÃO

Descrição: validação do cadastro básico pelo gerente. <br>
1. Dados utilizados: <br>
- Nome: João Silva Oliveira <br>
- E-mail: joaosilvaoliveira@gmail.com <br>
- CPF: 12345678910 <br>
- Data de filiação: 08/08/2000 <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro do associado deverá ser criado com sucesso.

3. Status final: <br>
✅APROVADO

4. Evidência:

<img width="1919" height="1047" alt="image" src="https://github.com/user-attachments/assets/7f6fd414-39b5-447c-8d7a-264163ad7fa8" />

## CASO DE TESTE 2 - OBRIGATORIEDADE DOS CAMPOS

Descrição: validação da obrigatoriedade dos campos na hora do cadastro. <br>
1. Dados utilizados: <br>
- Nome: sem preencher <br>
- E-mail: sem preencher <br>
- CPF: sem preencher <br>
- Data de filiação: sem preencher <br>
2. Resultados esperados:
- o sistema não deverá aceitar o cadastro sem o preenchimento dos campos;
- sem mudanças no banco de dados.

3. Status final: <br>
✅APROVADO

4. Evidências:

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/e6196ce2-49e6-44e1-bdab-6b2ef10ea506" />

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/87695f1a-1791-4092-88d9-80f96a456068" />

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/19a846d2-8aad-470f-a61d-05eb5084f7ad" />

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/6dafa006-a871-43dc-97b8-a7886b55b8e7" />

## CASO DE TESTE 3 - DUPLICIDADE DOS CAMPOS

Descrição: validação da duplicidade dos campos na hora do cadastro. <br>
1. Etapas: <br>
- Associado já cadastrado no sistema;
- Utilizar os mesmos dados de CPF e e-mail do associado já criado.
2. Resultados esperados:
- o sistema não deverá aceitar o cadastro com duplicidade de CPF e e-mail.

3. Status final: <br>
✅APROVADO

4. Evidência:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/b5305793-2f1c-44fb-8b0b-7fdf5f005921" />

## CASO DE TESTE 4 - FORMATAÇÃO DO CAMPO CPF

Descrição: validação formatação (11 dígitos) do campo CPF. <br>
1. Etapas: <br>
- testar com menos de 11 dígitos;
- testar com mais de 11 dígitos;
- testar com caracteres especiais (@#$%&*);
- testar com letras.
2. Resultado esperado:
- o sistema não deverá aceitar o cadastro.

3. Status final: <br>
❌NÃO APROVADO

4. Motivo: não aceita caracteres especiais, letras, mais de 11 dígitos mas aceita menos de 11 dígitos

5. Evidência:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/1ce0b5cf-5a18-47aa-b535-7259bb4ac025" />

## CASO DE TESTE 5 - DATA DE FILIAÇÃO POSTERIOR
Descrição: validação do campo data de filiação diferente de anterior ou dia atual. <br>
1. Etapa: <br>
- acrescentar um dia a mais em relação ao dia da execução desse caso de teste.
2. Resultado esperado:
- o sistema não deverá aceitar o cadastro de data posterior.

3. Status final: <br>
❌NÃO APROVADO

4. Motivo: o campo aceita data posterior em relação a data atual.

5. Evidências:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/5acc478a-64cb-4b07-bc8a-7261ea183cbc" />

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/3da7c850-eb30-412e-a76f-839829276ca6" />

## Módulo Cadastro de anuidades
## CASO DE TESTE 6 - CADASTRO DE ANUIDADES PADRÃO

Descrição: validação do cadastro básico pelo gerente. <br>
1. Dados utilizados: <br>
- Ano: 2026 <br>
- Valor: 150 <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro da anuidade deverá ser criada com sucesso.

3. Status final: <br>
✅APROVADO

4. Evidência: 

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/ee447afa-38f2-4c91-809a-e1bcb5e309d9" />

## CASO DE TESTE 7 - EDIÇÃO DO VALOR

Descrição: validação da edição pelo gerente. <br>
1. Etapas: <br>
- Entrar na edição de um ano já cadastrado; <br>
- Editar o valor para o ano em questão. <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de sucesso;
- no banco de dados o registro para o ano em questão deverá ser atualizado com o novo valor preenchido.

3. Status final: <br>
✅APROVADO

4. Evidência: 

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/abfad4c3-5035-4a43-bcae-14b23f3e8207" />

## CASO DE TESTE 8 - CADASTRO DE ANUIDADE PARA ANO EXISTENTE

Descrição: validação do cadastro de anuidade para um ano já existente no sistema. <br>
1. Etapa: <br>
- Realizar o cadastro de anuidade para um ano já existente, exemplo: 2020. <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de erro pois não poderá cadastrar um ano de exercício que já existe;
- para uma atualização do valor deverá usar a edição do ano em questão.

3. Status final: <br>
✅APROVADO

4. Evidência:

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/fea91e13-68bd-4c03-ad56-33bfa86ca7f0" />

## CASO DE TESTE 9 - CADASTRO DE VALORES NEGATIVOS

Descrição: validação do cadastro de valores e ano com o sinal de negativo (-). <br>
1. Etapas: <br>
- Seguir o fluxo de cadastro de ano e valor;
- Usar o símbolo de negativo (-) em ambos os campos. <br>
2. Resultados esperados:
- deverá retornar uma mensagem  de erro pois não poderá aceitar dados negativos para esse fluxo.

3. Status final: <br>
✅APROVADO

4. Evidência:

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/9456022b-8b86-41ac-9851-c427440f3f85" />

## Módulo Cobrança das anuidades do associado
## CASO DE TESTE 10 - ASSOCIADO FILIADO NO INÍCIO DO ANO ATUAL (2026)

Descrição: validação do reconhecimento do ano corrente para afiliado que entrou no sistema no início do ano de 2026. <br>
1. Etapas: <br>
- Associado: X; <br>
- Data de filiação: 01/01/2026. <br>
2. Resultado esperado:
- o sistema deverá reconhecer o ano corrente para anuidade somente de 2026.

3. Status final: <br>
✅APROVADO

4. Evidências:

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/e6d54c11-067f-4efb-a9b0-f354630f164d" />

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/a0b1e274-3308-47cc-b057-5fb2d43ba93f" />

## CASO DE TESTE 11 - ASSOCIADO FILIADO NO ANO PASSADO (2025)

Descrição: validação do reconhecimento do ano corrente para afiliado que entrou no sistema no meio do ano de 2025. <br>
1. Etapas: <br>
- Associado: Y; <br>
- Data de filiação: 10/07/2025. <br>
2. Resultado esperado:
- o sistema deverá reconhecer os anos de 2025 e 2026 para as anuidades.

3. Status final: <br>
✅APROVADO

4. Evidências:

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/b20d17f8-ce9b-4a10-a1b1-daa718c1912d" />

<img width="1919" height="1052" alt="image" src="https://github.com/user-attachments/assets/8813154e-8f65-44c3-9008-61515cc67c4d" />

## CASO DE TESTE 12 - ASSOCIADO FILIADO RECENTEMENTE

Descrição: validação do reconhecimento do ano corrente para afiliado que entrou no sistema no meio do ano de 2025. <br>
1. Etapas: <br>
- Associado: Z; <br>
- Data de filiação: 08/08/2026. <br>
2. Resultado esperado:
- o sistema deverá reconhecer o ano de 2026 para a anuidade mas deve considerar um exercício em atraso 90 dias após a data de filiação.

3. Status final: <br>
✅APROVADO

4. Evidências:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/fb543912-ef61-449b-8a78-60f708abcf45" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/d50d6123-2543-48fe-82ad-d15285b6746c" />

## Módulo "Pagamento"/"Checkout"
## CASO DE TESTE 13 - COBRANÇA UM DIA APÓS DO VENCIMENTO DA ANUIDADE

Descrição: validação do comportamento da cobrança caso a data de vencimento seja um dia após o atual. <br>
1. Etapas: <br>
- Criar ou editar um vencimento para 07/08/2026; <br>
- Data atual no exemplo: 06/08/2026. <br>
2. Resultados esperados:
- não deverá considerar a anuidade como vencida;
- não haverá cobrança de juros;
- sem categorizar o associado como inadimplente.

3. Status final: <br>
✅APROVADO

4. Evidências: 

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/584c15f9-ea56-405f-b48c-8ade1a8e4453" />

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/4edbc7fe-c4d7-4efd-bc8c-ac6851f44768" />

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/a98065a8-8b61-48b9-8e4e-74934a8c4377" />


## CASO DE TESTE 14 - COBRANÇA UM DIA ANTES DO VENCIMENTO DA ANUIDADE

Descrição: validação do comportamento da cobrança caso a data de vencimento seja um dia antes do atual. <br>
1. Etapas: <br>
- Criar ou editar um vencimento para 06/08/2026; <br>
- Data atual no exemplo: 07/08/2026. <br>
2. Resultados esperados:
- deverá considerar a anuidade como vencida;
- haverá cobrança de juros;
- categorizar o associado como inadimplente.

3. Status final: <br>
✅APROVADO

4. Evidências:

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/4fad5580-2bb8-46a2-b5bc-8254b53b9e54" />

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/94355f94-e8f9-47dc-9f42-89679cab7cc7" />


## CASO DE TESTE 15 - COBRANÇA NO DIA DO VENCIMENTO DA ANUIDADE

Descrição: validação do comportamento da cobrança seja no dia do vencimento. <br>
1. Etapas: <br>
- Criar ou editar um vencimento para 07/08/2026; <br>
- Data atual no exemplo: 07/08/2026. <br>
2. Resultados esperados:
- não deverá considerar a anuidade como vencida;
- não haverá cobrança de juros;
- sem categorizar o associado como inadimplente.

3. Status final: <br>
✅APROVADO

4. Evidências:

<img width="1919" height="1053" alt="image" src="https://github.com/user-attachments/assets/43e792d0-47ba-4d9a-b64c-10a0544fb469" />

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/367620aa-3a03-4fe7-b4ff-0f66549902a8" />

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/cd054d86-b440-4ca3-99b6-d26395345d27" />

## CASO DE TESTE 16 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE SEM ATRASO

Descrição: validação do comportamento da cobrança dos juros caso ela não esteja em atraso. <br>
1. Etapa: <br>
- Criar ou editar um associado sem anuidade em atraso. <br>
2. Resultados esperados:
- deverá considerar somente a anuidade;
- não haverá cobrança de juros.

3. Status final: <br>
✅APROVADO

4. Evidência: 

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/a98065a8-8b61-48b9-8e4e-74934a8c4377" />

## CASO DE TESTE 17 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM UM MÊS DE ATRASO

Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 1 mês. <br>
1. Etapa: <br>
- Criar ou editar um associado com anuidade em atraso por 1 mês (anuidade a R$100,00). <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- haverá cobrança de juros de R$1,00.

3. Status final: <br>
❌NÃO APROVADO

4. Motivo: não está sendo cobrado juros em anuidades atrasadas.

5. Evidência:

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/8f7c9dff-93ca-4baa-a2dc-2cf062c15a31" />

## CASO DE TESTE 18 - CONFERÊNCIA DO CÁLCULO DOS JUROS PARA ANUIDADE COM 5 MESES DE ATRASO

Descrição: validação do comportamento da cobrança dos juros caso ela esteja em atraso por 5 meses (anuidade a R$100,00). <br>
1. Etapa: <br>
- Criar ou editar um associado com anuidade em atraso por 5 meses. <br>
2. Resultados esperados:
- deverá considerar a anuidade vigente;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- haverá cobrança de juros de R$5,00.

3. Status final: <br>
❌NÃO APROVADO

4. Motivo: mesma questão do Caso de Teste 17.

## CASO DE TESTE 19 - CONFERÊNCIA DO CHECKOUT DE ASSOCIADO INADIMPLENTE 

Descrição: validação do comportamento do checkout para associado inadimplente que nunca pagou. <br>
1. Etapa: <br>
- Criar ou editar um associado com anuidades nunca pagas, por exemplo desde o ano corrente de 2023. <br>
2. Resultados esperados:
- o checkout deverá retornar as anuidades referentes aos anos 2024, 2025 e 2026;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- o checkout assim deve retornar o total devido.

3. Status final: <br>
❌NÃO APROVADO

4. Motivo: apesar de mostrar corretamente as anuidades em aberto e o total devido não está sendo cobrado os juros na hora de pagar, está cobrando só o valor referente às anuidades. Com isso, mesma questão dos Casos de Teste 17 e 18.

## CASO DE TESTE 20 - CONFERÊNCIA DO CHECKOUT DE ASSOCIADO COM ANUIDADE PAGA 

Descrição: validação do comportamento do checkout para associado que pagou uma anuidade. <br>
1. Etapa: <br>
- Criar ou editar um associado com uma anuidade paga, por exemplo do ano corrente de 2024 estando em 2026. <br>
2. Resultados esperados:
- o checkout deverá retornar as anuidades referentes aos anos 2025 e 2026;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros;
- o checkout assim deve retornar o total devido.

3. Status final: <br>
✅APROVADO

4. Evidência: 

<img width="1919" height="1051" alt="image" src="https://github.com/user-attachments/assets/79ed3707-300a-4cdd-a2d7-0d1afd70e48c" />

## CASO DE TESTE 21 - CONFERÊNCIA DO CHECKOUT DE ASSOCIADO COM ANUIDADE PAGA PARCIALMENTE

Descrição: validação do comportamento do checkout para associado que pagou uma parte da anuidade. <br>
1. Etapa: <br>
- Criar ou editar um associado com uma anuidade paga parcialmente, por exemplo do ano corrente de 2026. <br>
2. Resultado esperado:
- o checkout deverá retornar a pendência do resultado restante devido;
- deverá discriminar no banco de dados separadamente os valores pagos de anuidade e de juros.

3. Status final: <br>
✅APROVADO

4. Evidência: 

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/8eac6ff8-f568-4926-bafc-96fe8ab57ce8" />

------------------------------------------------------------------------------------------------------------

# Extras (módulos/telas não contempladas no plano de teste inicial)
## Módulo Listagem de associados
## CASO DE TESTE 1 - CONFERÊNCIA DA LISTAGEM DE ASSOCIADOS

Descrição: tentativa de filtragem de associados usando os dados já existentes.
1. Etapa: <br>
- Utilizar algum dado de um associado já cadastrado no sistema.
2. Resultado esperado:
- retorno dos dados que correspondem a filtragem.

3. Status final: <br>
✅APROVADO

4. Evidência:

<img width="1919" height="1050" alt="image" src="https://github.com/user-attachments/assets/ea168c43-84d4-402d-b9ee-791a633e27ca" />

## CASO DE TESTE 2 - CONFERÊNCIA DO FUNCIONAMENTO DOS BOTÕES

Descrição: validação do funcionamento dos campos.
1. Etapas: <br> 
- Clicar no botão Filtrar;
- Clicar no botão Limpar.
2. Resultado esperado:
- funcionamento correto dos campos.

3. Status final: <br>
❌NÃO APROVADO

4. Motivo: ao clicar no botão de Limpar retornou um erro 404.

5. Evidência:

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/cd80806c-2892-4c3d-9800-6af3e3a0f87c" />

## Módulo Geração de Cobrança
## CASO DE TESTE 3 - CONFERÊNCIA DO RETORNO NA GERAÇÃO PARA TODOS OS ASSOCIADOS

Descrição: validação do retorno dos dados para o fluxo de geração para todos os associados.
1. Etapas:
- Clicar em Gerar Para Todos Associados;
- Escolher um ano em Ano da Anuidade, ex: 2025;
- Data de Vencimento: 12/08/2026.
2. Resultado esperado:
- deverá ser registrado cobranças de anuidades para todos os associados que se enquadram aos parâmetros usados.

3. Status final: <br>
✅APROVADO

4. Evidências:
   
<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/b3e9dba1-49a0-445f-9784-d020e402fa13" />

<img width="1919" height="1049" alt="image" src="https://github.com/user-attachments/assets/156609d5-00fa-49b0-ab2c-1de5087a867d" />

<img width="1919" height="1047" alt="image" src="https://github.com/user-attachments/assets/169c7e99-bef4-4cc6-84bf-161c75889ba9" />

<img width="1919" height="1046" alt="image" src="https://github.com/user-attachments/assets/7701630a-fb1d-4b97-af29-690a4546a52b" />

<img width="1919" height="1048" alt="image" src="https://github.com/user-attachments/assets/f97f6422-49b1-4619-935d-168c20cdd42a" />

------------------------------------------------------------------------------------------------------------

# Melhorias
## Módulo Cadastro de associados
- Adição de um botão de Limpar.

## Módulo de Anuidade
- O horário da coluna Data de Cadastro está incorreta, está a 3 horas a frente do horário atual após criar um registro;
- Ao clicar no botão de Editar seria interessante abrir uma janela popup para edição do valor, pois no fluxo atual ele preenche os campos na tela seguindo o mesmo fluxo de cadastro, podendo deixar o usuário confuso.

## Módulo "Pagamento"/"Checkout"
- Para pagamentos em que o vencimento é igual ao dia atual em questão, acredito que deveria categorizar como em Aberta, não como Vencida. Somente ao virar o dia deveria categorizar como Vencida (após 23:59).
