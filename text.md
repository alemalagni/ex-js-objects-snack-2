## Snack 1

```
console.log(hamburger.name); // Double Cheese Burger
console.log(secondBurger.name ); // Double Cheese Burger
```

Creato **1** oggetto in memoria

## Snack 2

```
console.log(hamburger.ingredients[0]); // Salad
console.log(secondBurger.ingredients[0]); // Salad
```

Creati **3** oggetti in memoria

## Snack 3

Creati **9** oggetti in memoria

## Snack 4
1. ### Spread Operator (...)
   l'oggetto chef ha solo elementi di primo livello (non ha oggetti o array), inoltre Spread Operator permette di copiare la funzione makeBurger

2. ### StructuredClone()
    l'oggetto restaurant presenta un oggetto e un Date. StructuredClone ci permette di fare una Deep Copy (copiare tutti gli oggeti annidati) e salva la variabile openingDate come Date

## Snack 5

```
console.log(hamburger.maker.name); // Chef Hyur
console.log(secondBurger.maker.name); // Chef Hyur
console.log(hamburger.maker.restaurant.name); // Hyur's II
console.log(secondBurger.maker.restaurant.name); // Hyur's II
```

Creati **5** oggetti in memoria

## Snack 6
1. ### Spread Operator (...)
    L'oggetto contiene a sua volta diversi oggetti annidati, ognuna con una funzione al suo interno, di conseguenza non si può copiare "in profondità". Dato che lo Spread Operator fa una copia superficiale di primo livello, e quindi non fa una copia effettiva degli oggetti, bisogna usare lo Spread Operator per ogni oggetto presente:
    ```
    const copyChef = {
        ...chef, 
        restaurant: {
            ...chef.restaurant, 
            address: {
                ...chef.restaurant.address
                }
            }
        }
    ```