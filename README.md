import java.util.Scanner;
public class Main{
    public static void main(String[] args) {
        char tema, p1,p2,p3,p4,p5;
        int acerto,erro;
        boolean sair = false;
        Scanner leia = new Scanner (System.in);
        
        //Menu de apresentação e opção de escolha do tema, com DO para repetição.
        
        do{
            
            //Menu 

            sair=false;
            acerto = 0;
            erro=0;
            System.out.print("Escolha um tema: \n");
            System.out.println("A) Futebol");
            System.out.println("B) Filmes");
            System.out.println("C) Sair");
            System.out.print(" ");
            tema = leia.next().charAt(0);  // -----> //A variavel tema ira receber a entrade de leitura .

            /*Aqui ocorre a validação da variável "TEMA", para caso seja informado uma opção inválida sera exibida uma mensagem
             e ira repetir o menu até que o usuario escolha uma opção do menu ou arramque o pc da tomada.*/
            
            if (tema!='a' && tema!='A' && tema!='b' && tema!='B' && tema!='c' && tema!='C') {  
                System.out.println("Opção Inválida! Escolha entre A, B e C.");
            }else{
                
            //Nesse switch a variável "TEMA" vai ter dois casos, o caso 'a' ou 'A', e o caso 'b' ou 'B' definindo assim qual tema foi escolhido.
            
            switch (tema) {                  
   
                    /**********
                     TEMA FUTEBOL
                    ************/
                
                case 'a': case 'A':
                    
                    if(sair == false){          /*Este if faz a comparação da variável "sair", ser for verdadeiro continua executando o programa
                                                a baixo se não ele ira saltar para o proximo if que também ira comprar assim passando por todos 
                                                os if voltando para o menu inicial, colocado apenas para ter uma oção de sair a cada pergunta*/

                        do{
                               //Primeira pergundo no laço de repetição DO.
                            
                            System.out.println("\033[0;33m" + "Questão 1)" + "\033[0m");    
                            System.out.println("Quem é conhecido como o rei do futebol?\n");
                            System.out.println("a) Pelé.");
                            System.out.println("b) Maradona.");
                            System.out.println("c) Ronaldinho gaucho (bruxo).");
                            System.out.println("d) Ronaldo (fenomeno)");
                            System.out.println("e) Voltar ao Menu");
                           
                                //p1 é a variavel que recebe o leia armazenando a informação do usuario.
                            
                            p1 = leia.next().charAt(0);                 

                                /*Este if compara a varival p1 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                           
                            if (p1=='a' || p1=='A'){                    
                                System.out.println("\033[0;34m" + "Você acertou a questão\n" + "\033[0m");
                                
                                acerto++;
                            } else if (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E') { //Se a resposta guardada na variável "p1" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                                System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d \n");
                                
                            } else if (p1=='e' || p1=='E'){             //Se a resposta guardada na variável "p1" for igual a 'e' ou 'E', voltará ao menu.
                                sair = true;
                            } else{                                     //Se a resposta guardada na variável "p1" estiver errada, vai aparecer "Resposta Errada! ...".
                                System.out.println("\033[1;33m" + "Você errou! ..." + "\033[0m" + "Resposta correta letra A\n");
                                 erro++;
                            }

                            }while (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E');  //Aqui ocorre a validação da variável "p1", para caso seja informado uma opção inválida.
                
                    } if (sair == false) {

                        do{
                                //Segunda pergundo no laço de repetição DO.
                            System.out.println("\033[0;33m" + "Questão 2)" + "\033[0m");
                            System.out.println("Onde foi disputada a primeira copa do mundo?\n");
                            System.out.println("a) Brasil ");
                            System.out.println("b) Argentina ");
                            System.out.println("c) Uruguai ");
                            System.out.println("d) Paraguai ");
                            System.out.println("e) Voltar ao Menu");
                           
                            //p1 é a variavel que recebe o leia armazenando a informação do usuario.
                            
                            p2 = leia.next().charAt(0); 
                            
                                /*Este if compara a varival p2 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                            
                            if (p2=='c' || p2=='C'){                    //Se a resposta guardada na variável "p2" estiver certa, vai aparecer "Você acertou a questão".
                                System.out.println("\033[0;34m" + "Você acertou a questão\n" + "\033[0m");
                                
                                acerto++;
                            } else if (p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E') { //Se a resposta guardada na variável "p2" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                                System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d \n");  
                            } else if (p2=='e' || p2=='E'){              //Se a resposta guardada na variável "p2" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                            }else{                                     //Se a resposta guardada na variável "p2" estiver errada, vai aparecer "Resposta Errada! ...".
                                System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra C\n");
                                erro++;
                            }

                        }while(p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E');

                } if (sair == false){
                    
                        do{
                            //Terceira pergundo no laço de repetição DO.
                            System.out.println("\033[0;33m" + "Questão 3)" + "\033[0m");
                            System.out.println("Qual time de futebol ganhou mais Copas do Mundo?\n");
                            System.out.println("a) Italia ");
                            System.out.println("b) Brasil ");
                            System.out.println("c) Argentina ");
                            System.out.println("d) Uruguai ");
                            System.out.println("e) Voltar ao Menu");
                            p3 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p3".

                                /*Este if compara a varival p3 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                            
                            if (p3=='b' || p3=='B'){                    //Se a resposta guardada na variável "p3" estiver certa, vai aparecer "Você acertou a questão".
                                System.out.println("\033[0;34m" + "Você acertou a questão\n" + "\033[0m");
                                
                                acerto++;
                            } else if (p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E') { //Se a resposta guardada na variável "p3" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                                System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                            } else if (p3=='e' || p3=='E'){              //Se a resposta guardada na variável "p3" for igual a 'e' ou 'E', voltará ao menu.
                                sair = true;
                            } else{                                     //Se a resposta guardada na variável "p3" estiver errada, vai aparecer "Resposta Errada! ...".
                                System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra B\n");
                                erro++;
                            }

                        }while(p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E');
                    
                } if (sair == false){
                    
                        do{ 
                    
                            //Quarta pergundo no laço de repetição DO.
                            System.out.println("\033[0;33m" + "Questão 4)" + "\033[0m");    
                            System.out.println("Quem ganhou a Copa do Mundo de 2010?\n");
                            System.out.println("a) Argentina ");
                            System.out.println("b) Brasil ");
                            System.out.println("c) Espanha ");
                            System.out.println("d) Alemanhã ");
                            System.out.println("e) Voltar ao Menu");
                            p4 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p4".

                            /*Este if compara a varival p4 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                            if (p4=='c' || p4=='C'){                    //Se a resposta guardada na variável "p4" estiver certa, vai aparecer "Você acertou a questão".
                                System.out.println("\033[0;34m" + "Você acertou a questão\n" + "\033[0m");
                                
                                acerto++;
                            } else if (p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E') { //Se a resposta guardada na variável "p4" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                                System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                            } else if (p4=='e' || p4=='E'){              //Se a resposta guardada na variável "p4" for igual a 'e' ou 'E', voltará ao menu.
                                sair = true;
                            } else{                                     //Se a resposta guardada na variável "p4" estiver errada, vai aparecer "Resposta Errada! ...".
                                System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra C\n");
                                erro++;
                            }
                        
                        }while(p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E');

                } if (sair == false){ 

                        do{
                                //Quinta pergundo no laço de repetição DO.
                            System.out.println("\033[0;33m" + "Questão 5)" + "\033[0m");    
                            System.out.println("Quantas bolas de ouro Luis Figo ganhou?\n");
                            System.out.println("a) Uma ");
                            System.out.println("b) Duas ");
                            System.out.println("c) Cinco ");
                            System.out.println("d) Seis ");
                            System.out.println("e) Voltar ao Menu");
                            p5 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p5".

                            /*Este if compara a varival p5 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                            if (p5=='a' || p5=='A'){                    //Se a resposta guardada na variável "p5" estiver certa, vai aparecer "Você acertou a questão".
                                System.out.println("\033[0;34m" + "Você acertou a questão\n" + "\033[0m");
                                
                                acerto++;
                            } else if (p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E') { //Se a resposta guardada na variável "p5" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                                System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                            } else if (p5=='e' || p5=='E'){              //Se a resposta guardada na variável "p5" for igual a 'e' ou 'E', voltará ao menu.
                                sair = true;
                            } else{                                     //Se a resposta guardada na variável "p5" estiver errada, vai aparecer "Resposta Errada! ...".
                                System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra A\n");
                                erro++;
                            }
                        
                    }while(p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E');

                } if (sair == false){
                    
                            /*Se a condição if for falsa e o usuario passar por todos as alternativas do (DO While) chegando ao final 
                            o primeiro questionario chegara ao fim e será apresentado o resultado das variaveis "acertou" e " errou" 
                            mostrando ao usuario o taltal de erros e acertos que ele teve dando um break e voltando ao menu inicial*/
                         
                            
                        System.out.println("_____________________________________\n");    
                        System.out.println("Total de Acertos: "+acerto);
                        System.out.println("Total de Erros: "+erro);
                        System.out.println("_____________________________________\n");

                break;
              
                }
                    /**********
                     TEMA FILMES
                    ************/
                
                case 'b': case 'B':
                    
                if (sair == false){    

                    do{
                            //Primeira pergundo no laço de repetição DO.
                        System.out.println("\033[0;33m" + "Questão 1)" + "\033[0m");
                        System.out.println("No filme Halloween - A Noite do Terror a mascara de Michael Myers não era uma pessa original do filme ela foi retirada de outro filme qual seria esse?\n");
                        System.out.println("a) Darth Vader - Star Wars");
                        System.out.println("b) Freddy Krueger - A hoar do Pesadelo");
                        System.out.println("c) Capitão Kirk - Star Trek ");
                        System.out.println("d) Regan McNeil - O Exorcista ");
                        System.out.println("e) Voltar ao Menu");
                   
                
                        p1 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p1".

                        /*Este if compara a varival p1 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                        if (p1=='c' || p1=='C'){                    //Se a resposta guardada na variável "p1" estiver certa, vai aparecer "Você acertou a questão"
                            System.out.println("\033[0;34m" + "Você acertou! " + "\033[0m" + "A mascara custou apenas 2 dolares!\n");
                            
                            acerto++;
                        } else if (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E') { //Se a resposta guardada na variável "p1" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                        } else if (p1=='e' || p1=='E'){              //Se a resposta guardada na variável "p1" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                     //Se a resposta guardada na variável "p1" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra C\n");
                            erro++;
                        }

                    }while (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E');  //Aqui ocorre a validação da variável "p1", para caso seja informado uma opção inválida.

                }if (sair == false) {

                    do{
                            //Segunda pergundo no laço de repetição DO.
                        System.out.println("\033[0;33m" + "Questão 2)" + "\033[0m");    
                        System.out.println(" O que Marlon Brando usou na boca  para criar um estilo diferente de fala assim coneguindo o papel de Vito Corleone em O Poderoso Chefão ?\n");
                        System.out.println("a) Duas bolita");
                        System.out.println("b) Tampinhas de garrafa ");
                        System.out.println("c) Algodão ");
                        System.out.println("d) Chupeta ");
                        System.out.println("e) Voltar ao Menu");
                        p2 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p2".

                        /*Este if compara a varival p2 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                        if (p2=='c' || p2=='C'){                    //Se a resposta guardada na variável "p2" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("\033[0;34m" + "Você acertou! " + "\033[0m" + "Depois que conseguiu o papel, o seu dentista criou uma peça exclusiva para a mesma função.\n");
                            
                            acerto++;
                        } else if (p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E') { //Se a resposta guardada na variável "p2" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                        } else if (p2=='e' || p2=='E'){              //Se a resposta guardada na variável "p2" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                       //Se a resposta guardada na variável "p2" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra C\n");
                            erro++;
                        }

                    }while(p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E');

                } if (sair == false){
            
                    do{
                            //Terceira pergundo no laço de repetição DO.
                        System.out.println("\033[0;33m" + "Questão 3)" + "\033[0m");
                        System.out.println("Quantas vezes Stanley Kubrick no filme O Iluminado teve que regravar a famosa cena do banheiro até que ela ficasse do jeito que o diretor queria?\n");
                        System.out.println("a) 25 ");
                        System.out.println("b) 80 ");
                        System.out.println("c) 50 ");
                        System.out.println("d) 127 ");
                        System.out.println("e) Voltar ao Menu");
                        p3 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p3".

                        /*Este if compara a varival p3 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                        if (p3=='d' || p3=='D'){                    //Se a resposta guardada na variável "p3" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("\033[0;34m" + "Você acertou! " + "\033[0m" + "O número do quarto assustador foi alterado de 217 para 237, pois os administradores do local ficaram com medo de que ninguém quisesse se hospedar lá futuramente.\n");
                            
                            acerto++;
                        } else if (p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E') { //Se a resposta guardada na variável "p3" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                        } else if (p3=='e' || p3=='E'){              //Se a resposta guardada na variável "p3" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                      //Se a resposta guardada na variável "p3" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra D\n");
                            erro++;
                        }

                    }while(p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E');
            
                } if (sair == false){
            
                    do{ 
            
                            //Quarta pergundo no laço de repetição DO.
                        System.out.println("\033[0;33m" + "Questão 4)" + "\033[0m");    
                        System.out.println("Qual era o carro dirigido por Tio Ben em Homem-Aranha (2002)?\n");
                        System.out.println("a) Oldsmobile Delta 88 ");
                        System.out.println("b) Opala ss (1970) ");
                        System.out.println("c) Maverick v8 ");
                        System.out.println("d) Ford Corcel (1980) ");
                        System.out.println("e) Voltar ao Menu");
                        
                        p4 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p4".

                        /*Este if compara a varival p4 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                        if (p4=='a' || p4=='A'){                    //Se a resposta guardada na variável "p4" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("\033[0;34m" + "Você acertou! " + "\033[0m" + "Oldsmobile Delta 88 do diretor Sam Raimi, que tenta inserir o veículo em quase todos os seus filmes.\n");
                            
                            acerto++;
                        } else if (p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E') { //Se a resposta guardada na variável "p4" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                        } else if (p4=='e' || p4=='E'){              //Se a resposta guardada na variável "p4" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                      //Se a resposta guardada na variável "p4" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra A\n");
                            erro++;
                        }
                
                    }while(p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E');

                } if (sair == false){ 

                    do{
                            //Quinta pergundo no laço de repetição DO.
                        System.out.println("\033[0;33m" + "Questão 5)" + "\033[0m");
                        System.out.println("O filme que mais apresentou mortes na história do cinema foi?\n");
                        System.out.println("a) Kill Bill ");
                        System.out.println("b) O Senhor dos Anéis ");
                        System.out.println("c) Rambo ");
                        System.out.println("d) 300 ");
                        System.out.println("e) Voltar ao Menu");
                        p5 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p5".

                        /*Este if compara a varival p5 com a resposta se for igual a respota será exibina a mensagem e o variavel acertou recebera +1
                            caso o contrario eslse if confirma se o usuario digitou uma opção valida caso a opção escolhida for "e" a variavel sair passara a ser true
                            saltando todas as perguntas voltando para o menu inicial, se a opção escolhida for diferente do if e não atender nemnhuma das condições dos
                            eslse if então o else sera executado exibindo a mensagem e a variavel erro recebera +1*/
                        if (p5=='b' || p5=='B'){                    //Se a resposta guardada na variável "p5" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("\033[0;34m" + "Você acertou! " + "\033[0m" + "Com 836 baixas contabilizadas, “O Senhor dos Anéis: O Retorno do Rei” ficou na frente até dos sanguinários “300” (com 600 mortes) e o clássico de guerra “O resgate do Soldado Ryan” (com 255).\n");
                            
                            acerto++;
                        } else if (p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E') { //Se a resposta guardada na variável "p5" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("\033[0;31m" + "Resposta Inválida! " + "\033[0m" + "Escolha entre a, b, c ou d\n");  
                        } else if (p5=='e' || p5=='E'){              //Se a resposta guardada na variável "p5" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                      //Se a resposta guardada na variável "p5" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("\033[1;33m" + "Você errou! ...\n" + "\033[0m" + "Resposta correta letra B\n");
                            erro++;
                        }
                
                    }while(p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E');

                } if (sair == false){
                            
                            /*Se a condição if for falsa e o usuario passar por todos as alternativas do (DO While) chegando ao final 
                            o primeiro questionario chegara ao fim e será apresentado o resultado das variaveis "acertou" e " errou" 
                            mostrando ao usuario o taltal de erros e acertos que ele teve dando um break e voltando ao menu inicial*/
                         
                        System.out.println("_____________________________________\n");    
                        System.out.println("Total de Acertos: "+acerto);
                        System.out.println("Total de Erros: "+erro);
                        System.out.println("_____________________________________\n");

                break;
      
                    }
                }
            }

        } while (tema!='c' && tema!='C');               //Se for escolhida a opção 'c' ou 'C' do tema, finalizará o código.

                
    }

}
