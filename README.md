/* fruitshop
First C program */

#include <stdio.h>

int main() {
    /*Variable Declaration*/
    
    int O,A,P;
    int price,budget,remain_budget;
    char option;
    
    
    /*Items Structure & Prefixes*/
    
    printf("*** ItemPrefixes ***\t");
    printf("\nO: Orange\nA: Apple\nP: Pear\n");
    printf("********************\n");
    
    /*Shopkeeper Panel & Product Price Declaration*/
    
    
    printf("\n*** SHOPKEEPER PANEL ***\n");
    
    
    printf("Please enter apple price: £");
    scanf(" %d", &A);
    printf("\nPlease enter orange price: £");
    scanf(" %d", &O);
    printf("\nPlease enter pear price: £");
    scanf(" %d", &P);
    
    
    /*  Shop Menu Items & Prices List   */
    
    printf("\n***** Shop Menu *****\n");
    printf("Item: \t Price \n A: \t £%d \n O: \t £%d \n P: \t £%d\n", O,A,P);
    
    
    /*  Customer Panel & Budget Declaration */
    
    printf("\n*** CUSTOMER PANEL ***\n");
    printf("Please Enter your budget:£");
    scanf(" %d",&budget);
    
    /* Add to Basket Option */
    
    printf("Please enter ItemPrefix from the Menu to purchase: ");
    scanf(" %c", &option);
    
    
    /* Purchase Calculation - Evaluation Against the Available Items & Prices */
    
    /* First Item */
    
    if (option == 'A'){
        
    /*Item Price Comparison against The Allocated Budget & Result  */
        
        price = A;
        if(budget < price){
            printf("\nPURCHASE FAILED!\nLow budget or missing item\n");
            printf("\nThanks for shopping with us!\n");
        }
       else {
        remain_budget= budget - price;
        printf("\nPURCHASE SUCCESS!\nPurchase details\n");
        printf("-----------------\n");
        printf(" Item: A \n Price: £%d \n Remaining budget: £%d \n \n Thanks for shopping with us! ",price,remain_budget);
       }
    }
    
    /*Second Item */
    
    else if (option == 'O'){
        price = O;
        
    /*Item Price Comparison against The Allocated Budget & Result  */
        
        if(budget < price){
            printf("\nPURCHASE FAILED!\nLow budget or missing item\n");
            printf("\nThanks for shopping with us!\n");
        }
       else {
        remain_budget= budget - price;
        printf("\nPURCHASE SUCCESS!\nPurchase details\n");
        printf("-----------------\n");
        printf(" Item: O \n Price: £%d \n Remaining budget: £%d \n \n Thanks for shopping with us! ",price,remain_budget);
        }
    }
    
    
    /*Third Item */
    
     else if (option == 'P'){
        price = P;
        
    /*Item Price Comparison against The Allocated Budget & Result  */
     
        if(budget < price){
            printf("\nPURCHASE FAILED!\nLow budget or missing item\n");
            printf("\nThanks for shopping with us!\n");
        }
       else {
        remain_budget= budget - price;
        printf("\nPURCHASE SUCCESS!\nPurchase details\n");
        printf("-----------------\n");
        printf(" Item: P \n Price: £%d \n Remaining budget: £%d \n \n Thanks for shopping with us! ",price,remain_budget);
        }
    }
    
    /* Wrong Input or Item Missing from the List Statement */
    
    else{
        printf("\nPURCHASE FAILED!\nLow budget or missing item\n");
            printf("\nThanks for shopping with us!\n");
        
    }
    
    

    return 0;
}



