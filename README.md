# Proyecto_Taller_Parqueo
de<iostream>
#include<cstdlib>

using namespace std;


de<iostream>
#include<cstdlib>

using namespace std;


int main()
{
int numero;

	
//Elimina todas las cosas que se imprimieron 
system("cls");
	
cout<<"       Menu\n 1.Configuracion\n 2.Dinero del cajero \n 3.Entrada de vehiculo\n 4.Cajero del parqueo\n 5.Salida de vehiculo\n 6.Ayuda\n 7.Acerca de\n 8.Salir\n";
			
cout<<"\n Ingrese la accion que desea realizar:";
cin>>numero;
			
switch(numero)
{
	case 1:
		system("cls");
		cout<<"Configuracion\n";
		system("pause");
	break;
			
	case 2:
		system("cls");
		cout<<"   Dinero del cajero\n";
		dinero_del_cajero();
		system("pause");
	break;
			
	case 3:
		system("cls");
		cout<<"Entrada de vehiculo\n";
		system("pause");
	break;
			
	case 4:
		system("cls");
		cout<<"Cajero del parqueo\n";
		system("pause");
	break;
			
	case 5:
		system("cls");
		cout<<"Salida de vehiculo\n";
		system("pause");
	break;
			
	case 6:
		system("cls");
		cout<<"Ayuda\n";
		system("pause");
	break;
			
	case 7:
		system("cls");
		cout<<"Acerca de\n";
		system("pause");
	break;
			
	case 8:
		system("cls");
		cout<<"Salir\n";
		system("pause");
	break;
			
	default:
		system("cls");
		cout<<"ERROR: El dato no es correcto\n";
		system("pause");
		//Lama a la funcion principal 
		main();
	break;
			
	}	

	
return 0;
}
//Esto es un comentaio de una linea


/*
Esto
es un 
comentario de varias lineas
*/
