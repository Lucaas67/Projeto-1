//Nome: Lucas Gabriel Neves Pereira
//Matrícula: UC21102392
//Curso: Engenharia de software 

#include<stdio.h> //Biblioteca de entrada e saída (printf e scanf)
#include<locale.h> //Especifica constantes de acordo com a localização específica, como moeda, data, etc.
#include<ctype.h> //Funções para conversão de maiúsculas, minúsculas e outros tratamentos de caracteres.
#include<string.h> //Biblioteca para trabalhar com strings
#include<stdlib.h> //Biblioteca para limpar a tela
int main(){
	int sessao, pessoas, homens=0, mulheres=0, ingresso, idade, crianca=0, adolescente=0, adulto=0, idoso=0, precoDoIngresso, faturamento, nada, deMaiorMasculino=0, deMaiorFeminino=0, i=0; 
	char filme[50];
	char nome[50];
	char sexo;
	setlocale (LC_ALL, "Portuguese"); //para o uso de acentos e mais
	
	printf("=================================================\n");
	printf("Bem-vindo ao programa de verificação das sessões!\n");
	printf("=================================================\n");
	
	do{ //Comando de repetição em caso de erro
	printf("Número de sessões: "); //Apresenta texto na tela
	scanf("%i", &sessao); //Armazenar o que o usuário digitou na respectiva variável;
	fflush(stdin); //Limpa o lixo na memória
	}while(sessao != 2); //repetição quando não for verdadeiro
	
	do{ //Comando de repetição em caso de erro
	printf("Nome do filme: "); //Apresenta texto na tela
	fgets(filme,50,stdin); //Recebe string com espaçamento. 
	fflush(stdin); //Limpa o lixo na memória
	if (strlen(filme) <= 2) //strlen: verifica o tamanho da string, se for "vazio", apresenta o erro
	printf("Este filme não existe!\n"); //Apresenta texto na tela
	else 
	filme;
	}while(strlen(filme) <= 2); //repetição quando não for verdadeiro
	
	do{ //Comando de repetição em caso de erro
	printf("Número de pessoas que assistiram ao filme: "); //Apresenta texto na tela
	scanf("%i", &pessoas); //Armazenar o que o usuário digitou na respectiva variável;
	fflush(stdin); //Limpa o lixo na memória
	}while(pessoas < 10); //repetição quando não for verdadeiro
	
	//Nova função adicionada
	faturamento = pessoas*20;//Saber quanto a sessão rendeu, 20 é o preço do ingresso (20 reais). obs: sem meia entrada.
	
	for(int i = 0; i < pessoas; i++) { //Estrutura de repetição que irá realizar a quantidade de vezes que foi informado pelo usuário em "pessoas"
	system("cls"); //Comando para limpar a tela 
	
	do{ //Primeiro do-while - responsável por permitir ao usuário digitar os dados de várias pessoas
		
		do{ //Comando de repetição em caso de erro
		printf("Digite o nome do espectador: "); //Apresenta texto na tela
		fgets(nome,50,stdin); //Recebe string com espaçamento. 
		fflush(stdin); //Limpa o lixo na memória
		nome[strlen(nome) - 1] = '\0'; //Para dar erro se estiver "vazio", strlen: verifica o tamanho da string
		}while (strlen(nome) == 0); //Correspondente verdadeira, strlen: verifica o tamanho da string
		
		do{ //Comando de repetição em caso de erro
		printf("Digite o sexo (M para masculino e F para feminino): "); //Apresenta texto na tela
		scanf("%c", &sexo); //Armazenar o que o usuário digitou na respectiva variável;
		sexo = toupper(sexo); //Colocar a letra digitada em maiúsculo
		fflush(stdin); //Limpa o lixo na memória
		if (sexo == 'M') //Correspondente se o sexo for masculino = M
		homens++; //Incrimentar na respectiva variável
		else if (sexo == 'F') //Correspondente se o sexo for feminino = f
		mulheres++; //Incrimentar na respectiva variável
		else 
		nada++; //Incrimentar na respectiva variável
		}while ((sexo == 'M') && (sexo == 'F'));
		
		
		printf("Digite a idade: "); //Apresenta texto na tela
		scanf("%i", &idade); //Armazenar o que o usuário digitou na respectiva variável;
		fflush(stdin); //Limpa o lixo na memória
		if((idade >= 3) && (idade <= 13)) //If-else para corresponder a tabela de idade
		crianca++; //Incrimentar na respectiva variável
		else if ((idade >= 14) && (idade <= 17)) //If-else para corresponder a tabela de idade
		adolescente++; //Incrimentar na respectiva variável
		else if ((idade >= 18) && (idade <= 64)) //If-else para corresponder a tabela de idade
		adulto++; //Incrimentar na respectiva variável
		else if((idade >= 65) && (idade <= 100)) //If-else para corresponder a tabela de idade
		idoso++; //Incrimentar na respectiva variável
		else
		nada++; //Incrimentar na respectiva variável
	
	//Para mostrar os espectadores +18
		if(idade >= 18 && sexo=='M'){
			deMaiorMasculino++; //Incrimentar na respectiva variável
		}else
		if(idade >= 18 && sexo=='F'){ 
			deMaiorFeminino++; //Incrimentar na respectiva variável
	}
		
	}while((idade <= 100) && ((sexo == 'M') && (sexo == 'F')) && (strlen(nome) == 0) && (ingresso > 1)); //Do- while geral, corresponde a todas as correspondentes verdadeiras.
	}
	
	system("cls"); //Comando para limpar a tela
	
	//Tabela de informações exigidas
	
	printf("=================================================\n");
	printf("Filme: %s\n ", filme); //Mostrar o nome do filme
	printf("Pessoas do sexo feminino: %i\n ", mulheres); //Mostrar a quantidade de pessoas do sexo feminino
	printf("Pessoas do sexo masculino: %i\n ", homens); //Mostrar a quantidade de pessoas do sexo masculino
	printf("Quantidade de crianças: %i\n ", crianca); //Mostrar a quantidade de crianças
	printf("Quantidade de adolescentes: %i\n ", adolescente); //Mostrar a quantidade de adolescentes
	printf("Quantidade de adultos: %i\n ", adulto); //Mostrar a quantidade de adultos
	printf("Quantidade de idosos: %i\n ", idoso); //Mostrar a quantidade de idosos
	printf("Faturamento do filme: R$ %i,00\n", faturamento); //Mostrar o faturamento do cinema com o filme
	printf("=================================================\n");
	
	printf("\n=================================================\n");
	printf("Pessoas maiores de 18 anos do sexo feminino: %i\n", deMaiorFeminino); //Mostrar a quantidade de pessoas do sexo feminino maior de 18 anos
	printf("Pessoas maiores de 18 anos do sexo masculino: %i\n", deMaiorMasculino); //Mostrar a quantidade de pessoas do sexo masculino maior de 18 anosprintf(" =================================================\n");
	printf("=================================================\n");
	
	return 0; //Retorno da função
}
