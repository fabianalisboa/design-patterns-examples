

Este repositório contém exemplos e explicações de diversos padrões de design de software, como o padrão Prototype, Factory, Singleton, entre outros. O objetivo é ajudar desenvolvedores a entender e implementar esses padrões no seu dia a dia.


1. [Introdução aos Padrões de Design](#introdução-aos-padrões-de-design)
2. [Padrão Prototype](#padrão-prototype)
    - [O que é?](#o-que-é)
    - [Como Funciona?](#como-funciona)
    - [Vantagens e Desvantagens](#vantagens-e-desvantagens)
    - [Exemplo de Código](#exemplo-de-código)
3. [Outros Padrões](#outros-padrões)
    - [Factory](#factory)
    - [Singleton](#singleton)
4. [Conclusão](#conclusão)


Padrões de design são soluções recorrentes para problemas comuns enfrentados no desenvolvimento de software. Eles não são soluções específicas, mas sim abordagens testadas e comprovadas que podem ser adaptadas a diferentes cenários. O uso de padrões de design aumenta a reutilização do código e facilita a manutenção de sistemas complexos.


O padrão Prototype é um padrão de criação que permite a criação de novos objetos através da cópia de um objeto existente, em vez de criar um novo objeto do zero. Esse padrão é útil quando a criação de objetos é complexa ou dispendiosa.


Em um cenário de desenvolvimento de software, quando você possui um objeto muito complexo para ser recriado repetidamente, o padrão Prototype permite que você crie novas instâncias do objeto simplesmente clonando o protótipo, o que economiza recursos e tempo.


Aqui está um exemplo em Python que demonstra o uso do Padrão Prototype:

```python
from copy import deepcopy

class Produto:
    def __init__(self, nome, id):
        self.nome = nome
        self.id = id

    def clone(self):
        return deepcopy(self)

    def __str__(self):
        return f"Produto(nome={self.nome}, id={self.id})"

produto1 = Produto("Produto A", 1)
produto_clone = produto1.clone()

print(produto1)
print(produto_clone)
