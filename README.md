# Proyecto_Taller_Parqueo
//Programa 4: Parqueo C++
#include<iostream>
#include<vector>
using namespace std;
	
	
//Falta documentacion de la funcion de continuar
//Variables globales para usar en el programa


vector<int>parqueo;//Este vector puede cambiar segun que metodo usemos como vectores
float precioxhora;
int pago_minimo;
int redondeo;
int min_max;
int modena_1;
int modena_2;
int modena_3;
int billete_1;
int billete_2;
int billete_3;
int billete_4;
int billete_5;



int configuracion()
{	
	int espacios_config;
	float precioxhora_config;
	int pago_minimo_config;
	int redondeo_config;
	int min_max_config;
	int modena_1_config;
	int modena_2_config;
	int modena_3_config;
	int billete_1_config;
	int billete_2_config;
	int billete_3_config;
	int billete_4_config;
	int billete_5_config;
	
	//----------------------------------------------------------
	cout<<"La cantidad de espacios del parqueo: ";
	cin>>espacios_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Precio por hora: ";
	cin>>precioxhora_config;
	cout<<" \n";
	
	//----------------------------------------------------------
	cout<<"Pago minimo: ";
	cin>>pago_minimo_config;
	cout<<" \n";
	
	

	//----------------------------------------------------------
	cout<<"Redondeo al combro a los siguientes minutos: ";
	cin>>redondeo_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Minutos maximos para salir despues del pago: ";
	cin>>min_max_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Moneda 1: ";
	cin>>modena_1_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Moneda 2: ";
	cin>>modena_2_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Moneda 3: ";
	cin>>modena_3_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Billete 1: ";
	cin>>billete_1_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Billete 2: ";
	cin>>billete_2_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Billete 3: ";
	cin>>billete_3_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Billete 4: ";
	cin>>billete_4_config;
	cout<<" \n";
	
	
	//----------------------------------------------------------
	cout<<"Billete 5: ";
	cin>>billete_5_config;
	cout<<" \n";
	
	
	bool fallo;
	fallo=true;
	
	while (fallo==true)
	{
		if (espacios_config<1)
		{cout<<" \n";
		cout<<"ERROR: La cantidad de espacios debe ser >= 1\n";
		cout<<"Valor que le asigno: "<<espacios_config;
		cout<<"\nLa cantidad de espacios del parqueo:";
		cin>>espacios_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
		
		
		
		//-----------------------------------------------------------	
		if (precioxhora_config<0)
		{cout<<" \n";
		cout<<"ERROR: El precio por hora debe ser >= 0\n";
		cout<<"Valor que le asigno: "<<precioxhora_config;
		cout<<"\nPrecio por hora:";
		cin>>precioxhora_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
			
			
			
		//----------------------------------------------------------
		if (pago_minimo_config<0)
		{cout<<" \n";
		cout<<"ERROR: El pago minimo debe ser >= 0\n";
		cout<<"Valor que le asigno: "<<pago_minimo_config;
		cout<<"\nPago minimo:";
		cin>>pago_minimo_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
		
		
		
		
		//----------------------------------------------------------	
		if (redondeo_config<0 || redondeo_config>60)
		{cout<<" \n";
		cout<<"ERROR: El redondeo debe estar entre 0 y 60 \n";
		cout<<"Valor que le asigno: "<<redondeo_config;
		cout<<"\nRedondeo al combro a los siguientes minutos:";
		cin>>redondeo_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
		
		
		
		//----------------------------------------------------------	
		if (min_max_config<0)
		{cout<<" \n";
		cout<<"ERROR: Los minutos maximos deben ser >= 0\n";
		cout<<"Valor que le asigno: "<<min_max_config;
		cout<<"\nMinutos maximos para salir despues del pago:";
		cin>>min_max_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
		
		
		//----------------------------------------------------------	
		if ( modena_1_config<0 )
		{cout<<" \n";
		cout<<"ERROR: La moneda 1 debe ser >=0\n";
		cout<<"Valor que le asigno: "<<modena_1_config;
		cout<<"\nMoneda 1:";
		cin>>modena_1_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
		
		
		
		
		
		//----------------------------------------------------------	
		if ( modena_2_config<=modena_1_config)
		{cout<<" \n";
		cout<<"ERROR: La moneda 2 debe ser mayor a la moneda 1\n";
		cout<<"Valor de la moneda 1: "<<modena_1_config;
		cout<<"\nValor que le asigno a la moneda 2: "<<modena_2_config;
		cout<<"\nMoneda 2:";
		cin>>modena_2_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
		
		
		
		
		//----------------------------------------------------------	
		if ( modena_3_config<=modena_2_config)
		{cout<<" \n";
		cout<<"ERROR: La moneda 3 debe ser mayor a la moneda 2\n";
		cout<<"Valor de la moneda 2: "<<modena_2_config;
		cout<<"\nValor que le asigno a la moneda 3: "<<modena_3_config;
		cout<<"\nMoneda 3:";
		cin>>modena_3_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
			
		
		
		
		//----------------------------------------------------------	
		if (billete_1_config<0)
		{cout<<" \n";
		cout<<"ERROR: El billete 1 debe ser  >= 0\n";
		cout<<"Billete 1:";
		cin>>billete_1_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
			
		
			
		
		
		
		//----------------------------------------------------------	
		if (billete_2_config<=billete_1_config)
		{cout<<" \n";
		cout<<"ERROR: El billete 2 debe ser mayor al billete 1 \n";
		cout<<"Valor del Billete 1: "<<billete_1_config;
		cout<<"\nValor que le asigno al billete 2: "<<billete_2_config;
		cout<<"\n Billete 2:";
		cin>>billete_2_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
			
		
		
		
		//----------------------------------------------------------	
		if (billete_3_config<=billete_2_config)
		{cout<<" \n";
		cout<<"ERROR: El billete 3 debe ser mayor al billete 3 \n";
		cout<<"Valor del Billete 2: "<<billete_2_config;
		cout<<"\nValor que le asigno al billete 3: "<<billete_3_config;
		cout<<"\n Billete 3:";
		cin>>billete_3_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
			
			
		
		
		
		//----------------------------------------------------------	
		if (billete_4_config<=billete_3_config)
		{cout<<" \n";
		cout<<"ERROR: El billete 4 debe ser mayor al billete 3 \n";
		cout<<"Valor del Billete 3: "<<billete_3_config;
		cout<<"\nValor que le asigno al billete 4: "<<billete_4_config;
		cout<<"\nBillete 4:";
		cin>>billete_4_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
			
		
		
		
		//----------------------------------------------------------	
		if (billete_5_config<=billete_4_config)
		{cout<<" \n";
		cout<<"ERROR: El billete 5 debe ser mayor al billete 4 \n";
		cout<<"Valor del Billete 4: "<<billete_4_config;
		cout<<"\nValor que le asigno al billete 5: "<<billete_5_config;
		cout<<"\nBillete 5:";
		cin>>billete_5_config;
		fallo=true;
		system("pause");
		continue;	
		}
		else
			fallo=false;
				
	}
	bool salida;
	salida=true;
	int opcion;
	
	while ( salida==true){
		system("cls");
		cout<<"Desea confirmar o cancelar la informacion\n1---> Acertar\n2---> Cancelar\nOpcion: ";
		cin>>opcion;
		switch(opcion){
			
			case 1:
				cout<<"Confirmo informacion\n";
				salida=false;
				system("pause");
				
			break;
					
			case 2:
				cout<<"Cancelo la informacion\n";
				salida=false;
				system("pause");
			break;
			
			default:
				cout<<"ERROR: Seleccione una de las 2 opciones\n";
				system("pause");
		}
		
	}
	cout<<"\n       Menu principal\n";
	system("pause");



}
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
