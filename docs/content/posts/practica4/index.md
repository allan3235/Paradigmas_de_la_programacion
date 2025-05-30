
# 🧠 Práctica IV – Paradigma Lógico en Prolog


---

## 🔹 Introducción

El paradigma lógico es uno de los enfoques fundamentales en la programación declarativa. En lugar de describir paso a paso cómo debe realizarse una tarea (como en programación imperativa), el paradigma lógico se centra en **qué debe cumplirse** para que algo sea verdadero.

En este paradigma, los programas se componen de un conjunto de **hechos** y **reglas**, y el motor lógico (en este caso Prolog) se encarga de deducir las respuestas a las consultas hechas por el usuario.

Prolog (Programming in Logic) es uno de los lenguajes más representativos de este paradigma. Es utilizado ampliamente en inteligencia artificial, procesamiento de lenguaje natural, resolución de problemas lógicos, entre otros.

---

## 📌 Parte 1: Fundamentos

### ✅ Hechos (`hechos.pl`)

Los **hechos** representan afirmaciones que consideramos verdaderas dentro del sistema. Son la base del conocimiento y se representan en la forma:

```prolog
relación(objeto1, objeto2, ..., objetoN).
```

#### 📄 Código:

```prolog
cat(tom).
loves_to_eat(jorge, pasta).
of_color(hair, black).
loves_to_play_games(paty).
lazy(juan).
```

#### 📝 Explicación:

- `cat(tom).` ➜ Declara que Tom es un gato.
- `loves_to_eat(jorge, pasta).` ➜ Jorge ama comer pasta.
- `of_color(hair, black).` ➜ El pelo es de color negro.
- `loves_to_play_games(paty).` ➜ A Paty le encanta jugar juegos.
- `lazy(juan).` ➜ Juan es perezoso.

Los hechos son estáticos y no se derivan de ningún otro conocimiento. Son simplemente verdades conocidas.

---

### 🧠 Reglas (`reglas.pl`)

Las **reglas** permiten inferir nueva información a partir de hechos existentes. Se representan en la forma:

```prolog
conclusión :- condición1, condición2, ..., condiciónN.
```

#### 📄 Código:

```prolog
happy(lili) :- dances(lili).
hungry(tom) :- search_for_food(tom).
friends(jack, bili) :- lovesCricket(jack), lovesCricket(bili).
goToPlay(ryan) :- isClosed(school), free(ryan).
```

#### 📝 Explicación:

- `happy(lili) :- dances(lili).` ➜ Lili está feliz si baila.
- `hungry(tom) :- search_for_food(tom).` ➜ Tom tiene hambre si busca comida.
- `friends(jack, bili) :- lovesCricket(jack), lovesCricket(bili).` ➜ Jack y Bili son amigos si ambos aman el críquet.
- `goToPlay(ryan) :- isClosed(school), free(ryan).` ➜ Ryan irá a jugar si la escuela está cerrada y él está libre.

Las reglas nos permiten **modelar comportamientos más complejos** a partir de los hechos simples.

---

### 🔍 Consultas

Una vez definidos hechos y reglas, podemos realizar **consultas** a nuestro sistema para verificar si cierta afirmación es verdadera o para obtener datos que cumplan ciertas condiciones.

#### 📄 Ejemplos:

```prolog
?- cat(tom).
true.

?- loves_to_eat(jorge, pasta).
true.

?- happy(lili).
false.  % A menos que también esté definido dances(lili).

?- friends(jack, bili).
false.  % Depende de si existen los hechos lovesCricket(jack) y lovesCricket(bili)
```

Las consultas son la forma principal en la que interactuamos con el sistema lógico para **obtener respuestas a nuestras preguntas**.

---

📌 _Las siguientes partes del documento incluyen bases de conocimiento, relaciones familiares, operaciones con listas y más, lo cual permite modelar sistemas complejos como árboles genealógicos, estructuras de datos, operaciones aritméticas y flujos de control lógico._
