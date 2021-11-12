
import java.util.Scanner;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */

/**
 *
 * @author FTD
 */
public class Main {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        String User0 = "Admin";
        String Pass0 = "Admin";
        
        String User = "";
        String Pass = "";
        
        int opcion = 0;
                
        Doctores doctor = new Doctores();
        Pacientes paciente = new Pacientes();
        Citas citas = new Citas();
        
        Scanner sc = new Scanner(System.in);        
        
        System.out.println("Bienvenido al sistema de Citas");
        System.out.println("Ingresa tu usuario y contraseña para poder ingresar");
        System.out.println("Usuario: ");
        User = sc.nextLine();
        System.out.println("Contraseña: ");
        Pass = sc.nextLine();
        
        if(User.contains(User0) && Pass.contains(Pass0)){
            do{
                System.out.println("Ingresa una opción: ");
                System.out.println("1. Dar de alta un Doctor.");
                System.out.println("2. Dar de alta un Paciente.");
                System.out.println("3. Dar de alta una Cita.");
                System.out.println("4. Salir.");
                
                opcion = Integer.parseInt(sc.nextLine());
                switch(opcion){
                    case 1: 
                        doctor.Alta();
                        break;
                    case 2:
                        paciente.Alta();
                        break;
                    case 3:
                        citas.GeneraCita();
                        break;
                }
            }while(opcion != 4);                    
            
        }
        else{
            System.out.println("Usuario o Contraseña Incorrectos");
        }
             
    }
    
}
