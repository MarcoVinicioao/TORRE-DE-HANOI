
#include <iostream>
#include <stdlib.h> 
#include <stdio.h> 

using namespace std;

int paso = 1;
void mover_disco(int disco, char Torre1, char Torre2, char Torre3){    
system("color 3F");          
	if (disco==1){
		cout<<"\tMover disco "<<disco<<" de la torre "<<Torre1<<" hacia la torre "<<Torre3<<endl;
	}else{
		mover_disco(disco-1, Torre1,Torre3,Torre2);
		cout<<endl;
		cout<<"\tMOVIMIENTO "<<paso++<< "\n ";
		cout<<endl;
		cout<<"\tMover disco "<<disco<<" de la torre "<<Torre1<<" hacia la torre "<<Torre3<<endl;
		cout<<endl;
		cout<<"\tMOVIMIENTO "<<paso++<<endl;
		cout<<endl;
		mover_disco(disco-1,Torre2,Torre1,Torre3);
	}
}

int main(){

system("color 4F");
	int discos;
	char respuesta;
	cout<<"\n\                    **************************  PROYECTO TORRE DE HANOI ***********************\n\n"<<endl;


cout<<endl;	
	
cout<<"                                      0900 17 8658   Jose Roberto Lima Klee\n";                              
cout<<"                                      9941 16 15499   Hipolito Marco Vinicio Aguilar Oscal\n";                               
cout<<"                                      20900-18-5001 Juan Diego Albizurez Rivas\n\n\n"<<endl;
cout<<"\t                                  Los numeros representan los discos."<<endl;
	cout<<"\n\n";
	
	cout<<"\n\                      tLas letras representan las torres: A = Origen, B = Pivote, C = Destino.\n\n"<<endl;
cout<<"                                  ****                                                                       "<<endl;
cout<<"                                 ******                ****                                                      "<<endl;
cout<<"                                *********             ******            ***                                             "<<endl;
cout<<"                               ***********           ********          *****                                         "<<endl;
cout<<"                             ***************        **********        *******                                               "<<endl;
	do{
	cout<<"\nIngrese el numero de discos con los que desea jugar: "<<endl;
	cin>>discos;
	system("cls");
	cout<<endl;
	cout<<"\tMOVIMIENTO "<<paso++<<"\n";
	cout<<endl;
	mover_disco(discos,'A','B','C');	
	cout<<"\n\nSi desea volver a jugar ingrese la letra s:  ";
	cin>>respuesta;
	
    }while(respuesta == 's'); 

	return 0;
	
}
