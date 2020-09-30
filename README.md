# CONSTRUÇÃO DE OBJETOS


## Contextualização

O encapsulamento das regras de negócio referente ao nascimento de um novo objeto muitas vezes escapam de onde deveriam estar e acabam vazando a responsabilidade para camadas superiores/clientes.

## Exemplo

Para ilustrar a situação, trouxemos uma situação simplificada de um cenário real de controle de estoque. O cenário consiste da necessidade de controlar estoques de produtos que possuem diferentes características. Estas características podem ser coisas mais comumns como lote, data de validação, data de  fabricação bem como cor, tamanho ou alguma outra característica associada ao produto. Além da necessidade de buscar estoques com valores específicos para característica específicas, é muito comum a necessidade de ordenar os estoques pelos valores das características. Exemplo, buscar os estoques de queijo com data de validade até 31/12/2020 ordenados pela data de validade. 
Queijo podem possuir características como lote, data de validade e data de fabricação, enquanto camisetas, outro tipo de produto, podem ter outras características.

Ilustração mais lúdica


Para atender as necessidaes apresentadas, considere que existe um cadastro de possíveis características e que estas características são associadas ao produto no momento da entrada no estoque. Para que os filtros e a ordenação do estoque aconteça da forma correta, o tipo de dado de cada característica é muito importante. Ordenar uma data como data é completamente diferente de ordenar como um texto ou como um número. Sendo assim, cada característica tem a indicação do tipo de dado referente ao seu valor que pode ser um texto, número, data e até mesmo outros tipos. Este dinamismo no tipo de dado pode acarretar em uma complexidade técnica para tratar cada tipo de dado. Sendo assim, o exemplo aqui apresentado tem o objetivo de resolver dois pontos:
* Tornar a construção do objeto transparente independente do tipo de valor
* Tornar a ordenação das informações do estoque independente do tipo de valor

Ilustração técnica mostrando característica e característica valor

Mas onde entra o enum factory e como ele pode ajudar?

Trecho de código enum factory

Tornando a construção transparente

Trecho de código mostrando o construtor estático "valor" na entidade característica

Tornando a ordenação transparente






