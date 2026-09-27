# Estudos Realizados Sobre a Utilização do NotebookLM
Repositório criado para demonstrar a importância dos estudos em Inteligência Artificial e suas diversas aplicações. Juntando uma temática necessária para o aprendizado em aulas na universidade e tópicos aprendidos em aulas do curso da Dio para acelerar o aprendizado com IA.

O NotebookLM foi a maneira de juntar fontes e informações que demandariam uma maior quantidade de tempo para um estudo rápido, dinâmico e com uma economia de tempo para revisões.

__Tema Escolhido:__ JAVA.

__Objetivo do Estudo:__ Compreender aulas que utilizam Java como seu principal meio de aprendizado prático e teórico. Dando um foco em estrutura de dados.


**Fontes Utilizadas:**
1. <a href="https://www.kufunda.net/publicdocs/Java%20Como%20Programar%20(Paul%20Deitel%20Harvey%20Deitel)%20(z-lib.org).pdf" > Livro: Como Programar em Java</a>
2. <a href="https://www.devmedia.com.br/guia/linguagem-java/38169" > Guia Completo de Java: Aprenda a Linguagem de Programação Java </a>
3. <a href="https://www.dio.me/articles/java-para-iniciantes-tudo-o-que-voce-precisa-saber" > Java para Iniciantes: Tudo o que você precisa saber | Wallace Guimarães | Java | DIO</a>
4. <a href="https://www.kufunda.net/publicdocs/ESTRUTURA%20DE%20DADOS.pdf" >Estrutura de Dados</a>

### Perguntas para iniciar os estudos de maneira eficaz ###

1.  *Faça um resumo de como o Java é uma ótima ferramenta para entender estrutura de dados.* 
*Utilizando exemplos práticos de como iniciar os estudos de ambos tópicos. Até 300 palavras.*<br>
**Resultando:**
---
O **Java** é uma ferramenta de aprendizado excelente para estruturas de dados porque combina os princípios da **Orientação a Objetos** com a gestão transparente de memória por meio de **referências**.

### Por que aprender Estruturas de Dados com Java?

1. **Manipulação por Referências:** Em vez de exigir o gerenciamento manual de ponteiros, o Java utiliza variáveis de referência que armazenam as localizações dos objetos na memória. Isso facilita a criação de **classes autorreferenciais** (nós) para estruturar dinamicamente listas encadeadas, pilhas, filas e árvores.
2. **Do Conceitual à Produção:** O estudante pode implementar uma estrutura do zero e depois compará-la com as coleções genéricas prontas da API Java (*Java Collections Framework*).

---

### Exemplos Práticos para Iniciar os Estudos

* **1. Criando um Nó e Lista do Zero (Nível Conceitual):**
  Implemente uma classe autorreferencial `ListNode<T>` com o dado e a referência para o próximo nó:
  ```java
  class ListNode<T> {
      T data;               // Dado armazenado
      ListNode<T> nextNode; // Referência autorreferencial ao próximo nó
  }
  ```
  Ao vincular esses nós em uma classe `List<T>`, entende-se como os elementos se conectam dinamicamente na memória.

* **2. Utilizando o Java Collections Framework (Nível Prático):**
  Substitua arranjos estáticos pela classe genérica `ArrayList<T>` do pacote `java.util`, que oferece redimensionamento dinâmico:
  ```java
  List<String> lista = new ArrayList<>();
  lista.add("Java"); // Adiciona elementos dinamicamente
  ```
  Essa prática permite comparar estruturas personalizadas com alternativas predefinidas e otimizadas.

---

2. Como criar nó e lista e como isso pode ser feito por um iniciante.

* Faça um passo a passo levando em consideração um iniciante;
* Explicações simplificadas e sem termos técnicos;
* Após o passo a passo sem termos técnicos, explique como o Java faz o código funcionar introduzindo os termos de forma bem detalhada (explicação de até 200 palavras).<br>
**Resultando:**

