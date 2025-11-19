# JogoNarutp


/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package fundamentosjavasenac;
import java.util.Scanner;
import java.util.Random;
/**
 *
 * @author LUIZVINICIUSCASSABON
 */
public class Naruto {
    public static void main(String[] args) {
    
        Scanner entrada = new Scanner(System.in);
        Random sorteio = new Random();
        
        // personagem principal
        System.out.println("Me diga o seu nome de ninja: ");
        String nomeP = entrada.nextLine();
        
        System.out.println("Mostre as suas 2 habilidades (1°):");
        String h1 = entrada.nextLine();
        
        System.out.println("Mostre as suas 2 habilidades (2°): ");
        String h2 = entrada.nextLine();
        
        boolean ha1 = (h1.equals(h1));
        boolean ha2 = (h2.equals(h2));
        
        int habilidade1 = 19;
        int habilidade2 = 15;
        System.out.println(h1);
        
        System.out.println(h2);
        if(ha1 == true){
            System.out.println("Dano de "+h1+" = "+habilidade1);
        }if(ha2 == true){
         System.out.println("Dano de "+h2+" = "+habilidade2);
        }
        int vidaP = 100;
        
        System.out.println("Você está enfrentando um inimigo chamado 'Orochimaru'. Lute para vencer!!!!!!!!!!!");
        
        // inimigo 1 (Orochimaru)
        int hab1 = 10;
        int hab2 = 12;
        int hab3 = 0;
        int hab4 = 5;
        
        int vidaO = 85;
        
        while(vidaP >0 && vidaO > 0){
            System.out.println("\nVocê está lutando com Orichimaru, o que deseja fazer? (atacar ou defender?)");
            String resposta = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaO -= 19;
                 }else if(poder.equals(h2)){
                 vidaO -= 15;
                 }
                 int resultado = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O inimigo atacou com " + resultado+" de dano!");
        
            }else if("defender".equals(resposta)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado;
        if (Math.random() < 0.25) {
            resultado = hab1; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado = hab2; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado = hab3; // 25% de chance
        } else {
            resultado = hab4; // 25% de chance
        }

        System.out.println("\nO Orochimaru atacou com " + resultado+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaO);
            }
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Orochimaru, está com "+vidaO+" de vida!");
            
        }
        
        System.out.println("Parabéns por derrotar o Orochimaru. Recupere 37 pontos de vida. Prepare-se para o próximo inimigo, *Tsunade* ");
        System.out.println("\n"+nomeP+", Total de vida: "+ (vidaP+37));
        
        System.out.println("Próximo inimigo chega em 10 segundos. Se prepare  (subiu para o level 2 -> "+h1+" = "+ habilidade1 + " + 6.   "+h2+" = "+ habilidade2 + " + 4");
        
        
        // Valor inicial da contagem
        int inicio = 10;
        // Intervalo em milissegundos (1 segundo = 1000 ms)
        int intervalo = 1000;

        // Loop regressivo de 'inicio' até 1
        for (int i = inicio; i >= 1; i--) {
            System.out.println(i); // Exibe o número atual
            try {
                Thread.sleep(intervalo); // Pausa por 1 segundo
            } catch (InterruptedException e) {
                System.out.println("O temporizador foi interrompido.");
                // Em caso de interrupção, pode-se encerrar o loop
                break;
            }
        }

        // Mensagem final após a contagem
        System.out.println("Tempo esgotado!");
        
        System.out.println("Novo inimigo: Tsunade");
        System.out.println("Vida de "+ nomeP+": "+(vidaP+37)+" de vida!");
        System.out.println("Dano de "+ h1+": "+(habilidade1+6) + "!");
        System.out.println("Dano de "+ h2+": "+(habilidade2+4) + "!");
        
        habilidade1 += 6;
        habilidade2 +=4;
        vidaP +=37;
        
        int vidaT = 105;
        int d1 = 15;
        int d2 = 17;
        int d3 = 0;
        int d4 = 2;
        
        System.out.println("Você está lutando contra a Tsunade, Vença para prosseguir!!!!!!!!!!");
        while(vidaP >0 && vidaT > 0){
            System.out.println("\nVocê está lutando contra Tsunade, o que deseja fazer? (atacar ou defender?)");
            String resposta2 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta2)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaT -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaT -= habilidade2;
                 }
                 int resultado2 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado2;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O inimigo atacou com " + resultado2+" de dano!");
        
            }else if("defender".equals(resposta2)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado2;
        if (Math.random() < 0.25) {
            resultado2 = d2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado2 = d3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado2 = d1; // 25% de chance
        } else {
            resultado2 = d4; // 25% de chance
        }

        System.out.println("\nA Tsunade atacou com " + resultado2+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaT);
            }
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. A sua inimiga, Tsunade, está com "+vidaT+" de vida!");
            
        }
        System.out.println("\nParabéns, tu conseguiu derrotar a Tsunade!!");
        System.out.println("Vida total de "+ nomeP+": "+ vidaP);
        System.out.println("Subiu para o nível 3 -> Dano de "+h1+": "+ (habilidade1)+"+ 8.      Dano de "+h2+": "+ habilidade2+ "+ 7");
        System.out.println(nomeP+", Adquiriu 40 pontos de vida para a próxima batalha!");
        System.out.println("\nVida atualizada: "+ (vidaP+40));        
        System.out.println("\nPróximo inimigo, Kakuzo, chegando em 10 segundos. Se prepare!! \n");
        
        

        // Loop regressivo de 'inicio' até 1
        for (int i = inicio; i >= 1; i--) {
            System.out.println(i); // Exibe o número atual
            try {
                Thread.sleep(intervalo); // Pausa por 1 segundo
            } catch (InterruptedException e) {
                System.out.println("O temporizador foi interrompido.");
                // Em caso de interrupção, pode-se encerrar o loop
                break;
        
       
    }
    
}
        habilidade1 += 8;
        habilidade2 +=7;
        vidaP +=40;
        
        int vidaK = 135;
        int k1 = 24;
        int k2 = 19;
        int k3 = 0;
        int k4 = 15;
        
        
        
        
        System.out.println("Você está enfrentando o Kákuzo. Lute e vença para prosseguir!!!!!!!!");
        while(vidaP >0 && vidaK > 0){
            System.out.println("\nVocê está lutando contra Kakuzo, o que deseja fazer? (atacar ou defender?)");
            String resposta3 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta3)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaK -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaK -= habilidade2;
                 }
                 int resultado3 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado3;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O inimigo atacou com " + resultado3+" de dano!");
        
            }else if("defender".equals(resposta3)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado3;
        if (Math.random() < 0.25) {
            resultado3 = k2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado3 = k3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado3 = k1; // 25% de chance
        } else {
            resultado3 = k4; // 25% de chance
        }

        System.out.println("\nA Tsunade atacou com " + resultado3+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaK);
            }
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Kákuzo, está com "+vidaK+" de vida!");
            
        }
         System.out.println("\nParabéns, tu conseguiu derrotar o Kákuso!!");
        System.out.println("Vida total de "+ nomeP+": "+ vidaP);
        System.out.println("Subiu para o nível 4 -> Dano de "+h1+": "+ (habilidade1)+"+ 13.      Dano de "+h2+": "+ habilidade2+ "+ 10");
        System.out.println(nomeP+", Adquiriu 50 pontos de vida para a próxima batalha!");
        System.out.println("\nVida atualizada: "+ (vidaP+50));        
        System.out.println("\nPróximo inimigo, Tobi, chegando em 10 segundos. Se prepare!! \n");
        
        for (int i = inicio; i >= 1; i--) {
            System.out.println(i); // Exibe o número atual
            try {
                Thread.sleep(intervalo); // Pausa por 1 segundo
            } catch (InterruptedException e) {
                System.out.println("O temporizador foi interrompido.");
                // Em caso de interrupção, pode-se encerrar o loop
                break;
        
       
    }
    }
        vidaP += 50;
        
        habilidade1+=13;
        habilidade2+=10;
        
        int vidaTo = 169;
        int T1 = 39;
        int T2 = 25;
        int T3 = 2;
        int T4 = 18;
        
        
        
        System.out.println("Você está enfrentando o Tobi, completamente forte. Vença para proseguir!!!!!!! ");
        
        System.out.println("Subchefe 1: Tobi, vida: "+vidaTo);
         while(vidaP >0 && (vidaTo > ((vidaTo/100)*40))){
            System.out.println("\nVocê está lutando contra Tobi, o que deseja fazer? (atacar ou defender?)");
            String resposta4 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta4)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaTo -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaTo -= habilidade2;
                 }
                 int resultado4 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado4;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Tobi atacou com " + resultado4+" de dano!");
        
            }else if("defender".equals(resposta4)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado4;
        if (Math.random() < 0.25) {
            resultado4 = T2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado4 = T3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado4 = T1; // 25% de chance
        } else {
            resultado4 = T4; // 25% de chance
        }

        System.out.println("\nO Tobi atacou com " + resultado4+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaTo);
            }
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Tobi, está com "+vidaTo+" de vida!");
            
        }
         System.out.println("Tobi se transforma em seu 2° estágio... o Obito.   Seus danos aumentaram em em 25% e a vida recuperou 15%. Lute para vencer!!!!!!!!!");
         
         vidaTo += ((vidaTo/100)*15);
         T1 = 39 + (39/100)*25;
         T2 = 25 + (25/100)*25;
         T3 = 2 + (2/100)*25;
         T4 = 18 + (18/100)*25;
         
         while(vidaP >0 && vidaTo >0){
            System.out.println("\nVocê está lutando contra Obito, o que deseja fazer? (atacar ou defender?)");
            String resposta5 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta5)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaTo -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaTo -= habilidade2;
                 }
                 int resultado5 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado5;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Obito atacou com " + resultado5+" de dano!");
        
            }else if("defender".equals(resposta5)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado5;
        if (Math.random() < 0.25) {
            resultado5 = T2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado5 = T3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado5 = T1; // 25% de chance
        } else {
            resultado5 = T4; // 25% de chance
        }

        System.out.println("\nO Obito atacou com " + resultado5+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaTo);
            }
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Tobi, está com "+vidaTo+" de vida!");
            
        }
         
         
         
         
         System.out.println("\nParabéns, tu conseguiu derrotar o Tobi/Obito!!");
        System.out.println("Vida total de "+ nomeP+": "+ vidaP);
        System.out.println("Subiu para o nível 4 -> Dano de "+h1+": "+ (habilidade1)+"+ 19.      Dano de "+h2+": "+ habilidade2+ "+ 16");
        System.out.println(nomeP+", Adquiriu 60 pontos de vida para a próxima batalha!");
        System.out.println("\nVida atualizada: "+ (vidaP+60));        
        System.out.println("\nPróximo e último inimigo, Madara, chegando em 10 segundos. Se prepare!! \n");
        
        for (int i = inicio; i >= 1; i--) {
            System.out.println(i); // Exibe o número atual
            try {
                Thread.sleep(intervalo); // Pausa por 1 segundo
            } catch (InterruptedException e) {
                System.out.println("O temporizador foi interrompido.");
                // Em caso de interrupção, pode-se encerrar o loop
                break;
        
       
    }
    }
        
        
    }
}
