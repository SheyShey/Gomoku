# Gomoku
/* CODE DE PROGRAMMATION DU JEU GOMOKU POUR LE PROJET DU COURS ALGORITHMIQUE DE L'EPF
de Sheryleen GIBBS et Janice PRAXEL */

// Bibliothèque:
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#define L 11
#define M 11


    /* void color (int couleurDuTexte, int couleurDeFond);

         {  HANDLE H=GetStdHandle(STD_OUTPUT_HANDLE);
            SetConsoleTextAttribute(H,couleurDeFond*16+couleurDuTexte);
}*/

// Definition des différentes fonctions du programme //
void regles();
void info();
void affichegetab();
void deplacement (int *);



int main()

{
    // Initialisation du tableau //
char tableau [11] [11] =
{
    {'0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '10'},
    {'1', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'2', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'3', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'4', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'5', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'6', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'7', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'8', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'9', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
    {'10', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B', 'B'},
};


     // Programmation du MENU muni de 3 choix possibles par l'utilisateur //
    printf("____________________________________________________________________________________________________________________________________________________________________________\n\n\n");
            printf("                                                                               GOMOKU\n\n\n");
    printf("____________________________________________________________________________________________________________________________________________________________________________\n\n\n");

            printf("\n\n\n Pour apprendre a jouer, direction les règles du jeu !!!\n\n\n");
            int c;
            int nb;
            int x=1;
            do
            {
                printf ("Que voulez-vous faire ? : \n 1 : Jeu \n 2 : Règles \n3 : Credits\n Votre choix :");
                scanf("%d",&nb);
                switch(nb)
                {
                case 1 :
                    while(x==1)
                    {
                        affichagetab();
                        deplacement(&x);
                    }
                    break;

                case 2 :
                    regles();
                    break;

                case 3:
                    info();
                    break;

                default :
                    fprintf(stderr, "ERREUR : Ce nombre n'est pas attribue a un choix\n");
                    return -1;
                }

                printf("Souhaitez-vous continuer ? (o/n)");
                getchar();
                scanf("%c",&c);
            }
            while (c =='c'||c == 'o');
            return 0;


}
void deplacment (int* n)
{
    int t=1;
    n*=t;
    int b;
    int l;
    int c;
    printf("Entrez le numero de la ligne choix: /n ");
    scanf("%d",&l);
    printf ("Entrez le numero de la colonne: /n");
    scanf("%d",&c);


}
