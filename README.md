# TreeSet

## Concepto
	
	El TreeSet es una implementación de la interfaz SortedSet
de Java y que almacena los datos en forma de árbol binario. El TreeSet 
permite almacenar valores no duplicados los cuales son ordenados en el 
momento en el que se insertan. Se puede definir un comparator para 
ordenar los datos

## Ventajas contra los HashSet
	
- En caso de que se necesiten los datos ordenados el TreeSet se asegura
de que siempre lo esten
- Ofrece varios métodos útiles a la hora de tratar con los datos del set
como: first(), last(), headSet(), tailSet().
- Al estar seguros de que los datos están ordenados se pueden realizar
busquedas más rápidas que en un HashSet

## Ejemplo

'''
import java.util.TreeSet;
import java.util.Iterator;

class Main {
    public static void main(String[] args) {

	// Creamos el TreeSet 
        TreeSet<Integer> numeros = new TreeSet<>();
	
	// Añadimos los datos
        numeros.add(3);
        numeros.add(1);
        numeros.add(6);
	numeros.add(4);

	// Imprimimos el TreeSet directamente
        System.out.println("TreeSet: " + numeros);

        // Usamos un iterador

        Iterator<Integer> iterate = numeros.iterator();
        System.out.print("TreeSet con iterador: ");
        while(iterate.hasNext()) {

            System.out.print(iterate.next());
            System.out.print(", ");
        }
    }
}
'''

Resultado

'''
TreeSet: [1, 3, 4, 6]
TreeSet con iterador: 1, 3, 4, 6
'''

## Métodos

Algunos métodos que se pueden usar con TreeSet son:

- add(e) -> Añade el elemento 'e'
- ceiling(e) -> Devuelve el primer valor mayor que o igual a 'e'
- clear() -> Remueve todos los elementos del set
- first() -> Devuelve el valor más pequeño del TreeSet
- last() -> Devuel el valor más pequeño del TreeSet
- size() -> Devuelve la cantidad de elementos del TreeSet
