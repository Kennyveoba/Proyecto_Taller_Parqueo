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
	

	
	//clrscr
	system("cls");
	
	cout<<"       Menu\n 1.Configuracion\n 2.Dinero del cajero \n 3.Entrada de vehiculo\n 4.Cajero del parqueo\n 5.Salida de vehiculo\n 6.Ayuda\n 7.Acerca de\n 8.Salir\n";
			
	cout<<"\n Ingrese la accion que desea realizar:";
	cin>>numero;
			
	switch(numero)
	{
		case 1:
			//clrscr
			system("cls");
			cout<<"Configuracion\n";
			system("pause");
		break;
			
		case 2:
			//clrscr
			system("cls");
			cout<<"   Dinero del cajero\n";
			dinero_del_cajero();
			system("pause");
		break;
			
		case 3:
			//clrscr
			system("cls");
			cout<<"Entrada de vehiculo\n";
			system("pause");
		break;
			
		case 4:
			//clrscr
			system("cls");
			cout<<"Cajero del parqueo\n";
			system("pause");
		break;
			
		case 5:
			//clrscr
			system("cls");
			cout<<"Salida de vehiculo\n";
			system("pause");
		break;
			
		case 6:
			//clrscr
			system("cls");
			cout<<"Ayuda\n";
			system("pause");
		break;
			
		case 7:
			//clrscr
			system("cls");
			cout<<"Acerca de\n";
			system("pause");
		break;
			
		case 8:
			//clrscr
			system("cls");
			cout<<"Salir\n";
			system("pause");
		break;
			
		default:
			//clrscr
			system("cls");
			cout<<"ERROR: El dato no es correcto\n";
			system("pause");
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
