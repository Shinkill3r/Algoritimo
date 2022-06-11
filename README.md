import java.util.Scanner;
public class teste{
    public static void main(String[] args) {
        char tema, p1,p2,p3,p4,p5;
        int acerto,erro;
        boolean sair = false;
        Scanner leia = new Scanner (System.in);

        do{
            //Menu

            sair=false;
            acerto = 0;
            erro=0;

            System.out.println("a) Futebol");
            System.out.println("b) Filmes");
            System.out.println("c) Sair");
            System.out.print("Qual opção você deseja:");
            tema = leia.next().charAt(0);                         //Aqui a opção desejada será guardada na variável "TEMA".

            if (tema!='a' && tema!='A' && tema!='b' && tema!='B' && tema!='c' && tema!='C') {  //Aqui ocorre a validação da variável "TEMA", para caso seja informado uma opção inválida.
                System.out.println("Opção Inválida! Escolha a opção a, b ou c");
            }else{
                
            switch (tema) {                                            //Nesse switch a variável "TEMA" vai ter dois casos, o caso 'a' ou 'A', e o caso 'b' ou 'B'. 
   
                    //Tema "Futebol"
                case 'a': case 'A':
                    
                if(sair == false){                                     //Aqui vai ser comparada a variável "sair", ser for verdadeiro continua abaixo.

                    do{
                            //Pergunta 1
                        System.out.println("Pergunta 1");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                           
                        
                        p1 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p1".

                        if (p1=='a' || p1=='A'){                    //Se a resposta guardada na variável "p1" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        } else if (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E') { //Se a resposta guardada na variável "p1" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                          System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        } else if (p1=='e' || p1=='E'){             //Se a resposta guardada na variável "p1" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                     //Se a resposta guardada na variável "p1" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }

                    }while (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E');  //Aqui ocorre a validação da variável "p1", para caso seja informado uma opção inválida.
                
                } if (sair == false) {

                    do{
                            //Pergunta 2
                        System.out.println("Pergunta 2");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p2 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p2".

                        if (p2=='b' || p2=='B'){                    //Se a resposta guardada na variável "p2" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E') { //Se a resposta guardada na variável "p2" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                          System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p2=='e' || p2=='E'){              //Se a resposta guardada na variável "p2" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        }else{                                     //Se a resposta guardada na variável "p2" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }

                    }while(p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E');

                } if (sair == false){
                    
                    do{
                            //Pergunta 3
                        System.out.println("Pergunta 3");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p3 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p3".

                        if (p3=='c' || p3=='C'){                    //Se a resposta guardada na variável "p3" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E') { //Se a resposta guardada na variável "p3" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                          System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p3=='e' || p3=='E'){              //Se a resposta guardada na variável "p3" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                     //Se a resposta guardada na variável "p3" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }

                    }while(p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E');
                    
                } if (sair == false){
                    
                    do{ 
                    
                            //Pergunta 4
                        System.out.println("Pergunta 4");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p4 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p4".

                        if (p4=='d' || p4=='D'){                    //Se a resposta guardada na variável "p4" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E') { //Se a resposta guardada na variável "p4" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                          System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p4=='e' || p4=='E'){              //Se a resposta guardada na variável "p4" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                     //Se a resposta guardada na variável "p4" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }
                        
                    }while(p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E');

                } if (sair == false){ 

                    do{
                            //Pergunta 5
                        System.out.println("Pergunta 5");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p5 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p5".

                         if (p5=='a' || p5=='A'){                    //Se a resposta guardada na variável "p5" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E') { //Se a resposta guardada na variável "p5" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                          System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p5=='e' || p5=='E'){              //Se a resposta guardada na variável "p5" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                     //Se a resposta guardada na variável "p5" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }
                        
                    }while(p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E');

                } if (sair == false){
                            //Total de acertos e erros.
                        System.out.println("Total de Acertos: "+acerto);
                        System.out.println("Total de Erros: "+erro);

                    break;
              
                }
                    //Tema "Filmes"
                case 'b': case 'B':
                    
                if(sair == false){    

                    do{
                            //Pergunta 1
                        System.out.println("Pergunta 1");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                   
                
                        p1 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p1".

                        if (p1=='a' || p1=='A'){                    //Se a resposta guardada na variável "p1" estiver certa, vai aparecer "Você acertou a questão"
                            System.out.println("Você acertou a questão");
                            acerto++;
                        } else if (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E') { //Se a resposta guardada na variável "p1" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        } else if (p1=='e' || p1=='E'){              //Se a resposta guardada na variável "p1" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                     //Se a resposta guardada na variável "p1" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }

                    }while (p1!='a' && p1!='A' && p1!='b' && p1!='B' && p1!='c' && p1!='C' && p1!='d' && p1!='D' && p1!='e' && p1!='E');  //Aqui ocorre a validação da variável "p1", para caso seja informado uma opção inválida.

                }if (sair == false) {

                    do{
                            //Pergunta 2
                        System.out.println("Pergunta 2");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p2 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p2".

                        if (p2=='b' || p2=='B'){                    //Se a resposta guardada na variável "p2" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E') { //Se a resposta guardada na variável "p2" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p2=='e' || p2=='E'){              //Se a resposta guardada na variável "p2" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        }else{                                       //Se a resposta guardada na variável "p2" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }

                    }while(p2!='a' && p2!='A' && p2!='b' && p2!='B' && p2!='c' && p2!='C' && p2!='d' && p2!='D' && p2!='e' && p2!='E');

                } if (sair == false){
            
                    do{
                            //Pergunta 3
                        System.out.println("Pergunta 3");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p3 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p3".

                        if (p3=='c' || p3=='C'){                    //Se a resposta guardada na variável "p3" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E') { //Se a resposta guardada na variável "p3" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p3=='e' || p3=='E'){              //Se a resposta guardada na variável "p3" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                      //Se a resposta guardada na variável "p3" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }

                    }while(p3!='a' && p3!='A' && p3!='b' && p3!='B' && p3!='c' && p3!='C' && p3!='d' && p3!='D' && p3!='e' && p3!='E');
            
                } if (sair == false){
            
                    do{ 
            
                            //Pergunta 4
                        System.out.println("Pergunta 4");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p4 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p4".

                        if (p4=='d' || p4=='D'){                    //Se a resposta guardada na variável "p4" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E') { //Se a resposta guardada na variável "p4" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p4=='e' || p4=='E'){              //Se a resposta guardada na variável "p4" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                      //Se a resposta guardada na variável "p4" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }
                
                    }while(p4!='a' && p4!='A' && p4!='b' && p4!='B' && p4!='c' && p4!='C' && p4!='d' && p4!='D' && p4!='e' && p4!='E');

                } if (sair == false){ 

                    do{
                            //Pergunta 5
                        System.out.println("Pergunta 5");
                        System.out.println("a) Resposta 1");
                        System.out.println("b) Resposta 2");
                        System.out.println("c) Resposta 3");
                        System.out.println("d) Resposta 4");
                        System.out.println("e) Voltar ao Menu");
                        p5 = leia.next().charAt(0);                 //Aqui a resposta vai ser guardada na variável "p5".

                        if (p5=='a' || p5=='A'){                    //Se a resposta guardada na variável "p5" estiver certa, vai aparecer "Você acertou a questão".
                            System.out.println("Você acertou a questão");
                            acerto++;
                        }else if (p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E') { //Se a resposta guardada na variável "p5" for diferente de qualquer uma das alternativas, vai aparecer "Resposta Inválida! Escolha a letra a, b, c, d ou e".
                            System.out.println("Resposta Inválida! Escolha a letra a, b, c ou d");  
                        }else if (p5=='e' || p5=='E'){              //Se a resposta guardada na variável "p5" for igual a 'e' ou 'E', voltará ao menu.
                            sair = true;
                        } else{                                      //Se a resposta guardada na variável "p5" estiver errada, vai aparecer "Resposta Errada! ...".
                            System.out.println("Resposta Errada! ...");
                            erro++;
                        }
                
                    }while(p5!='a' && p5!='A' && p5!='b' && p5!='B' && p5!='c' && p5!='C' && p5!='d' && p5!='D' && p5!='e' && p5!='E');

                } if (sair == false){
                            //Total de acertos e erros.
                        System.out.println("Total de Acertos: "+acerto);
                        System.out.println("Total de Erros: "+erro);

                    break;
      
                }
            }
            }

        } while (tema!='c' && tema!='C');                           //Se for escolhida a opção 'c' ou 'C' do tema, finalizará o código.

                
        }

    }
