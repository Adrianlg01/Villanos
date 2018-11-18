#include <stdio.h>
#include <time.h>
#include <unistd.h>
#include <stdlib.h>

#define raya "                                    ==========================================================================================="
#define raya1 "    ======================================================================================================================================================="
#define menu1 "                                   | Villanos  |Nivelde| Vuelo | Fuerza|  Ego  | Mono  | logros|Ingenio| Poder |Audacia|Riqueza|\n"
#define menu2 "   |                               |           | Maldad|       |       |       | logar |       |       | Mental|       |   $   |\n"
#define TOP 10
#define MAX 500

int i,j;
char villanos[MAX][MAX]={
" Jocker    "," Voldemort "," Sindrome  ",
" Magneto   "," Hannibal  ","Darth Vader",
" Kid Bu    "," Venom     "," Mr Burns  ",
" Doomsday  "};
char villanos2[MAX][MAX]={
" Thanos    "," Loki      "," El Buitre  ",
"Zemo       "," Ego        "," Ultron     ",
" Acertijo  "," Steppenwolf"," Malekith   ",
" Galactus  "};

int datos[MAX][MAX]={
{5,0,3,5,5,3,5,0,5,0},
{3,3,2,4,4,4,3,2,3,0},
{2,4,1,4,5,1,5,0,5,0},
{5,5,4,5,3,4,5,2,5,0},
{4,0,3,4,5,2,5,2,4,0},
{4,0,5,3,3,1,3,5,3,2},
{5,5,5,4,0,3,0,0,0,0},
{4,2,5,5,4,2,4,3,3,0},
{1,0,0,3,2,5,5,1,5,5},
{5,0,5,0,0,5,0,0,0,0}};

//declaration prototypes
void menu();
int imprimirtabla();
char cambiartabla();


//programa principal
int main(){
	intro();









}

int intro(){
	int op, op2,a,A,B,b;
	system("cls");
	printf(raya1);
	printf("\n\n\t\t\t\t\t\t\t\tHola, bienvenido a este programa\n");
	printf(raya1);
	men:
	printf("\n\n\t\t ¿Estas listo para crear a el peor villano del Universo?\n");
	
	printf("\n\t\tSi estas listo oprime 1\n");
	
	printf("\t\tSi no te sientes preparado oprime 2\n");
	scanf("%i",&op);
	if(op==1){
		system("cls");
		printf("\n\t\t\t\t\t\t\tA este paso dominaremos el MUNDO\n\n\t\t\t\t\t\t\t ......:::::SIGUEME:::::......\n\n\n\t\t\tEn este momento disponemos de estos temibles villanos\n\n\n");
		imprimirtabla();
	}
		else if(op==2){
			printf("\t\tTal vez aún no tu momento\n\t\tNo te preocupes, tampoco fue facil la primera vez para mi");

			return 0;
			
		}
		else{
			printf("\n\n\t\tCreo que no te entendí, ¿puedes repetirlo?\n");
 
			goto men;
		}
			

	return 0;
		


	
}
void menu(){
    printf(raya);
    printf("\n");
    printf(menu1);
    printf(menu2);
}

