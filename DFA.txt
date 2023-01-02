#include<stdio.h>

int main(){
    int tt[5][2],st=0,len;
    char inp[100];
    tt[0][0]=1;
    tt[0][1]=3;
    tt[1][0]=2;
    tt[1][1]=2;
    tt[2][0]=2;
    tt[2][1]=2;
    tt[3][0]=4;
    tt[3][1]=3;
    tt[4][0]=4;
    tt[4][1]=3;
    printf("transition table\n");
    printf("state\ta\tb");
    
    
    for(int i=0; i<5; i++){
        printf("\n%d",i);
        for(int j=0; j<2;j++){
            printf("\t%d", tt[i][j]);
            
        }
    }

    printf("\n enter length of string: ");
    scanf("%d",&len);
    printf("\n enter input string :");
    scanf("%s", inp);
    printf("\n sequence of transition \n");
    for (int i =0; i< len; i++){
        printf("state=%d->input = %c->",5,inp[i]);
       if(inp[i]=='a')
        st= tt[st][0];
        else if (inp[i]=='b')
        st = tt[st][1];
        else {
            st=-1;
            break;
        }
        printf("state=%d\n",st);
        
    }
    if(st==2 || st ==4)
    printf("\n valid\n");
    else printf("\n Invalid\n");
    
    
}
