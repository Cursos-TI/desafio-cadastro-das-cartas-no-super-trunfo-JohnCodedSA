#include <stdio.h>

int main() {
    //Declarando variáveis.
    
    // Primeira carta
    char estado1, codigo1[4], cidade1[50];
    unsigned long int populacao1;
    float area1, pib1;
    int pontosturisticos1;
    float densidadepopulacional1, pibpercapita1, superpoder1;
    
    
    // Segunda carta
    char estado2, codigo2[4], cidade2[50];
    unsigned long int populacao2;
    float area2, pib2;
    int pontosturisticos2;
    float densidadepopulacional2, pibpercapita2, superpoder2;

    // Cadastro da primeira carta
    printf("\nInsira os dados da carta 1\n");
    
    printf("\nDigite o estado (A-H): ");
    scanf(" %c", &estado1); // Espaço antes de %c para evitar problemas com buffer
    
    printf("Digite o código da carta (ex: A01,B02): ");
    scanf("%s", &codigo1);
    
    printf("Digite o nome da cidade: ");
    scanf("%s", &cidade1);
    
    printf("População: ");
    scanf("%lu", &populacao1);
    
    printf("Área (em km²): ");
    scanf("%f", &area1);
    
    printf("PIB: ");
    scanf("%f", &pib1);
    
    printf("Número de pontos turísticos: ");
    scanf("%d", &pontosturisticos1);

    // Calculo da densidade populacional e pib per capita da primeira carta
    densidadepopulacional1 = populacao1 / area1;
    pibpercapita1 = (pib1 * 1.0e9) / populacao1;
    
    // Calculo do Super Poder da primeira carta 
    superpoder1 = (float)populacao1 + area1 + pib1 + pontosturisticos1 + pibpercapita1 + (1.0 / densidadepopulacional1); // 1.0 forçando a operação a ser feita em ponto flutuante
   
    // Cadastro da segunda carta
    printf("\nInsira os dados da carta 2\n");
    
    printf("\nDigite o estado (A-H): ");
    scanf(" %c", &estado2); // Espaço antes de %c para evitar problemas com buffer
    
    printf("Digite o código da carta (ex: A01,B02): ");
    scanf("%s", &codigo2);
    
    printf("Digite o nome da cidade: ");
    scanf("%s", &cidade2);
    
    printf("População: ");
    scanf("%lu", &populacao2);
    
    printf("Área (em km²): ");
    scanf("%f", &area2);
    
    printf("PIB: ");
    scanf("%f", &pib2);
    
    printf("Número de pontos turísticos: ");
    scanf("%d", &pontosturisticos2);


    // Calculo da densidade populacional e pib per capita da segunda carta
    densidadepopulacional2 = populacao2 / area2;
    pibpercapita2 = (pib2 * 1.0e9) / populacao2;

    // Calculo do Super Poder da segunda carta
    superpoder2 = (float)populacao2 + area2 + pib2 + pontosturisticos2 + pibpercapita2 + (1.0 / densidadepopulacional2); // 1.0 forçando a operação a ser feita em ponto flutuante
    
    
    // Exibição dos dados da primeira carta
    printf("\n*** Carta 1 ***\n");
    printf("Estado: %c\n", estado1);
    printf("Código: %s\n", codigo1);
    printf("Nome da Cidade: %s\n", cidade1);
    printf("População: %lu\n", populacao1);
    printf("Área: %.2f km²\n", area1);
    printf("PIB: %.2f bilhões de reais\n", pib1);
    printf("Número de Pontos Turísticos: %d\n", pontosturisticos1);
    printf("Densidade Populacional: %.2f hab/km²\n", densidadepopulacional1);
    printf("PIB per Capita: %.2f reais\n", pibpercapita1);
    
    // Exibição dos dados da segunda carta
    printf("\n*** Carta 2 ***\n");
    printf("Estado: %c\n", estado2);
    printf("Código: %s\n", codigo2);
    printf("Nome da Cidade: %s\n", cidade2);
    printf("População: %lu\n", populacao2);
    printf("Área: %.2f km²\n", area2);
    printf("PIB: %.2f bilhões de reais\n", pib2);
    printf("Número de Pontos Turísticos: %d\n", pontosturisticos2);
    printf("Densidade Populacional: %.2f hab/km²\n", densidadepopulacional2);
    printf("PIB per Capita: %.2f reais\n", pibpercapita2);
   
    // Comparação dos atributos
    // 1:2: Determina qual carta venceu a comparação e 1:0 Imprime quem venceu de maneira simples
    printf("\n~~~~ Comparação das Cartas ~~~~\n");
    printf("População: Carta %d Venceu (%d)\n", (populacao1 > populacao2) ? 1 : 2, (populacao1 > populacao2) ? 1 : 0);
    printf("Área: Carta %d Venceu (%d)\n", (area1 > area2) ? 1 : 2, (area1 > area2) ? 1 : 0 );
    printf("PIB: Carta %d Venceu (%d)\n", (pib1 > pib2) ? 1 : 2, (pib1 > pib2) ? 1 : 0);
    printf("Pontos Turísticos: Carta %d venceu (%d)\n", (pontosturisticos1 > pontosturisticos2) ? 1 : 2, (pontosturisticos1 > pontosturisticos2) ? 1 : 0);
    printf("Densidade Populacional: Carta %d venceu (%d)\n", (densidadepopulacional1 < densidadepopulacional2) ? 1 : 2, (densidadepopulacional1 < densidadepopulacional2) ? 1 : 0);
    printf("PIB per Capita: Carta %d venceu (%d)\n", (pibpercapita1 > pibpercapita2) ? 1 : 2, (pibpercapita1 > pibpercapita2) ? 1 : 0);
    printf("Super Poder: Carta %d venceu (%d)\n", (superpoder1 > superpoder2) ? 1 : 2, (superpoder1 > superpoder2) ? 1 : 0);
    
    return 0;
}