# Loja-de-Selos---MER---"Filatelia Rara"
Loja de Selos - Seleção Smartbreeder - Estágio Banco de Dados

## Entidades e atributos indentificadas:
**Selo:**\
    -Cod_indentificador\
    -Ano_emissao\
    -ValorNominal\
    -Descricao
    
**País:**\
  -Cod_pais\
  -Nome_pais

**Colecao:**\
  -Cod_colecao\
  -Nome_colecao\
  -Descricao_colecao

**Cliente:**\
  -Cod_cliente\
  -Nome_Completo\
  -Emali\
  -Endereco\
  -Telefone
  
**Compra:**\
  -Cod_compra\
  -Data_compra\
  -Valor_total\
  -Desconto
  
**Venda_cliente_loja:**\
  Cod_transacao_venda\
  -Data_venda\
  -Valor_pago
  
**Autor_desenhista:**\
  -Cod_autor\
  -Nome_autor\
  -biografia_breve\
  -Nacionalidade
  
**Lista_de_desejos:**\
  -Cod_lista_desejos\
  -Data_criacao\
  -Nome_lista

## Relaçoes das Entidades:
Selo -->(Pertence a)--> Pais >> Tipo(N:M)

Selo -->(Faz parte de)-->Colecao >> Tipo(0:N)

Cliente -->(Efetua)-->Compra >> Tipo(1:N)

Compra -->(Contem)--> Selo >> Tipo(N:M)

Cliente -->(Vende para)--> Venda_cliente_loja >> Tipo(1:N)

Venda_cliente_loja -->(adquire)--> >> Tipo(1:1)

Selo -->(Tem autoria)--> Autor_desenhista >> Tipo(N:M)

Cliente -->(Cria)--> Lista_desejos >> Tipo(1:N)
