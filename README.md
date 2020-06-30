# clean-code

# Origem
As técnicas do Clean Code apareceram pela primeira vez no livro “Clean Code: A Handbook of Agile Software Craftsmanship”, lançado em 2008. Ele foi escrito por Robert Cecil Martin, conhecido na comunidade como Uncle Bob. O autor atua na área de desenvolvimento desde 1970 e é um dos profissionais por trás do Manifesto Ágil, lançado em 2001.
Com seus longos anos de experiência, ele conseguiu perceber que o gargalo principal no desenvolvimento de software estava justamente na manutenção. Ou seja, um código mal escrito desde a sua primeira versão pode funcionar, mas vai gerar prejuízos enormes.

# O que é?
Clean Code é uma filosofia de desenvolvimento cuja o principal objetivo é aplicar técnicas simples que visam facilitar a escrita e leitura de um código, tornando-o de fácil compreensão e revelando a sua real intenção.

# Por quê?
A produtividade de um programador está diretamente ligada a qualidade do código em que ele trabalha. Por isso, realizar a manutenção de um software é bem mais complicado do que desenvolver um do início. Os programadores passam a maior parte do tempo lendo e entendo o código do que programando. A proporção de leitura para escrita do código é de 10:1— Essa afirmação foi feita pelo Robert C. Martin ao analisar o histórico de atividades do seu próprio editor quando estava programando.
É impossível escrever um código sem lê-lo, constantemente lemos um código antigo quando estamos criando um. Por isso, escrever um código que facilite a leitura é de suma importância. Se você quiser ser um programador melhor e mais produtivo, não há como escapar, comece escrevendo um código mais limpo.


# EXEMPLOS

## Variaveis

Use nomes de variáveis significativos e pronunciáveis
### Errado:

```JAVA
String a = new SimpleDateFormat("YYYY/MM/DD").format(new Date());
```

### Certo:

```JAVA
String dataAtual = new SimpleDateFormat("YYYY/MM/DD").format(new Date());
```

## Use o mesmo vocabulario para o mesmo tipo de variavel

### Errado:
```JAVA
  getUsuarioInfo();
  getUsuarioRegistro();
  getCliente();
```

### Correto:
```JAVA
  getUsuario();
```

## Use nomes que possam ser consultados e lembrados

Este passo é muito importante pois o livro ressalta que passsamos mais tempo lendo código do que _codando_ e por isso devemos deixar de uma forma que para quem for ler não seja doloroso.

### Errado

```JAVA
  //O que significa o 5 ?
  
  boolean podeTerMaisDependentes(){
    return pessoa.dependentes.size() > 5
  }
  ```

  ```JAVA
  boolean podeTerMaisDependentes(){
    int NUMERO_MAXIMO_DE_DEPENDENTES = 5; 
    return pessoa.dependentes.size() > NUMERO_MAXIMO_DE_DEPENDENTES
  }
  ```
