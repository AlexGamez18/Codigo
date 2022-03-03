/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package tienda_level.sshop;

import java.util.Scanner;


public class Tienda_LevelSShop {

    /**
     * @param args
     * @autor Silas Antonio Aguilar Bonilla
     */
    public static void main(String[] args) {
        // TODO code application logic here
        String Inventario[] = new String[4];
        Scanner sc = new Scanner(System.in);
        System.out.println("Ingrese los productos ingresados en las 4 semanas del mes: ");
        for(int i=0;i<Inventario.length;i++)
        {
            System.out.println("Inventario "+(i+1));
            Inventario[i] = sc.next();
        }
        
        /**
         * @autor Edenilson Alexander Pino Gamez
         */
        //Use un método de arreglo para poder saber en que dias se vendio mas.
        double Ventas[] = new double[28];
        System.out.println("Ingrese las venta de los 28 dias del mes: ");
        for(int i=0;i<Ventas.length;i++)
        {
            System.out.println("Ventas "+(i+1));
            Ventas[i] = sc.nextDouble();
        }
        //Use este método para saber las ventas mayores o iguales a $100.
        int k = 0;
        int total = 0;
        System.out.println("Ventas mayores o igual a $100");
        while(k<28)
        {
            if(Ventas[k]>=100)
            {
                System.out.println("$"+Ventas[k]);
            total++;
            }
            k++;
        }
        System.out.println("El total de las ventas mayores a $100 es "+total);
    }  
}
