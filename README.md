# Modulo route-spa-hash
Este modulo esta diseñado para la creacion de aplicaciones de una sola pagina (SPA), cambiando el contenido de la web en funcion del hash que tiene la URL. Esto permite crear una SPA y poder suvirla a prodiccion sin la necesidas de hacer una configuracion extra en el servidor para la gestion de las rutas de la aplicación. 

## Instalación
Para poder integrar el modulo en un proyecto Js vanilla con npm:
```bash
 npm i route-spa-hash
```
## Descripción
El modulo añade la clase __RoutesHash__, la cual permite configurar en su metodo constructor los hash que funcionaran como rutas de la SPA, el contenido que mostrara cada ruta y un nodo para poder cerntralizar el contenodo que motrara cada una de las rutas

### Interfaz
La clase RoutesHash en su mayoria consta de propiedades y metodos que deben ser tratados como privados, a continuacion se describen los metodos que pueden tratados como publicos.

➤ __Constructor__. Cuando se instancia un nuevo objeto este puede recibir dos parametros:
```js
new RoutesHash(routes, rootNode);
```
Donde:
- _routes_ es un arreglo de objetos con las propiesades `hash` cuyo valor es  una cadena de caracteres con el hash que se usara como ruta y `view` cuyo valor es el contenido se mostrara en el nodo raiz asicuadio al hash. Su valor por defecto es un arreglo vacio.
```js
{
    hash: ruta,
    view: contenido
}
```
> [!NOTE]
> Para que el valor de `hash` sea valido deve iniciar con el simbolo # 

> [!NOTE]
> El modulo eta disñado para que el valor de `view` sean una referencia a un nodo del DOM, si el nodo es:
>- Un elemento HTML o un fragmento. Basta con pasar la referencia al nodo o el nodo
>- Un template. Se pasa el valor de la propiedad `content` de la referenci al nodo del template
>
>para cualquier otro nodo o valor diferente a un nodo el contenodo se pasa como una cadena de caracteres

