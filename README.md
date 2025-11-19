# Estudo-Array-e-projeto-de-listamento-de-carros-
Mais um estudo focado em Java, agora focando no principio Array

import java.util.ArrayList;
import java.utill.JOptionPane;

public class ArrayListCarros{
// O ARRAYLIST SO ADICIONA NO FINAL DA LISTA 
    public static void main(String[] args) {
        // contruindo um arraylist para os carros
        ArrayList<String> carros = new ArrayList<>();
        
        // adicionando Carros ao arraylist
        carros.add("Kombi");
        carros.add("JAGUAR");
        carros.add("BMW");
        carros.add("MERCEDES");
        carros.add("Fusca");
        carros.add("VECTRA");

        // mostra array
       System.out.println(carros); 

       //substituindo FUSCA por MITSUBUSHI
       carros.set(5, "MITSUBUSHI");
       //mostra array
         System.out.println(carros);

       // removendo o carro VECTRA
        carros.remove("VECTRA");
        //mostra array
        System.out.println(carros);

       //adciocionando carros ao arraylist com JOptionPane
       carros.add(JOptionPane.showInputDialog("Informe a marca do carro"));
         //mostra array
         System.out.println(carros);
        /* 
       //limpando o arraylist
       carros.clear();
         //mostra array
        System.out.println(carros);

        //verificando se o arraylist está vazio
        if (carros.idEmpty()) {
            System.out.println("O arraylist está vazio");
        }
        */
       
        //verificando se no arraylist contém a marca BMW
        System.out.println(carros.size());
        boolean achei = false;
        if (carros.contains("BMW")) {
            // SUBISTITUINDO QUANDO NÃO SE SABE A POSIÇÃO
            for (int i = 0; i <carros.size(); i++) {
                if ("BMW M3".equals(carros.get(i))) {
                    carros.set(i, "BUGATTI");
                    achei = true;
                    break;
                }
            }
         }     if (!achei) {
                System.out.println("Não encontrei o argumento pesquisado");
         } else {
        System.out.println("Achei o argumento pesquisado na posição" + i);
         }
     }


        //mostra array
        System.out.println(carros);





    }
