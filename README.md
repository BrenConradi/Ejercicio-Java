# Ejercicio-Java
Ejercicio java
#crear dos métodos, uno que cuente los números impares de una lista y otro que retorne los números consecutivos que hay en una lista.


public static int contarImpares(List<Integer> numeros) {
        int contadorImpares = 0;
        for (int numero : numeros) {
            if (numero % 2 != 0) {
                contadorImpares++;
            }
        }
        return contadorImpares;
}
 public static List<List<Integer>> encontrarConsecutivos(List<Integer> numeros) {
        List<List<Integer>> numerosConsecutivos = new ArrayList<>();
        List<Integer> secuenciaConsecutivaActual = new ArrayList<>();

        for (int i = 0; i < numeros.size(); i++) {
            if (i > 0 && numeros.get(i) == numeros.get(i - 1) + 1) {
                secuenciaConsecutivaActual.add(numeros.get(i));
            }