---

### Passo a Passo Prático para Iniciantes (Sem Termos Técnicos)

Imagine uma **Lista Encadeada** como um **trem de brinquedo** formado por vários vagões conectados por ganchos ou barbantes.

---

#### **Etapa 1: Criando o Vagão (O Nó)**
A primeira coisa a fazer é criar a receita do nosso vagão. Cada vagão precisa de duas coisas: um compartimento para carregar uma carga (o número) e um barbante para engatar no vagão seguinte.

```java
class No {
    int valor;  // A carga guardada no vagão (um número inteiro)
    No proximo; // O barbante que conecta ao próximo vagão
}
```
* **Finalidade:** Definir a estrutura básica do nó. O campo `valor` armazena a informação e o campo `proximo` permite criar o elo de ligação com a próxima caixinha.

---

#### **Etapa 2: Criando a Estação (A Lista)**
A lista em si não guarda todos os vagões dentro de si. Ela funciona como uma estação com uma placa indicando onde a fila de vagões começa.

```java
class ListaEncadeada {
    No primeiro; // Placa indicando qual é o primeiro vagão da fila
}
```
* **Finalidade:** Estruturar a lista. A variável `primeiro` serve como o ponto de entrada inicial. Quando a lista é criada, essa placa começa apontando para o "vazio" (sem vagões).

---

#### **Etapa 3: Colocando um Vagão no Início da Fila**
Para adicionar um vagão no começo, nós criamos a caixinha nova, amarrarmos o barbante dela no vagão que antes era o primeiro e atualizamos a placa da estação.

```java
public void adicionarNoInicio(int novoValor) {
    No novoNo = new No();       // 1. Cria um vagão novo
    novoNo.valor = novoValor;   // 2. Coloca a carga dentro dele
    
    novoNo.proximo = primeiro;  // 3. Amarra o barbante no vagão que já estava no início
    primeiro = novoNo;          // 4. Atualiza a placa da estação para apontar para o vagão novo
}
```
* **Finalidade:** Inserir um elemento no início da lista, garantindo que o novo nó aponte para o antigo primeiro elemento e que a estação reconheça o novo nó como o começo oficial.

---

#### **Etapa 4: Lendo a Fila de Vagões**
Para ver o que está guardado, começamos da placa inicial e vamos caminhando de vagão em vagão até chegar ao final.

```java
public void mostrarLista() {
    No atual = primeiro; // Começa da placa da estação
    
    while (atual != null) { // Enquanto houver um vagão válido
        System.out.println(atual.valor); // Mostra a carga do vagão
        atual = atual.proximo;           // Segue o barbante até o próximo vagão
    }
}
```
* **Finalidade:** Percorrer a lista do início ao fim, exibindo o valor de cada nó sequencialmente até que o caminho termine.

---

### Como o Java Faz o Código Funcionar (Explicação Técnica)

No Java, o nó é implementado como uma **classe autorreferencial**, pois possui um campo de **variável de referência** (`proximo`) que aponta para um objeto do mesmo tipo. Ao executar `new No()`, a JVM realiza a **alocação dinâmica de memória** na *heap* e retorna o endereço desse objeto. 

A **Lista Encadeada** é uma estrutura de dados linear e dinâmica gerida por variáveis de referência como `primeiro` (`firstNode`) e `ultimo` (`lastNode`). Diferente de um array estático que ocupa espaços contíguos, os nós ficam distribuídos na memória e vinculados logicamente por essas referências. 

Ao inserir no início, a referência do novo nó é ajustada para o antigo primeiro nó, e a referência `primeiro` da lista é atualizada. O encerramento da estrutura é demarcado pela referência especial `null`. Quando um nó é desvinculado e perde todas as suas referências no programa, o **coletor de lixo** (*Garbage Collector*) do Java recupera e desaloca essa memória automaticamente em tempo de execução.

---

---
