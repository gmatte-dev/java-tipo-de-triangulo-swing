# Verificador de Triangulos

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Swing-GUI-blue?style=for-the-badge" alt="Swing">
  <img src="https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=for-the-badge" alt="Status">
</p>

## Sobre o Projeto

Aplicacao desktop desenvolvida em **Java** com interface grafica **Swing JFrame** que verifica se tres segmentos de reta podem formar um triangulo e identifica seu tipo com base nos valores informados pelo usuario.

---

## Origem do Projeto

> Este projeto foi desenvolvido durante o **Curso de Java - 40 Horas** ministrado pelo professor **Gustavo Guanabara** no [Curso em Video](https://www.cursoemvideo.com/).

O curso oferece uma base solida em programacao Java, abordando desde conceitos fundamentais ate a criacao de interfaces graficas com Swing.

---

## Conceitos Matematicos

### Condicao de Existencia de um Triangulo

Para que tres segmentos formem um triangulo, cada lado deve ser **menor** que a soma dos outros dois:

```
|a - b| < c < a + b
|a - c| < b < a + c
|b - c| < a < b + c
```

**Ou de forma simplificada:**
- A < B + C
- B < A + C
- C < A + B

### Classificacao dos Triangulos

| Tipo | Condicao |
|------|----------|
| **Equilatero** | Todos os lados iguais (A = B = C) |
| **Isoceles** | Dois lados iguais (A = B ou A = C ou B = C) |
| **Escaleno** | Todos os lados diferentes (A =/= B =/= C) |

---

## Como Funciona

```
1. O usuario informa os valores dos tres lados (A, B e C)
2. O programa verifica se os valores formam um triangulo valido
3. Se for valido:
   - Identifica o tipo (Equilatero, Isoceles ou Escaleno)
   - Exibe o resultado na interface
4. Se nao for valido:
   - Exibe mensagem informando que nao e possivel formar um triangulo
```

---

## Funcionalidades

- [x] Entrada de tres valores (lados A, B e C)
- [x] Validacao de existencia do triangulo
- [x] Identificacao do tipo de triangulo
- [x] Interface grafica intuitiva com Swing JFrame
- [x] Mensagens claras de resultado
- [x] Validacao de entrada (apenas numeros positivos)
- [x] Botao para limpar campos e fazer nova verificacao

---

## Screenshot

```
+-----------------------------------------------+
|         VERIFICADOR DE TRIANGULOS             |
+-----------------------------------------------+
|                                               |
|   Informe os valores dos tres lados:          |
|                                               |
|   Lado A:  [    5    ]                        |
|                                               |
|   Lado B:  [    5    ]                        |
|                                               |
|   Lado C:  [    5    ]                        |
|                                               |
|            [ VERIFICAR ]                      |
|                                               |
+-----------------------------------------------+
|                                               |
|   Resultado: TRIANGULO EQUILATERO             |
|   Os tres lados sao iguais!                   |
|                                               |
+-----------------------------------------------+
|            [ LIMPAR ]                         |
+-----------------------------------------------+
```

---

## Pre-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

- **Java JDK 8** ou superior
- Uma IDE de sua preferencia (NetBeans, Eclipse, IntelliJ IDEA, VS Code)

---

## Como Executar

1. **Clone o repositorio**
   ```bash
   git clone https://github.com/seu-usuario/verificador-triangulos-java.git
   ```

2. **Acesse a pasta do projeto**
   ```bash
   cd verificador-triangulos-java
   ```

3. **Compile o projeto**
   ```bash
   javac Main.java
   ```

4. **Execute a aplicacao**
   ```bash
   java Main
   ```

> **Dica:** Se estiver usando uma IDE como NetBeans ou Eclipse, basta abrir o projeto e clicar em "Run".

---

## Estrutura do Projeto

```
verificador-triangulos-java/
|
+-- src/
|   +-- Main.java               # Classe principal
|   +-- Triangulo.java          # Logica de verificacao
|   +-- TelaTriangulo.java      # Interface Swing
|
+-- README.md
```

---

## Tecnologias Utilizadas

- **Java SE** - Linguagem de programacao
- **Swing** - Biblioteca para interface grafica
- **JFrame** - Container principal da aplicacao
- **JTextField** - Campos de entrada dos lados
- **JButton** - Botoes de acao
- **JLabel** - Exibicao de mensagens e resultados

---

## Logica de Verificacao

```java
// Verifica se pode formar triangulo
public boolean ehTriangulo(double a, double b, double c) {
    return (a < b + c) && (b < a + c) && (c < a + b);
}

// Identifica o tipo do triangulo
public String tipoTriangulo(double a, double b, double c) {
    if (a == b && b == c) {
        return "EQUILATERO";
    } else if (a == b || a == c || b == c) {
        return "ISOCELES";
    } else {
        return "ESCALENO";
    }
}
```

---

## Exemplos de Uso

| Lado A | Lado B | Lado C | Resultado |
|--------|--------|--------|-----------|
| 5 | 5 | 5 | Triangulo Equilatero |
| 5 | 5 | 3 | Triangulo Isoceles |
| 3 | 4 | 5 | Triangulo Escaleno |
| 1 | 2 | 10 | Nao forma triangulo |

---

## Aprendizados

Durante o desenvolvimento deste projeto, foram aplicados os seguintes conceitos:

- Programacao Orientada a Objetos (POO)
- Criacao de interfaces graficas com Swing
- Manipulacao de eventos (ActionListener)
- Estruturas condicionais (if/else)
- Operadores logicos (&&, ||)
- Operadores relacionais (==, <, >)
- Validacao de dados de entrada
- Tratamento de excecoes

---

## Possiveis Melhorias

- [ ] Adicionar classificacao por angulos (Acutangulo, Retangulo, Obtusangulo)
- [ ] Calcular o perimetro do triangulo
- [ ] Calcular a area do triangulo (Formula de Heron)
- [ ] Desenhar o triangulo graficamente
- [ ] Adicionar historico de verificacoes

---

## Contribuicoes

Contribuicoes sao sempre bem-vindas! Se voce tem alguma sugestao para melhorar este projeto:

1. Faca um Fork do projeto
2. Crie uma Branch para sua feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudancas (`git commit -m 'Adiciona NovaFeature'`)
4. Push para a Branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

---


## Autor

Desenvolvido durante o **Curso de Java 40 Horas** do [Curso em Video](https://www.cursoemvideo.com/)

**Professor:** Gustavo Guanabara

---

## Links Uteis

- [Curso em Video - Java](https://www.cursoemvideo.com/curso/java-basico/)
- [Documentacao Java](https://docs.oracle.com/en/java/)
- [Tutorial Swing](https://docs.oracle.com/javase/tutorial/uiswing/)
- [Condicao de Existencia de Triangulo](https://pt.wikipedia.org/wiki/Desigualdade_triangular)

---

<p align="center">
  Se este projeto te ajudou, considere dar uma estrela!
</p>
