# Jeu

#include <stdio.h>
#include <stdlib.h>

void xp(int *xp)
{
    *xp = 0;
}

void enter_name(){
	char *name;
	int i = 1;
	printf(" Entre ton nom de rappeur\n");
	scanf(" %s", name);
	printf(" \nBienvenue %s dans rentre dans le cercle \n\n", name);
	printf(" pour demarer votre nouvelle carriere de rappeur,\n veuillez vous diriger dans une des directions proposer,\n vous rencontrerez peut-etre un de vos adversaire\n\n\n");

	direction();
}

int ennemis(){
	srand(time(NULL));
	int nb = rand()%5+1;
	f (nb == 1)
		printf("Vous rencontrer EMINEM\n");
	else if (nb == 2)
		printf("Vous rencontrer DAMSO\n");
	else if(nb == 3)
		printf("Vous rencontrer POST MALONE\n");
	else if(nb == 4)
		printf("Vous rencontrer XXX TENTATION\n");
	else if (nb == 5)
		printf("Vous rencontrer KALASH\n");
	return 0;
}

void combat(){
	int combat = 0;
	printf("Vous rencontrer votre adversaire c'est une chance pour vous de prouver ce que vous vallez en BATTLE !\n mai
	vous pouvez aussi fuir et vous ridiculiser devant tout le monde\n alors taper 1 pour combattre ou 2 pour fuir.\n");
	scanf("%d", combat);
	switch(combat){
	case 1:
	ennemis();
	break;
	case 2:
	ennemis();
	break;
	default:
	printf("Veuillez rentrer un nombre valide")
	}
}


	
}

void direction(){
	int direction;

	printf(" Choisissez 1.Est, 2.Ouest, 3.Sud, 4.Nord\n\n");
	scanf(" %d", &direction);

	switch(direction){
		case 1:
		printf(" Vous allez a l'ESt\n");
		ennemis();
		combat();
		break; 

		case 2:
		printf(" Vous allez a l'Ouest\n");
		ennemis();
		combat();
		break;

		case 3:
		printf(" Vous allez au Sud\n");
		ennemis();
		combat();
		break;

		case 4:
		printf(" Vous allez au Nord\n");
		ennemis();
		combat();
		break;

		default:
		printf(" veuillez entrer un nombre valide\n");
		ennemis();
		combat();
		break;
	}
}


void main_menu_choice(){
	int reponse = 0;

	printf( "MAIN MENU\n1. Create New Game\n2. Load Save Game\n3. About\n4. Exit\n");
	scanf("%d", &reponse);
	

	switch(reponse){
		case 1:
		enter_name();
	 	break;
	 	
	 	case 2:
	 	printf(" Charge Game\n");
	 	break;

	 	case 3:
	 	printf(" Parameter\n");
	 	break;

	 	case 4:
	 	printf(" Quit Game\n");
	 	break;

	 	default:
	 	printf(" enter a valid number\n");
	 	break;
	}
}


int main(int argc, char const *argv[])
{

	main_menu_choice();

	return 0;
}


