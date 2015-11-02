* Trabalho 2 de Programacao de Computadores I - Retangulo
* Curso de Sistemas da informacao
* Aluno: Filipe Amaral - matricula: 0050013433
* Professor: Alex Salgado
#include <stdio.h>

int main(){
    
    int a=0, l=0;
    int altura, largura;
    int loopRetry = 0;
    char retry, pixel;
    
    while( loopRetry == 0 )
    {
       printf("Informe altura retangulo.\n");
        scanf("%d", &altura);
        printf("Informe largura retangulo.\n");
        scanf("%d", &largura);
        printf("Que simbolo de pixel deseja usar?\n");
        scanf(" %c", &pixel);
        
        printf("Olá, meu nome é Filipe Amaral e seu retangulo ficou assim:\n");
        
        for(a; a<altura; a++)
        {
            for( l; l < largura; l++)
            {
                if( a == 0 || a == altura - 1 || l == 0 || l == largura - 1)
                {
                    printf("%c", pixel);
                }else
                {
                    printf("   ");
                }   
            }
            
            l = 0;
            printf("\n");
        }
        
        printf("Deseja continuar (s/n)?\n");
        scanf(" %c", &retry);
        
        if(retry == 'n')
        {
            loopRetry = 1;
        }
        
        altura = 0;
        largura = 0;
        a = 0;
        
    }

    return 0;
}
