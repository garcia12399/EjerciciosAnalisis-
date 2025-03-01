
package ejerciciosanalisis;

import java.util.Scanner;
public class Ejerciciosanalisis {

    public static void main(String[] args) {
          Scanner scanner = new Scanner(System.in);
        double suma = 0.0;
        boolean continuar = true;

        while (continuar) {
            System.out.print("Ingrese un número real: ");
            double numero = scanner.nextDouble();
            suma += numero;    

            System.out.print("¿Desea ingresar otro número? (si/no): ");
            String respuesta = scanner.next();

            if (respuesta.equalsIgnoreCase("no")) {
                System.out.print("¿Está seguro que desea salir? (si/no): ");
                String confirmacion = scanner.next();

                if (confirmacion.equalsIgnoreCase("si")) {
                    continuar = false;
                }
            }
        }

        System.out.println("La suma de los números ingresados es: " + suma);
        scanner.close();
    }
    
}
