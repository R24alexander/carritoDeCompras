# Carrito de compras

Creamos un sistema en el cual agregamos productos a nuestro carrito de compras, si queremos agregar más de un producto damos click en (+) y finalmente nos muestra el total.

### Herramientas

- HTML
- CSS
- JAVASCRIPT
- FIGMA
- TRELLO

### Programa carrito compras

![carritoDeCompras](https://gcdnb.pbrd.co/images/nuMLsh5oEd6v.png?o=1)

### Código

```Js
document.querySelectorAll(".item .actions .add").forEach((button) => {
    button.addEventListener("click", (e) => {
      const id = parseInt(button.getAttribute("data-id"));
      const item = db.methods.find(id);

      if (item && item.qty - 1 > 0) {
        // añadir a shopping cart
        shoppingCart.methods.add(id, 1);
        // console.log(shoppingCart);
        renderShoppingCart();
      } else {
        console.log("Ya no hay inventario");
      }
    });
```

_Manipulación de DOM para agregar los articulos._
