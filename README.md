/* Votação de vereadores e prefeitos em linguagem c, utilizando switch dentro de switch.*/
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

	int vJoao  = 0, vMaria = 0, vZe = 0, nulo = 0, vInvalido = 0;
	int dZureta = 0, sGomes = 0, vNulo = 0, vinvalido = 0;
	
int main()
{	setlocale(LC_ALL,"Portuguese");
	int menu = 0;
	int opcao_vereador, opcao_prefeito;
	
	system("cls");
	printf("-------------MENU-----------:  ");
	printf("\n O QUE VOCE DESEJA FAZER?: ");
	printf("\n 1 - Votar: ");
	printf("\n 2 - Apurar Votos: ");
	printf("\n 3 - Sair:");
	printf("\n---------------------------: ");
	printf("\n-->");
	scanf("%i", &menu);
	fflush(stdin);
  /* opções de menu*/
	
	switch (menu)	{
	case 1 :
  /* escolha do candidato a vereador */
	 	system("cls");
	 	printf("\n Escolha seu Candidato");
		printf("\n------VOTAÇÃO-VEREADOR------:  ");
		printf("\n 111 - Joao do Frete: ");
		printf("\n 222 - Maria da Pamonha: ");
		printf("\n 333 - Ze da Farmacia: ");
		printf("\n 444 - Voto Nulo: ");
		printf("\n-----------------------------: ");
		printf("\n-->");
		scanf("%i", &opcao_vereador);
		fflush(stdin);
		system("cls");
		switch (opcao_vereador)
		{
			case 111:
				printf("\n Voto confirmado em Joao do Frete \n");
				vJoao = vJoao + 1;
				break;
			case 222:
				printf("\n Voto confirmado em Maria da Pamonha\n");
				vMaria = vMaria + 1;				
				break;
			case 333:
				printf("\n Voto confirmado em Ze da Farmacia\n");
				vZe = vZe + 1;	
				break;
			case 444:
				printf("\n Voto Nulo\n");
				nulo = nulo + 1;
				break;			
			default:
				printf("Voto invalido\n");
				vInvalido = vInvalido + 1;
				break;
		}
    /* escolha de candidato a prefeito*/
		fflush(stdin);
		system("pause");
		system("cls");
		printf("--------VOTAÇAO-PREFEITO--------:  ");
		printf("\n 11 - Dr. Zureta: ");
		printf("\n 22 - Senhor Gomes: ");
		printf("\n 44 - Nulo: ");
		printf("\n-->");
		scanf("%d", &opcao_prefeito);
		fflush(stdin);
		switch (opcao_prefeito)
		{
			case 11:
				printf("\n Voto confirmado em Dr. Zureta\n");
				dZureta= dZureta + 1;
				break;
			case 22 :
				printf("\n Voto confirmado em Senhor Gomes\n");
				sGomes = sGomes + 1;
				break;
			case 44 :
				printf("\n Voto NULO\n");
				vNulo = vNulo + 1;
				break;
			default:
				vinvalido = vinvalido + 1;
				break;				
		}
		printf("Pressione Enter para continuar...: \n");
		system("pause");
		fflush(stdin);
		main();
    /* apuração de votos*/
						
	case 2:
	system("cls");
		printf("--------APURAÇAO DE VOTOS---------");
		printf("--------VEREADORES--------:  ");
		printf("\n Vereador Joao do Frete : %d votos.\n", vJoao);
		printf("\n Vereador Maria da Pamonha : %d votos.\n", vMaria);
		printf("\n Vereador Ze da Farmacia : %d votos.\n", vZe);
		printf("\n Votos Nulos : %d votos.\n", nulo);
		printf("\n Votos Inválidos : %d votos.\n", vInvalido);
		printf("\n--------PREFEITOS--------:  ");
		printf("\n Prefeito Dr.Zureta : %d votos.\n", dZureta);
		printf("\n Prefeito Senhor Gomes : %d votos.\n", sGomes);
		printf("\n Voto Nulos: %d votos.\n", vNulo);
		printf("\n Votos Inválidos : %d votos.\n", vinvalido);
		printf("\n----------------------------------\n: ");
		
		printf("\n Pressione Enter para continuar...: ");
 		system("pause");
		main();
	    break;		
	
	case 3:
		printf("Finalizando o Programa...\n");
		exit(0);
		break;
	default:
		printf("Opção Invalida, Tente Novamente...\n");
		system("pause");
		fflush(stdin);	
	    main();
        break;
    }
    return(0);
}