int imprimirtabla(){
	int opc;
               menu();
                  for(i=0;i<TOP;i++){
					  
                      printf(raya);
                      printf("\n\t\t\t\t");
                      printf("   |");
                      printf("%s", villanos[i]);
                      printf("|");
                      for(j=0;j<TOP;j++)
                          printf("   %d   |", datos[i][j]);
                          printf("\n");
                  }
				  
                  printf(raya);
              
			  imp:
			  printf("\n\t\t Te gusta lo que ves?");
			  printf("\n\n\t\tSi si preiona 1");
			  printf("\n\t\tSi no presiona 2\n");
			  scanf("%i",&opc);
			  if(opc==1){
				  printf("\n\t\t\tGenial, entonces sigamos(risa muy malvada)");
				  return 0;
			  }
			  else if(opc==2){
				  printf("\n\t\tVale");
				  cambiartabla();
			  }
			  else {
				  printf("Perdona, ¿Lo puedes repetir?");
			  goto imp;
			  }
			  
}
int cambtodatabla(){
	
	int i,j;
for(i=0;TOP;i++){
                        printf(raya);
                        printf("\n");
                        printf("   |");
                        printf("%s", villanos2[i]);
                        printf("|");
                            for(j=0;j<TOP;j++){
                               datos[i][j]=rand()%6;
                               printf("   %d   |", datos[i][j]);
                               }
                               printf("\n");
                        }
}
int cambcaract(){
	int i,j;
for(i=0;TOP;i++){
                        printf(raya);
                        printf("\n");
                        printf("   |");
                        printf("%s", villanos[i]);
                        printf("|");
                            for(j=0;j<TOP;j++){
                               datos[i][j]=rand()%6;
                               printf("   %d   |", datos[i][j]);
                               }
                               printf("\n");
                        }
}
int cambvillan(){
	int i,j;
               menu();
                  for(i=0;i<TOP;i++){
					  
                      printf(raya);
                      printf("\n\t\t\t\t");
                      printf("   |");
                      printf("%s", villanos2[i]);
                      printf("|");
                      for(j=0;j<TOP;j++)
                          printf("   %d   |", datos[i][j]);
                          printf("\n");
                  }
				  
                  printf(raya);
}
int cambvillanesp(){
	int i,j,villan;
	char nombre;
	               menu();
                  for(i=0;i<TOP;i++){
					  
                      printf(raya1);
                      printf("\n\t\t\t\t");
                      printf("Villanos\n\n");
                      printf("%i. %s",i+1, villanos[i]);


				  
                  printf(raya1);
				  }
				  printf("\n¿Cual villano quieres cambiar?");
				  scanf("%i", &villan);
				  villan=i-1;
				  printf("\nCual sera el nuevo nombre\n");
				  scanf("%s",&nombre);
				  villanos[villan][MAX]=nombre;
				  system("cls");
				  
				  menu();
                  for(i=0;i<TOP;i++){
					  
                      printf(raya);
                      printf("\n\t\t\t\t");
                      printf("   |");
                      printf("%s", villanos[i]);
                      printf("|");
                      for(j=0;j<TOP;j++)
                          printf("   %d   |", datos[i][j]);
                          printf("\n");
                  }
				  
                  printf(raya);
				  printf("\n LISTO.....SIGAMOS\n");
				  getchar;
			
				  
}
int cambaleat(){
	



}	



char cambiartabla(){
              char opcion,opcion2,opcion3,a,b,c;
              int dato;
			  do{
              printf("\n\nCambiar datos:\n");
              printf("a -> aleatoriamente\n");
              printf("b -> configuracion personal\n");
			  printf("c -> regresar a la página anterior");
			  scanf("%c",&opcion);
			  }while(opcion==a||opcion==b||opcion==c);
			  switch(opcion){
				 case 'a':
				 printf("\n\t\t ¿Que quieres cambiar?\n");
				 printf("\t1 -> Toda la tabla\n");
				 printf("\t2 -> Las características de todos los villanos\n");
				 printf("\t3 -> Todos los supervillanos\n");
				 printf("\t4 -> Una villano específico\n");
				 printf("\t5 -> Una característica específica\n");
				 break;
				 switch(opcion2){
					case '1':
					cambtodatabla();
					break;
					case '2':
					cambcaract();
					break;
					case '3':
					cambvillan();
					break;
					case '4':
					cambvillanesp();
					break;
					
					

				 case 'b':
				 
                 printf("\n\t\t ¿Que quieres cambiar?\n");
                 printf("\t1 -> Toda la tabla\n");
                 printf("\t2 -> Solo supervillanos\n");
				 printf("\t3 -> El nombre de un supervillano\n");
				 printf("\t4 -> Una casilla especifica\n");
				 printf("\t5 -> Todo un renglón\n");
                 setbuf(stdin,NULL);
                 scanf("%c",&opcion2);
                 scanf("%d",&dato);
				 break;
                 switch(opcion2){
                        case 'd':
                        todatabla();
                        break;
                        case'e':
                        printf("Elige al villano que quieres cambiar:\n");
                        printf("Oprime:\n");
                        printf("a -> Jocker\n");
                        printf("b -> Voldemort\n");
                        printf("c -> Sindrome\n");
                        printf("d -> Magneto\n");
                        printf("e -> Hannibal\n");
                        printf("f -> Darth Vader\n");
                        printf("g -> Kid Bu\n");
                        printf("h -> Venom\n");
                        printf("i -> Mr Burns\n");
                        printf("j -> Doomsday\n");

                        scanf("%c",&opcion3);
                             switch(opcion3){
                                   case 'a':
                                   printf(raya);
                                   printf("\n");
                                   printf("   |");
                                   printf("%s", villanos[0]);
                                   printf("|");
                                   for(j=0;j<TOP;j++){
                                      datos[1][j]=rand()%6;
                                      printf("   %d   |", datos[0][j]);
                                      }
                                      printf("\n");
                                      printf(raya);
                                      printf("\n");
                                   break;
                                   default:
                                   printf("Opcion no valida\n");
                                   break;
                                   }
                          break;
                          default:
                          printf("Opcion no valid\n");
                          break;
                        }
                }
          }
}
