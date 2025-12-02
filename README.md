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
        if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
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
         if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
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

        System.out.println("\nA Kakuzo atacou com " + resultado3+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaK);
            }
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Kákuzo, está com "+vidaK+" de vida!");
            
        }
         if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
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
         while(vidaP >0 && (vidaTo > ((169/100)*40))){
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
          if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
        }
         System.out.println("Tobi se transforma em seu 2° estágio... o Obito.   Seus danos aumentaram em em 25% e a vida recuperou 15%. Lute para vencer!!!!!!!!!");
         
         vidaTo += ((vidaTo/100)*15);
         T1 = 39 + (39/100)*25;
         T2 = 25 + (25/100)*25;
         T3 = 2 + (2/100)*25;
         T4 = 18 + (18/100)*25;
         
         habilidade1 -= 15;
         habilidade2 -= 10;
         
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
         
          if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
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
        
        System.out.println("Você se aproxima de Madara, ninja temido por todos os demais da região.");
        System.out.println("\n Você encontra uma pequena cabana na região.");
        System.out.println("\n Você explora por curiosidade... um mercante sai de dentro desta cabana te entregando 3 frascos de habilidade.");
        System.out.println("O tempo é curto e ele pede para você de beber antes que seja tarde........");
        System.out.println("Você bebe e adquire 3 novas habilidades: cura, envenenamento e enfraquecimento");
        
        String veneno = "Veneno";
        int envenenar = 10;
        
        String cura = "Cura";
        int curar = 30;
        
        String Enfraquecimento = "Enfraquecimento";
        int enfraquecer = 10;
        
        System.out.println("Agora vá e salve a humanidade!!!!!!");
        
        System.out.println("\n\n\n\n\n\n\n");
        
        habilidade1 += 20;
        habilidade2 +=16;
        int invenenar = 0;
        vidaP +=70;
        
        int vidaM = 1205;
        int m1 = 24;
        int m2 = 19;
        int m3 = 0;
        int m4 = 15;
        
        System.out.println("A sua vida atual é "+vidaP+" pontos.");
        System.out.println("Dano da habilidade "+h1+" = "+ habilidade1);
        System.out.println("Dano da habilidade "+h2+" = "+ habilidade2);
        
        System.out.println("Novas habilidades adquiridas: ");
        System.out.println("Valor da "+ cura +" = "+ curar);
        System.out.println("Valor de "+ Enfraquecimento + " = "+ enfraquecer);
        System.out.println("Valor de "+ veneno+ " = "+ envenenar);
        
        System.out.println("\n\n Efeito do veneno: a vida do inimigo diminui a cada rodada de acordo com a quantidade de vezes usada. (acumulativa)");
        System.out.println("\n Efeito da cura: tu não ataca nem defende, mas cura a sua vida dependendo do momento.");
        System.out.println("\n Efeito do enfraquecimento: Diminui o ataque do inimigo a cada rodada que passa (acumulativa");
        
         System.out.println("Novo boss: Madara");
         System.out.println("vida total: "+vidaM);
         System.out.println("habilidade 1:"+m1+ " de dano");
         System.out.println("Habilidade 2:"+m2);
         System.out.println("Habilidade 3: "+m3);
         System.out.println("Habilidade 4: "+m4);
         
         System.out.println("Se proteja... se prepare!!!! Madara está sem aproximando em 5 segundos. Lute para vencer!!!!!");
         
          for (int i = inicio-5; i >= 1; i--) {
            System.out.println(i); // Exibe o número atual
            try {
                Thread.sleep(intervalo); // Pausa por 1 segundo
            } catch (InterruptedException e) {
                System.out.println("O temporizador foi interrompido.");
                // Em caso de interrupção, pode-se encerrar o loop
                break;
        
       
    }
    }
          
           System.out.println("Você está enfrentando o Madara, temidos por todos na região. Vença para proseguir!!!!!!! ");
        
        System.out.println("boss : Madara, vida: "+vidaM);
         while(vidaP >0 && (vidaM > ((1205/100)*75))){
            System.out.println("\nVocê está lutando contra Madara, o que deseja fazer? (atacar, envenenar, curar, enfraquecer ou defender?)");
            String resposta6 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta6)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaTo -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaTo -= habilidade2;
                 }
                 int resultado6 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado6;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Madara atacou com " + resultado6+" de dano!");
        
            }else if("defender".equals(resposta6)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado6;
        if (Math.random() < 0.25) {
            resultado6 = m2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado6 = m3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado6 = m1; // 25% de chance
        } else {
            resultado6 = m4; // 25% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado6+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaM);
            }else if("curar".equals(resposta6)){
            vidaP +=30;
                System.out.println("Tu curou 30 pontos de vida");
                 int resultado6;
        if (Math.random() < 0.25) {
            resultado6 = m2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado6 = m3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado6 = m1; // 25% de chance
        } else {
            resultado6 = m4; // 25% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado6+" de dano!");
        vidaP -= resultado6;
                
            }else if("envenenar".equals(resposta6)){
                invenenar += envenenar;
                System.out.println("Envenenou o inimigo com +"+envenenar+" de dano");
            
            }else if("enfraquecer".equals(resposta6)){
                 m1 -= (m1/100)*enfraquecer;
                  m2 -= (m2/100)*enfraquecer;
                   m3 -= (m3/100)*enfraquecer;
                    m4 -= (m4/100)*enfraquecer;
                    
                    System.out.println("Enfraqueceu 10% do dano do Madara");
            }
            
            vidaM -= invenenar;
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Madara, está com "+vidaM+" de vida!");
            
        }
          if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
        }
         
         System.out.println("O Madara se irritou.... as trevas o circulou e a fúria tomou a sua conta!!!");
         System.out.println("Aumento de 50% em seus ataques");
         
         m1 += (m1/100)*50;       
          m2 += (m2/100)*50;   
           m3 += (m3/100)*50;   
            m4 += (m4/100)*50;   
        
        System.out.println("O Madara está mais forte do que nunca. Tome cuidadoi em suas próximas escolhas!");
        System.out.println("Vida de "+nomeP+ " atual: "+ vidaP + "de vida");
        System.out.println("Dano de "+h1+" = "+habilidade1);
        System.out.println("Dano de "+h2+" = "+habilidade2);
        
        System.out.println("habilidades de Madara: "+ m1+"; "+m2+"; "+m3+"; e "+m4);
        System.out.println("Vida total de Madara: "+vidaM);
        
          System.out.println("Você esta enfrentando o Madara em seu segundo estagio. Vença para proseguir!!!!!!! ");
        
        System.out.println("boss : Madara, vida: "+vidaM);
         while(vidaP >0 && (vidaM > ((1205/100)*50))){
            System.out.println("\nVocê esta lutando contra Madara, o que deseja fazer? (atacar, envenenar, curar, enfraquecer ou defender?)");
            String resposta7 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta7)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaTo -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaTo -= habilidade2;
                 }
                 int resultado7 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado7;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Madara atacou com " + resultado7+" de dano!");
        
            }else if("defender".equals(resposta7)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado7;
        if (Math.random() < 0.25) {
            resultado7 = m2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado7 = m3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado7 = m1; // 25% de chance
        } else {
            resultado7 = m4; // 25% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado7+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaM);
            }else if("curar".equals(resposta7)){
            vidaP +=30;
                System.out.println("Tu curou 30 pontos de vida");
                 int resultado7;
        if (Math.random() < 0.25) {
            resultado7 = m2; // 25% de chance
        } else if (Math.random() < 0.5) {
            resultado7 = m3; // 25% de chance
        } else if (Math.random() < 0.75) {
            resultado7 = m1; // 25% de chance
        } else {
            resultado7 = m4; // 25% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado7+" de dano!");
        vidaP -= resultado7;
                
            }else if("envenenar".equals(resposta7)){
                invenenar += envenenar;
                System.out.println("Envenenou o inimigo com +"+envenenar+" de dano");
            
            }else if("enfraquecer".equals(resposta7)){
                 m1 -= (m1/100)*enfraquecer;
                  m2 -= (m2/100)*enfraquecer;
                   m3 -= (m3/100)*enfraquecer;
                    m4 -= (m4/100)*enfraquecer;
                    
                    System.out.println("Enfraqueceu 10% do dano do Madara");
            }
            
            vidaM -= invenenar;
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Madara, está com "+vidaM+" de vida!");
            
        }
          if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
        }
         System.out.println("Madara está irritado, ficou mais enfurecido e tomado pela fúria");
         System.out.println("\n Ele recuperou 10% de vida e ganhou envenenamento");
         
         int m5 = 0;
         vidaP +=250;
         
         
         System.out.println("O mercante te deu uma poção que ganha vida. Adquiriu mais 250 pontos de vida.");
           System.out.println("O Madara está mais forte do que nunca. Tome cuidadoi em suas próximas escolhas!");
        System.out.println("Vida de "+nomeP+ " atual: "+ vidaP + "de vida");
        System.out.println("Dano de "+h1+" = "+habilidade1);
        System.out.println("Dano de "+h2+" = "+habilidade2);
        
        System.out.println("habilidades de Madara: "+ m1+"; "+m2+"; "+m3+"; "+m4+" e envenenar ("+m5+5+")");
        System.out.println("Vida total de Madara: "+vidaM);
        
          System.out.println("Você esta enfrentando o Madara em seu terceiro estagio. Vença para proseguir!!!!!!! ");
        
        System.out.println("boss : Madara, vida: "+vidaM);
         while(vidaP >0 && (vidaM > ((1205/100)*20))){
            System.out.println("\nVocê esta lutando contra Madara, o que deseja fazer? (atacar, envenenar, curar, enfraquecer ou defender?)");
            String resposta8 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta8)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaTo -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaTo -= habilidade2;
                 }
                 int resultado8 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado8;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Madara atacou com " + resultado8+" de dano!");
        
            }else if("defender".equals(resposta8)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado8;
        if (Math.random() < 0.2) {
            resultado8 = m2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultado8 = m3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultado8 = m1; // 20% de chance
        } else if(Math.random()< 0.8){
            resultado8 = m4; // 20% de chance
        }else{
        resultado8 = m5;
        m5 +=5;        
// 20% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado8+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaM);
            }else if("curar".equals(resposta8)){
            vidaP +=30;
                System.out.println("Tu curou 30 pontos de vida");
                 int resultado8;
        if (Math.random() < 0.2) {
            resultado8 = m2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultado8 = m3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultado8 = m1; // 20% de chance
        } else if(Math.random() < 0.8){
            resultado8 = m4; // 20% de chance
        }else{
        resultado8 = m5;
           m5 += 5;        
// 20% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado8+" de dano!");
        vidaP -= resultado8;
                
            }else if("envenenar".equals(resposta8)){
                invenenar += envenenar;
                System.out.println("Envenenou o inimigo com +"+envenenar+" de dano");
            
            }else if("enfraquecer".equals(resposta8)){
                 m1 -= (m1/100)*enfraquecer;
                  m2 -= (m2/100)*enfraquecer;
                   m3 -= (m3/100)*enfraquecer;
                    m4 -= (m4/100)*enfraquecer;
                    
                    System.out.println("Enfraqueceu 10% do dano do Madara");
            }
            
            vidaM -= invenenar;
            vidaP -= m5;
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Madara, está com "+vidaM+" de vida!");
            
        }
          if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
        }
         System.out.println("Você consegue chegar na barra dos 20% da vida dele.... mas algo inesperado acontece!");
         System.out.println("Madara se irrita cada vez mais com você. Ele realiza um jutsu proibido, o 'edo tensei'");
         System.out.println("\n Madara revive todos os inimigos anteriores que você já havia enfrentado. Os seus danos aumentaram em 25% e você terá que enfrenta-los ao mesmo tempo!!!!!");
         
         System.out.println("\n\n\n\n\n\n\n..... Tsunade, Obito, Orochimaru e Kakuzo, todos renasceram de seus caixos e, aparentemente, todos inconscientes!  ");
         
         System.out.println("Voce deve enfrenta-los juntios e sobreviver!!! Hora de batalhar!!!!");
         
         vidaTo +=169;
         vidaO += 85;
         vidaK += 135;
         vidaT += 105;
         
        //Tsunade
         d1 += (d1/100)*25;
         d2 += (d2/100)*25;
         d3 += (d3/100)*25;
         d4 += (d4/100)*25;
         
        int envenenaD = 0;
         
          // Orochimaru
          hab1 += (hab1/100)*25;
          hab2 += (hab2/100)*25;
          hab3 += (hab3/100)*25;
          hab4 += (hab4/100)*25;
          
           int envenenaO = 0;
          
          
          // Obito
                   
          T1 += (T1/100)*25;
          T2 += (T2/100)*25;
          T3 += (T3/100)*25;
          T4 += (T4/100)*25;
          
           int envenenaTO = 0;
          // Kakuzo
          
          k1 += (k1/100)*25;
          k2 += (k2/100)*25;
          k3 += (k3/100)*25;
          k4 += (k4/100)*25;
          
           int envenenaK = 0;
          
          System.out.println("Hora de batalhar!!!!!");
          while(vidaP >0 && (vidaK > 0 || vidaO>0 || vidaTo > 0 || vidaT > 0)){
            System.out.println("\nVocê esta lutando contra Tsunade, Obito, Orochimaru e Kakuzo. O que deseja fazer? (atacar, envenenar, curar, enfraquecer ou defender?)");
            String resposta9 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta9)){
                System.out.println("\nEscolha quem você quer lutar: (Kakuzo, Tsunade, Obito ou Orochimaru)");
                 String escolha = entrada.nextLine().toLowerCase();
                 if("kakuzo".equals(escolha)){
                     System.out.println("Diga qual habilidade usar: ("+h1+" ou "+h2+")");
                     String poder = entrada.nextLine();
                 }else if("obito".equals(escolha)){
                 vidaTo -= habilidade2;
                 }else if("Orochimaru".equals(escolha)){
                 
                 }else if("Tsunade".equals(escolha)){
                 
                 }
                 int resultado9 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado9;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Madara atacou com " + resultado9+" de dano!");
        
            }else if("defender".equals(resposta9)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
              
              // Orochimaru
        int resultadoO;
        if (Math.random() < 0.25) {
            resultadoO = hab2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoO = hab3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoO = hab1; // 20% de chance
        } else {
            resultadoO = hab4; // 20% de chance
             
// 20% de chance
        }
        // Tsunade
        int resultadoT;
        if (Math.random() < 0.25) {
            resultadoT = d2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoT = d3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoT = d1; // 20% de chance
        } else {
            resultadoT = d4; // 20% de chance
        }
        
        // Kakuzo
         int resultadoK;
        if (Math.random() < 0.25) {
            resultadoK = k2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoK = k3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoK = k1; // 20% de chance
        } else {
            resultadoK = k4; // 20% de chance
        }
        
        // Obito
         int resultadoOB;
        if (Math.random() < 0.2) {
            resultadoOB = T2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultadoOB = T3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultadoOB = T1; // 20% de chance
        } else {
            resultadoOB = T4; // 20% de chance
        }

        System.out.println("\nO Orochimaru atacou com " + resultadoO+" de dano!");// Usando if/else para escolher um dos quatro valores
                System.out.println("\n A Tsunade atacou com "+ resultadoT+" de dano!");
                System.out.println("\n O Obito atacou com "+ resultadoOB+" de dano!");
                System.out.println("\n O Kakuzo atacou com "+ resultadoK+" de dano!");
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida Tsunade: "+vidaT);
                
                
            }else if("curar".equals(resposta9)){
            vidaP +=30;
                System.out.println("Tu curou 30 pontos de vida");
                 
               // Orochimaru
        int resultadoO;
        if (Math.random() < 0.25) {
            resultadoO = hab2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoO = hab3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoO = hab1; // 20% de chance
        } else {
            resultadoO = hab4; // 20% de chance
             
// 20% de chance
        }
        // Tsunade
        int resultadoT;
        if (Math.random() < 0.25) {
            resultadoT = d2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoT = d3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoT = d1; // 20% de chance
        } else {
            resultadoT = d4; // 20% de chance
        }
        
        // Kakuzo
         int resultadoK;
        if (Math.random() < 0.2) {
            resultadoK = k2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultadoK = k3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultadoK = k1; // 20% de chance
        } else {
            resultadoK = k4; // 20% de chance
        }
        
        // Obito
         int resultadoOB;
        if (Math.random() < 0.2) {
            resultadoOB = T2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultadoOB = T3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultadoOB = T1; // 20% de chance
        } else {
            resultadoOB = T4; // 20% de chance
        }

        System.out.println("\nO Orochimaru atacou com " + resultadoO+" de dano!");// Usando if/else para escolher um dos quatro valores
                System.out.println("\n A Tsunade atacou com "+ resultadoT+" de dano!");
                System.out.println("\n O Obito atacou com "+ resultadoOB+" de dano!");
                System.out.println("\n O Kakuzo atacou com "+ resultadoK+" de dano!");
        
              int ataqueInimigo = resultadoK+resultadoO+resultadoOB+resultadoT;
              vidaP -= ataqueInimigo;
                System.out.println("\nTu perdeu"+ataqueInimigo+" 1hp de vida. Vida total: "+ vidaP+", vida Tsunade: "+vidaT);
                System.out.println("Vida de Obito: "+ vidaTo);
                System.out.println("Vida de Orochimaru: "+vidaO);
                System.out.println("Vida de Kakuzo: "+vidaK);
                
                
            }else if("envenenar".equals(resposta9)){
                
                
                System.out.println("\nEscolha o inimigo que deseja realizar a ação: Orochimaru, Obito, Tsunade ou Kakuzo?");
                 String personagem = entrada.nextLine();
                 
                 if("Kakuzo".equals(personagem)){
                  envenenaK += envenenar;
                 }else if("Tsunade".equals(personagem)){
                    envenenaD += envenenar;
                 }else if("Obito".equals(personagem)){
                    envenenaTO += envenenar;
                 
                 }else if("Orochimaru".equals(personagem)){
                envenenaO += envenenar;
                 }
                 
                 
                System.out.println("Envenenou "+ personagem+" com +"+envenenar+" de dano");
                
                 int resultadoO;
        if (Math.random() < 0.25) {
            resultadoO = hab2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoO = hab3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoO = hab1; // 20% de chance
        } else {
            resultadoO = hab4; // 20% de chance
             
// 20% de chance
        }
        // Tsunade
        int resultadoT;
        if (Math.random() < 0.25) {
            resultadoT = d2; // 20% de chance
        } else if (Math.random() < 0.5) {
            resultadoT = d3; // 20% de chance
        } else if (Math.random() < 0.75) {
            resultadoT = d1; // 20% de chance
        } else {
            resultadoT = d4; // 20% de chance
        }
        
        // Kakuzo
         int resultadoK;
        if (Math.random() < 0.2) {
            resultadoK = k2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultadoK = k3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultadoK = k1; // 20% de chance
        } else {
            resultadoK = k4; // 20% de chance
        }
        
        // Obito
         int resultadoOB;
        if (Math.random() < 0.2) {
            resultadoOB = T2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultadoOB = T3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultadoOB = T1; // 20% de chance
        } else {
            resultadoOB = T4; // 20% de chance
        }

        System.out.println("\nO Orochimaru atacou com " + resultadoO+" de dano!");// Usando if/else para escolher um dos quatro valores
                System.out.println("\n A Tsunade atacou com "+ resultadoT+" de dano!");
                System.out.println("\n O Obito atacou com "+ resultadoOB+" de dano!");
                System.out.println("\n O Kakuzo atacou com "+ resultadoK+" de dano!");
        
              int ataqueInimigo = resultadoK+resultadoO+resultadoOB+resultadoT;
              vidaP -= ataqueInimigo;
                System.out.println("\nTu perdeu"+ataqueInimigo+" 1hp de vida. Vida total: "+ vidaP+", vida Tsunade: "+vidaT);
                System.out.println("Vida de Obito: "+ vidaTo);
                System.out.println("Vida de Orochimaru: "+vidaO);
                System.out.println("Vida de Kakuzo: "+vidaK);
                
            
            }else if("enfraquecer".equals(resposta9)){
                System.out.println("\nEscolha o inimigo que deseja realizar a ação: Orochimaru, Obito, Tsunade ou Kakuzo?");
                 String personagem = entrada.nextLine();
                 if("Kakuzo".equals(personagem)){
                  k1 -= (k1/100)*enfraquecer;
                  k2 -= (k2/100)*enfraquecer;
                   k3 -= (k3/100)*enfraquecer;
                    k4 -= (k4/100)*enfraquecer;
                 }else if("Tsunade".equals(personagem)){
                   d1 -= (d1/100)*enfraquecer;
                   d2 -= (d2/100)*enfraquecer;
                   d3 -= (d3/100)*enfraquecer;
                   d4 -= (d4/100)*enfraquecer;
                 }else if("Obito".equals(personagem)){
                   T1 -= (T1/100)*enfraquecer;
                   T2 -= (T2/100)*enfraquecer;
                   T3 -= (T3/100)*enfraquecer;
                   T3 -= (T3/100)*enfraquecer;
                 
                 }else if("Orochimaru".equals(personagem)){
                  hab1 -= (hab1/100)*enfraquecer;
                  hab2 -= (hab2/100)*enfraquecer;
                  hab3 -= (hab3/100)*enfraquecer;
                  hab4 -= (hab4/100)*enfraquecer;
                 }
                 
                    System.out.println("Enfraqueceu 10% do dano de "+personagem);
            }
            
            vidaK -= envenenaK;
            vidaO -= envenenaO;
            vidaT -= envenenaD;
            vidaTo -= envenenaTO;
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida.");
              System.out.println("A Tsunade está com "+vidaT+" de vida");
              System.out.println("O Kakuzo esta com "+vidaK+" de vida");
              System.out.println("O Obito esta com "+vidaTo+" de vida");
              System.out.println("O Orochimaru esta com "+vidaO+" de vida");
              
              
              if(vidaK == 0){
                  System.out.println("Kakuzo morreu. Ataque os outros!!!");
              }
              if(vidaO == 0){
                  System.out.println("Orochimaru morreu. Ataque os outros!!");
              }
              if(vidaT == 0){
                  System.out.println("Tsunade morreu. Ataque os outros!!");
              }
              if(vidaTo == 0){
                  System.out.println("O Obito morreu. Ataque os outros!!!!!");
              }
        }
           if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
            
        }
        }
           
           System.out.println("Parabéns, voce conseguiu derrotar todos sem morrer,mas o Madara não está contente com isso. Ele está infurecido, recuperou 5% de vida");
           System.out.println("A sua missão é acabar com a raça dele. Ataque!!!!!  (vida + 190)");
           
           vidaM += (vidaM/100)*5;
             System.out.println("Você esta enfrentando o Madara em seu ultimo estagio. Vença para proseguir!!!!!!! ");
        
        System.out.println("boss : Madara, vida: "+vidaM);
         while(vidaP >0 && vidaM > 0){
            System.out.println("\nVocê esta lutando contra Madara, o que deseja fazer? (atacar, envenenar, curar, enfraquecer ou defender?)");
            String resposta10 = entrada.nextLine().toLowerCase();
            if("atacar".equals(resposta10)){
                System.out.println("\nEscolha qual habilidade usar: ("+h1+" ou "+h2+")");
                 String poder = entrada.nextLine();
                 if(poder.equals(h1)){
                 vidaTo -= habilidade1;
                 }else if(poder.equals(h2)){
                 vidaTo -= habilidade2;
                 }
                 int resultado10 = Math.random() < 0.5 ? hab1 : hab2;
                 
                 vidaP -= resultado10;
                  if(h1.equals(h1)){
                      System.out.println("Tu atacou com "+ habilidade1+ " de dano!");
                  } else if(h2.equals(h2)){
                      System.out.println("Tu atacou com "+ habilidade2+" de dano!!");
                  }

        System.out.println("O Madara atacou com " + resultado10+" de dano!");
        
            }else if("defender".equals(resposta10)){
              vidaP -= 1;
              // sorteio 
              // Gerar número aleatório entre 0 e 1
        int resultado10;
        if (Math.random() < 0.2) {
            resultado10 = m2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultado10 = m3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultado10 = m1; // 20% de chance
        } else if(Math.random()< 0.8){
            resultado10 = m4; // 20% de chance
        }else{
        resultado10 = m5;
        m5 +=5;        
// 20% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado10+" de dano!");// Usando if/else para escolher um dos quatro valores
        
              
                System.out.println("\nTu defendeu perdendo 1hp de vida. Vida total: "+ vidaP+", vida inimigo: "+vidaM);
            }else if("curar".equals(resposta10)){
            vidaP +=30;
                System.out.println("Tu curou 30 pontos de vida");
                 int resultado10;
        if (Math.random() < 0.2) {
            resultado10 = m2; // 20% de chance
        } else if (Math.random() < 0.4) {
            resultado10 = m3; // 20% de chance
        } else if (Math.random() < 0.6) {
            resultado10 = m1; // 20% de chance
        } else if(Math.random() < 0.8){
            resultado10 = m4; // 20% de chance
        }else{
        resultado10 = m5;
           m5 += 5;        
// 20% de chance
        }

        System.out.println("\nO Madara atacou com " + resultado10+" de dano!");
        vidaP -= resultado10;
                
            }else if("envenenar".equals(resposta10)){
                invenenar += envenenar;
                System.out.println("Envenenou o inimigo com +"+envenenar+" de dano");
            
            }else if("enfraquecer".equals(resposta10)){
                 m1 -= (m1/100)*enfraquecer;
                  m2 -= (m2/100)*enfraquecer;
                   m3 -= (m3/100)*enfraquecer;
                    m4 -= (m4/100)*enfraquecer;
                    
                    System.out.println("Enfraqueceu 10% do dano do Madara");
            }
            
            vidaM -= invenenar;
            vidaP -= m5;
            System.out.println("\nVocê, "+nomeP+" está com "+vidaP+" de vida. O seu inimigo, Madara, está com "+vidaM+" de vida!");
            
        }
          
          if(vidaP == 0){
        while(vidaP == 0){
            System.out.println("Voce perdeu... recomece reiniciando o jogo!!!!");
        }
        }
          
          System.out.println("Madara finalmente é derrotado... e voce é gravemente ferido");
          System.out.println("Madara, já sem forcas para lutar e sua enorme forma, ele acaba caindo com tudo, o derrubando junto com voce");
          System.out.println("\n você, por sorte, caiu numa planície terrestre, onde se feriu mais ainda e está quase inconsciente....");
          System.out.println("\n Ao longe você percebe um senhor se aproximando, parece até aquele que saiu da cabana antes da batalhaas....");
          System.out.println("Ele se aproxima de você, o lamentando por estar quase inconsciente...");
          System.out.println("você não possui mais habilidades, não possui mais cura e a sua vida está completamente limitada....");
          System.out.println("\n Ele oferece para você ir junto com ele para um lugar desconhecido por você.... Qual a sua escolha???? (ficar ou ir)");
             String respostaFinal = entrada.nextLine().toLowerCase();
             
             if("ficar".equals(respostaFinal)){
                 System.out.println("\n\nVocê decidiu ficar, mas isso te torna incapaz de sair de lá....");
                 System.out.println("O senhor desaparece no meio da nevoa que o cercou.... a sua vida esta cada vez menor e aos poucos voce vai perdendo a consciencia");
                 System.out.println("\n ninguem estava ali para te ajudar, e voce deixa de existir naquele lugar... naquela realidade.... e naquele mundo.....");
             }else if("ir".equals(respostaFinal)){
                 System.out.println("Você decidiu ir com ele, o senhor te carrega e te cura... mas incapaz de lutar...");
                 System.out.println("Ele te leva para uma vila desconhecida.... onde lá você começa a sua jornada...");
             }
                  
             System.out.println("Naruto's Legacy");
              System.out.println("Naruto's Lega");
          System.out.println("Naruto's Le");
          System.out.println("Naruto's ");
          System.out.println("Naruto'");
         System.out.println("Narut");
         System.out.println("Naru");
         System.out.println("Nar");
         System.out.println("Na");
          System.out.println("N");
           System.out.println("");
            System.out.println("..");
             System.out.println("....");
              System.out.println("Produzido por Luiz");
         
              entrada.close();
    }
}
