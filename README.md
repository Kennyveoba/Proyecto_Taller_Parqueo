# Proyecto_Taller_Parqueo
de<iostream>
#include<cstdlib>

using namespace std;
//___________________________Dinero_del_cajero___________________________________________________________________________________________________________________

//Funcion Saldo del cajero 
saldo_del_cajero()
{
	int x;
	cout<<"Saldo del cajero";
	cin>>x;
}

//Funcion ingresos_del_cajero
ingresos_del_cajero()
{
	int x;
	cout<<"Ingresos del cajero";
	cin>>x;	
}


//Funcion cargar cajero 
cargar_cajero()
{	
	int x;
	cout<<"cargar cajero";
	cin>>x;
}


//Funcion dinero del cajero
dinero_del_cajero()
{
	int opcion;
	system("cls");
	cout<<"   Dinero del cajero\n";
	cout<<"\n 1.Cargar cajero\n 2.Saldo del cajero\n 3.Ingresos del cajero\n 4.Atras\n\n Digite la opcion que desea realizar:";
	cin>>opcion;
	switch(opcion)
	{
		case 1:
			system("cls");
			cargar_cajero();
			dinero_del_cajero();
		break;
		
		case 2:
			system("cls");
			saldo_del_cajero();
			dinero_del_cajero();
		break;
		
		case 3:
			system("cls");
			ingresos_del_cajero();
			dinero_del_cajero();
		break;
		
		case 4:
			system("cls");
		break;
		
		default:
			system("cls");
			cout<<"ERROR: El dato no es correcto\n";
			//Lama a la funcion principal 
			system("pause");
			dinero_del_cajero();
			
		break;
		
		
			
	}
	
}

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
	break;
			
	case 2:
		system("cls");
		dinero_del_cajero();
	break;
			
	case 3:
		system("cls");
		cout<<"Entrada de vehiculo\n";
	break;
			
	case 4:
		system("cls");
		cout<<"Cajero del parqueo\n";
	break;
			
	case 5:
		system("cls");
		cout<<"Salida de vehiculo\n";
	break;
			
	case 6:
		system("cls");
		cout<<"Ayuda\n";
	break;
			
	case 7:
		system("cls");
		cout<<"Acerca de\n";
	break;
			
	case 8:
		system("cls");
		return 0;
	break;
			
	default:
		system("cls");
		cout<<"ERROR: El dato no es correcto\n";
		system("pause");
		//Lama a la funcion principal 
		main();
	break;
		
	}	

main();	
return 0;
}
//Esto es un comentaio de una linea


/*
Esto
es un 
comentario de varias lineas
*/
