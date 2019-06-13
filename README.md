# Proyecto_Taller_Parqueo
//Programa 4: Parqueo C++
#include<iostream>
#include<vector>
using namespace std;
//.................Variables GLOBLAES PARA EL SALDO.....................

// ........SE LE ASIGNA EL VALOR INICIAL DE 0........

int saldo_total_moneda_1 = 0;
int saldo_total_moneda_2 = 0;
int saldo_total_moneda_3 = 0;
int saldo_total_moneda_total = 0;
int saldo_total_billete_1 = 0;
int saldo_total_billete_2 = 0;
int saldo_total_billete_3 = 0;
int saldo_total_billete_4 = 0;
int saldo_total_billete_5 = 0;
int saldo_total_billete_total = 0;

int saldo_cantidad_moneda_1 = 0;
int saldo_cantidad_moneda_2 = 0;
int saldo_cantidad_moneda_3 = 0;
int saldo_cantidad_moneda_total = 0;
int saldo_cantidad_billete_1 = 0;
int saldo_cantidad_billete_2 = 0;
int saldo_cantidad_billete_3 = 0;
int saldo_cantidad_billete_4 = 0;
int saldo_cantidad_billete_5 = 0;
int saldo_cantidad_billete_total = 0;


	
//Falta documentacion de la funcion de configurar
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
				precioxhora=precioxhora_config;
				pago_minimo=pago_minimo_config;
				redondeo=redondeo_config;
				min_max=min_max_config;
				modena_1=modena_1_config;
				modena_2=modena_2_config;
				modena_3=modena_3_config;
				billete_1=billete_1_config;
				billete_2=billete_2_config;
				billete_3=billete_3_config;
				billete_4=billete_4_config;
				billete_5=billete_5_config;
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
	// Variables Para cargar cajero 
	
	//-------------------------Varibales de saldo locales-------------------------//
	int saldo_total_moneda_1_cargar;
	int saldo_total_moneda_2_cargar;
	int saldo_total_moneda_3_cargar;
	int saldo_total_moneda_total_cargar;
	int saldo_total_billete_1_cargar;
	int saldo_total_billete_2_cargar;
	int saldo_total_billete_3_cargar;
	int saldo_total_billete_4_cargar;
	int saldo_total_billete_5_cargar;
	int saldo_total_billete_total_cargar;
	
	int saldo_cantidad_moneda_1_cargar;
	int saldo_cantidad_moneda_2_cargar;
	int saldo_cantidad_moneda_3_cargar;
	int saldo_cantidad_moneda_total_cargar;
	int saldo_cantidad_billete_1_cargar;
	int saldo_cantidad_billete_2_cargar;
	int saldo_cantidad_billete_3_cargar;
	int saldo_cantidad_billete_4_cargar;
	int saldo_cantidad_billete_5_cargar;
	int saldo_cantidad_billete_total_cargar;
	
	//......SE ASIGNA EL VALOR DE LA GLOBAL DE SALDO......//
	
	saldo_total_moneda_1_cargar = saldo_total_moneda_1;
	saldo_total_moneda_2_cargar = saldo_total_moneda_2;
	saldo_total_moneda_3_cargar = saldo_total_moneda_3;
	saldo_total_moneda_total_cargar = saldo_total_moneda_total;
	saldo_total_billete_1_cargar = saldo_total_billete_1;
	saldo_total_billete_2_cargar = saldo_total_billete_2;
	saldo_total_billete_3_cargar = saldo_total_billete_3;
	saldo_total_billete_4_cargar = saldo_total_billete_4;
	saldo_total_billete_5_cargar = saldo_total_billete_5;
	saldo_total_billete_total_cargar = saldo_total_billete_total ;
	
	saldo_cantidad_moneda_1_cargar = saldo_cantidad_moneda_1;
	saldo_cantidad_moneda_2_cargar = saldo_cantidad_moneda_2;
	saldo_cantidad_moneda_3_cargar = saldo_cantidad_moneda_3;
	saldo_cantidad_moneda_total_cargar = saldo_cantidad_moneda_total;
	saldo_cantidad_billete_1_cargar = saldo_cantidad_billete_1;
	saldo_cantidad_billete_2_cargar = saldo_cantidad_billete_2;
	saldo_cantidad_billete_3_cargar = saldo_cantidad_billete_3;
	saldo_cantidad_billete_4_cargar = saldo_cantidad_billete_4;
	saldo_cantidad_billete_5_cargar = saldo_cantidad_billete_5;
	saldo_cantidad_billete_total_cargar= saldo_cantidad_billete_total;

	
	//-------------------------Varibales de saldo antes locales-------------------------//
	
	int antes_total_moneda_1_cargar;
	int antes_total_moneda_2_cargar;
	int antes_total_moneda_3_cargar;
	int antes_total_moneda_total_cargar;
	int antes_total_billete_1_cargar;
	int antes_total_billete_2_cargar;
	int antes_total_billete_3_cargar;
	int antes_total_billete_4_cargar;
	int antes_total_billete_5_cargar;
	int antes_total_billete_total_cargar;
	
	int antes_cantidad_moneda_1_cargar;
	int antes_cantidad_moneda_2_cargar;
	int antes_cantidad_moneda_3_cargar;
	int antes_cantidad_moneda_total_cargar;
	int antes_cantidad_billete_1_cargar;
	int antes_cantidad_billete_2_cargar;
	int antes_cantidad_billete_3_cargar;
	int antes_cantidad_billete_4_cargar;
	int antes_cantidad_billete_5_cargar;
	int antes_cantidad_billete_total_cargar;
	
	//......SE ASIGNA EL VALOR DE LA GLOBAL DE SALDO......//
	
	
	antes_total_moneda_1_cargar = saldo_total_moneda_1;
	antes_total_moneda_2_cargar = saldo_total_moneda_2;
	antes_total_moneda_3_cargar = saldo_total_moneda_3;
	antes_total_moneda_total_cargar = saldo_total_moneda_total;
	antes_total_billete_1_cargar = saldo_total_billete_1;
	antes_total_billete_2_cargar = saldo_total_billete_2;
	antes_total_billete_3_cargar = saldo_total_billete_3;
	antes_total_billete_4_cargar = saldo_total_billete_4;
	antes_total_billete_5_cargar = saldo_total_billete_5;
	antes_total_billete_total_cargar = saldo_total_billete_total ;
	
	antes_cantidad_moneda_1_cargar = saldo_cantidad_moneda_1;
	antes_cantidad_moneda_2_cargar = saldo_cantidad_moneda_2;
	antes_cantidad_moneda_3_cargar = saldo_cantidad_moneda_3;
	antes_cantidad_moneda_total_cargar = saldo_cantidad_moneda_total;
	antes_cantidad_billete_1_cargar = saldo_cantidad_billete_1;
	antes_cantidad_billete_2_cargar = saldo_cantidad_billete_2;
	antes_cantidad_billete_3_cargar = saldo_cantidad_billete_3;
	antes_cantidad_billete_4_cargar = saldo_cantidad_billete_4;
	antes_cantidad_billete_5_cargar = saldo_cantidad_billete_5;
	antes_cantidad_billete_total_cargar= saldo_cantidad_billete_total;

	
	
	//-------------------------Varibales de carga locales-------------------------//
	
	int carga_total_moneda_1_cargar=0;
	int carga_total_moneda_2_cargar=0;
	int carga_total_moneda_3_cargar=0;
	int carga_total_moneda_total_cargar=0;
	int carga_total_billete_1_cargar=0;
	int carga_total_billete_2_cargar=0;
	int carga_total_billete_3_cargar=0;
	int carga_total_billete_4_cargar=0;
	int carga_total_billete_5_cargar=0;
	int carga_total_billete_total_cargar=0;
	
	int carga_cantidad_moneda_1_cargar=0;
	int carga_cantidad_moneda_2_cargar=0;
	int carga_cantidad_moneda_3_cargar=0;
	int carga_cantidad_moneda_total_cargar=0;
	int carga_cantidad_billete_1_cargar=0;
	int carga_cantidad_billete_2_cargar=0;
	int carga_cantidad_billete_3_cargar=0;
	int carga_cantidad_billete_4_cargar=0;
	int carga_cantidad_billete_5_cargar=0;
	int carga_cantidad_billete_total_cargar=0;



	//-------------------------------------//
	
	
		
	int accion;
	
	// un while para que cargue el menú las veces que el quiera cargar el cajero, es decir, hasta que confirme.
	bool accion_carga;
	accion_carga=true;
	while(accion_carga==true)
	{	
		//Elimina todas las cosas que se imprimieron 
		system("cls");
		
		
		// Muestra la cantidad de saldo antes de la carga. 
		cout<<"__________________SALDO ANTE DE HACER LA CARGA__________________\n";
		cout<<"                    CANTIDAD     TOTAL";	
		cout<<"\n";	
		cout<<"\n Moneda de: "<< moneda_1<<"          "<<antes_cantidad_moneda_1_cargar<<"         "<<antes_total_moneda_1_cargar;
		cout<<"\n Moneda de: "<< moneda_2<<"          " <<antes_cantidad_moneda_2_cargar<<"         "<<antes_total_moneda_2_cargar;
		cout<<"\n Moneda de: "<< moneda_3<<"          "<<antes_cantidad_moneda_3_cargar<<"         "<<antes_total_moneda_3_cargar;
		cout<<"\n Total de monedas:        "<<antes_cantidad_moneda_total_cargar<<"         "<<antes_total_moneda_total_cargar;
		cout<<"\n Billete de: "<< billete_1<<"         "<<antes_cantidad_billete_1_cargar<<"         "<<antes_total_billete_1_cargar;
		cout<<"\n Billete de: "<< billete_2<<"         "<<antes_cantidad_billete_2_cargar<<"         "<<antes_total_billete_2_cargar;
		cout<<"\n Billete de: "<< billete_3<<"         "<<antes_cantidad_billete_3_cargar<<"         "<<antes_total_billete_3_cargar;
		cout<<"\n Billete de: "<< billete_4<<"         "<<antes_cantidad_billete_4_cargar<<"         "<<antes_total_billete_4_cargar;
		cout<<"\n Billete de: "<< billete_5<<"         "<<antes_cantidad_billete_5_cargar<<"         "<<antes_total_billete_5_cargar;
		cout<<"\n Total de billetes:       "<<antes_cantidad_billete_total_cargar<<"         "<<antes_total_billete_total_cargar;
		cout<<"\n";
		cout<<"\n TOTAL DEL DINERO  ------------->   "<<(antes_total_billete_total_cargar+antes_total_moneda_total_cargar);
		cout<<"\n";
		cout<<"\n";
		system("pause");
		
		cout<<"\n";
		cout<<"__________________SALDO SI ES REALIZA LA CARGA__________________\n";
		cout<<"                    CANTIDAD     TOTAL";	
		cout<<"\n";	
		cout<<"\n Moneda de: "<< moneda_1<<"          "<<saldo_cantidad_moneda_1_cargar<<"         "<<saldo_total_moneda_1_cargar;
		cout<<"\n Moneda de: "<< moneda_2<<"          " <<saldo_cantidad_moneda_2_cargar<<"         "<<saldo_total_moneda_2_cargar;
		cout<<"\n Moneda de: "<< moneda_3<<"          "<<saldo_cantidad_moneda_3_cargar<<"         "<<saldo_total_moneda_3_cargar;
		cout<<"\n Total de monedas:        "<<saldo_cantidad_moneda_total_cargar<<"         "<<saldo_total_moneda_total_cargar;
		cout<<"\n Billete de: "<< billete_1<<"         "<<saldo_cantidad_billete_1_cargar<<"         "<<saldo_total_billete_1_cargar;
		cout<<"\n Billete de: "<< billete_2<<"         "<<saldo_cantidad_billete_2_cargar<<"         "<<saldo_total_billete_2_cargar;
		cout<<"\n Billete de: "<< billete_3<<"         "<<saldo_cantidad_billete_3_cargar<<"         "<<saldo_total_billete_3_cargar;
		cout<<"\n Billete de: "<< billete_4<<"         "<<saldo_cantidad_billete_4_cargar<<"         "<<saldo_total_billete_4_cargar;
		cout<<"\n Billete de: "<< billete_5<<"         "<<saldo_cantidad_billete_5_cargar<<"         "<<saldo_total_billete_5_cargar;
		cout<<"\n Total de billetes:       "<<saldo_cantidad_billete_total_cargar<<"         "<<saldo_total_billete_total_cargar;
		cout<<"\n";
		cout<<"\n TOTAL DEL DINERO  ------------->  "<<(saldo_total_billete_total_cargar+saldo_total_moneda_total_cargar);
		cout<<"\n";
		cout<<"\n";
		system("pause");
		
		 
		cout<<"\n";	
		cout<<"\n";		
		cout<<"       Carga\n 1--> Moneda de: "<< moneda_1<< "\n 2--> Moneda de: "<< moneda_2<< "\n 3--> Moneda de: "<< moneda_3<< "\n 4--> Billete de: "<< billete_1<< "\n 5--> Billete de: "<< billete_2<< "\n 6--> Billete de: "<< billete_3<< "\n 7--> Billete de: "<< billete_4<< "\n 8--> Billete de: "<< billete_5<< "\n 9--> Confirmar. \n 10--> Cancelar.";                                  
		cout<<"\n";			
		cout<<"\n Ingrese la accion que desea realizar: ";
		cin>>accion;
		
		/* en cada caso va a llevar un cout del total y cantidad de esa moneda ( de la carga ), 
		los valores de que va a agregar, 
		las opciones de confimar esa carga y 
		luego un cout del monto total de variable si confimar el monto
		*/
		
		int cantidad_de_carga;
		cantidad_de_carga=0;			
		switch(accion)
		{
			bool bucle_accion_carga_monto;
			int accion_carga_monto;
			case 1:
				system("cls");
				cout<<"Moneda de: "<< moneda_1<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_moneda_1_cargar<<"   Total: "<<carga_total_moneda_1_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*moneda_1);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_moneda_1_cargar=carga_cantidad_moneda_1_cargar+cantidad_de_carga;
							carga_total_moneda_1_cargar=(carga_cantidad_moneda_1_cargar*moneda_1);
							
							saldo_cantidad_moneda_1_cargar = (carga_cantidad_moneda_1_cargar);
							saldo_total_moneda_1_cargar = ((saldo_cantidad_moneda_1_cargar*moneda_1));
							
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}	
				
			break;
					
			case 2:
				system("cls");
				cout<<"Moneda de: "<< moneda_2<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_moneda_2_cargar<<"   Total: "<<carga_total_moneda_2_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*moneda_2);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_moneda_2_cargar=carga_cantidad_moneda_2_cargar+cantidad_de_carga;
							carga_total_moneda_2_cargar=(carga_cantidad_moneda_2_cargar*moneda_2);
							
							
							saldo_cantidad_moneda_2_cargar = (carga_cantidad_moneda_2_cargar);
							saldo_total_moneda_2_cargar = ((saldo_cantidad_moneda_2_cargar*moneda_2));
	
					
							
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}	
			break;
					
			case 3:
				system("cls");
				cout<<"Moneda de: "<< moneda_3<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_moneda_3_cargar<<"   Total: "<<carga_total_moneda_3_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*moneda_3);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_moneda_3_cargar=carga_cantidad_moneda_3_cargar+cantidad_de_carga;
							carga_total_moneda_3_cargar=(carga_cantidad_moneda_3_cargar*moneda_3);
							
							saldo_cantidad_moneda_3_cargar = (carga_cantidad_moneda_3_cargar);
							saldo_total_moneda_3_cargar = ((saldo_cantidad_moneda_3_cargar*moneda_3));
						
							
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}	
			break;
					
			case 4:
				system("cls");
				cout<<"Billete de: "<< billete_1<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_billete_1_cargar<<"   Total: "<<carga_total_billete_1_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*billete_1);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_billete_1_cargar=carga_cantidad_billete_1_cargar+cantidad_de_carga;
							carga_total_billete_1_cargar=(carga_cantidad_billete_1_cargar*billete_1);
							
							saldo_cantidad_billete_1_cargar =(carga_cantidad_billete_1_cargar) ;
							saldo_total_billete_1_cargar =((saldo_cantidad_billete_1_cargar*billete_1));
									
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}

			break;
					
			case 5:
				system("cls");
				cout<<"Billete de: "<< billete_2<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_billete_2_cargar<<"   Total: "<<carga_total_billete_2_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*billete_2);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_billete_2_cargar=carga_cantidad_billete_2_cargar+cantidad_de_carga;
							carga_total_billete_2_cargar=(carga_cantidad_billete_2_cargar*billete_2);
			
							saldo_cantidad_billete_2_cargar =(carga_cantidad_billete_2_cargar) ;
							saldo_total_billete_2_cargar =((saldo_cantidad_billete_2_cargar*billete_2)) ;
									
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}

			break;
					
			case 6:
				system("cls");
				cout<<"Billete de: "<< billete_3<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_billete_3_cargar<<"   Total: "<<carga_total_billete_3_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*billete_3);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_billete_3_cargar=carga_cantidad_billete_3_cargar+cantidad_de_carga;
							carga_total_billete_3_cargar=(carga_cantidad_billete_3_cargar*billete_3);
							
							saldo_cantidad_billete_3_cargar =(carga_cantidad_billete_3_cargar) ;
							saldo_total_billete_3_cargar =((saldo_cantidad_billete_3_cargar*billete_3)) ;
							
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}
			break;
					
			case 7:
				system("cls");
				cout<<"Billete de: "<< billete_4<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_billete_4_cargar<<"   Total: "<<carga_total_billete_4_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*billete_4);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_billete_4_cargar=carga_cantidad_billete_4_cargar+cantidad_de_carga;
							carga_total_billete_4_cargar=(carga_cantidad_billete_4_cargar*billete_4);		
							
							saldo_cantidad_billete_4_cargar =(carga_cantidad_billete_4_cargar) ;
							saldo_total_billete_4_cargar =((saldo_cantidad_billete_4_cargar*billete_4)) ;
							
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}

			break;
					
			case 8:
				system("cls");
				cout<<"Billete de: "<< billete_5<<".\n";
				cout<<"Valores en carga:"<<"        "<<"Cantidad: "<<carga_cantidad_billete_5_cargar<<"   Total: "<<carga_total_billete_5_cargar;
				cout<<"\n";
				system("pause");
				cout<<"\nCantidad que desea cargar: ";
				cin>>cantidad_de_carga;
				cout<<"\nTotal de la carga : "<<(cantidad_de_carga*billete_5);
				bucle_accion_carga_monto=true;
				while (bucle_accion_carga_monto==true)
				{
					cout<<"\nDesea confirmar la carga:\n 1---> SI.\n 2---> NO.";
					cout<<"\n";
					cout<<"\nAccion a realizar: ";
					cin>>accion_carga_monto;
					switch(accion_carga_monto)
					{
						case 1:
							cout<<"\nSe realizaron los cambios";
							carga_cantidad_billete_5_cargar=carga_cantidad_billete_5_cargar+cantidad_de_carga;
							carga_total_billete_5_cargar=(carga_cantidad_billete_5_cargar*billete_5);
							
							
							saldo_cantidad_billete_5_cargar =(carga_cantidad_billete_5_cargar) ;
							saldo_total_billete_5_cargar =((saldo_cantidad_billete_5_cargar*billete_5)) ;
	
							
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						case 2:
							cout<<"\nSe cancelaron los cambios";
							bucle_accion_carga_monto=false;
							cout<<"\n";
							system("pause");
						break;
						
						default:
							system("cls");
							cout<<"\nERROR: Selecione alguna de las opciones.";
							cout<<"\n";
							system("pause");
							
						break;
					}
				}
			break;
			
			case 9:
				system("cls");
				cout<<"Confirmar.\n";
				
				saldo_cantidad_moneda_total_cargar =(saldo_cantidad_moneda_1_cargar+saldo_cantidad_moneda_2_cargar+saldo_cantidad_moneda_3_cargar) ;
				saldo_total_moneda_total_cargar =((saldo_cantidad_moneda_1_cargar*moneda_1)+(saldo_cantidad_moneda_2_cargar*moneda_2)+(saldo_cantidad_moneda_3_cargar*moneda_3)) ;
	
				saldo_cantidad_billete_total_cargar =(saldo_cantidad_billete_1_cargar+saldo_cantidad_billete_2_cargar+saldo_cantidad_billete_3_cargar+saldo_cantidad_billete_4_cargar+saldo_cantidad_billete_5_cargar) ;
				saldo_total_billete_total_cargar =((saldo_cantidad_billete_1_cargar*billete_1)+(saldo_cantidad_billete_2_cargar*billete_2)+(saldo_cantidad_billete_3_cargar*billete_3)+(saldo_cantidad_billete_4_cargar*billete_4)+(saldo_cantidad_billete_5_cargar*billete_5)) ;
				
				//-------------------------------------- Se le asigna las variables locales de saldo a las globales.
				saldo_total_moneda_1=saldo_total_moneda_1_cargar;
				saldo_total_moneda_2=saldo_total_moneda_2_cargar;
				saldo_total_moneda_3=saldo_total_moneda_3_cargar;
				saldo_total_moneda_total=saldo_total_moneda_total_cargar;
				saldo_total_billete_1=saldo_total_billete_1_cargar;
				saldo_total_billete_2=saldo_total_billete_2_cargar;
				saldo_total_billete_3=saldo_total_billete_3_cargar;
				saldo_total_billete_4=saldo_total_billete_4_cargar;
				saldo_total_billete_5=saldo_total_billete_5_cargar;
				saldo_total_billete_total=saldo_total_billete_total_cargar;
				
				saldo_cantidad_moneda_1=saldo_cantidad_moneda_1_cargar;
				saldo_cantidad_moneda_2=saldo_cantidad_moneda_2_cargar;
				saldo_cantidad_moneda_3=saldo_cantidad_moneda_3_cargar;
				saldo_cantidad_moneda_total=saldo_cantidad_moneda_total_cargar;
				saldo_cantidad_billete_1=saldo_cantidad_billete_1_cargar;
				saldo_cantidad_billete_2=saldo_cantidad_billete_2_cargar;
				saldo_cantidad_billete_3=saldo_cantidad_billete_3_cargar;
				saldo_cantidad_billete_4=saldo_cantidad_billete_4_cargar;
				saldo_cantidad_billete_5=saldo_cantidad_billete_5_cargar;
				saldo_cantidad_billete_total=saldo_cantidad_billete_total_cargar;
				cout<<"\n Se completo la carga.\n";
				system("pause");
		
				cout<<"\n";
				cout<<"__________________SALDO ACUAL__________________\n";
				cout<<"                    CANTIDAD     TOTAL";	
				cout<<"\n";	
				cout<<"\n Moneda de: "<< moneda_1<<"          "<<saldo_cantidad_moneda_1<<"         "<<saldo_total_moneda_1;
				cout<<"\n Moneda de: "<< moneda_2<<"          " <<saldo_cantidad_moneda_2<<"         "<<saldo_total_moneda_2;
				cout<<"\n Moneda de: "<< moneda_3<<"          "<<saldo_cantidad_moneda_3<<"         "<<saldo_total_moneda_3;
				cout<<"\n Total de monedas:        "<<saldo_cantidad_moneda_total<<"         "<<saldo_total_moneda_total;
				cout<<"\n Billete de: "<< billete_1<<"         "<<saldo_cantidad_billete_1<<"         "<<saldo_total_billete_1;
				cout<<"\n Billete de: "<< billete_2<<"         "<<saldo_cantidad_billete_2<<"         "<<saldo_total_billete_2;
				cout<<"\n Billete de: "<< billete_3<<"         "<<saldo_cantidad_billete_3<<"         "<<saldo_total_billete_3;
				cout<<"\n Billete de: "<< billete_4<<"         "<<saldo_cantidad_billete_4<<"         "<<saldo_total_billete_4;
				cout<<"\n Billete de: "<< billete_5<<"         "<<saldo_cantidad_billete_5<<"         "<<saldo_total_billete_5;
				cout<<"\n Total de billetes:       "<<saldo_cantidad_billete_total<<"         "<<saldo_total_billete_total;
				cout<<"\n";
				cout<<"\n TOTAL DEL DINERO  ------------->  "<<(saldo_total_billete_total+saldo_total_moneda_total);
				cout<<"\n";
				cout<<"\n";
				system("pause");
				accion_carga=false;
			break;
			
			case 10:
				system("cls");
				cout<<"Cancelar.\n";
				
				cout<<"\n Se cancelo la carga.\n";
				system("pause");
		
				cout<<"\n";
				cout<<"__________________SALDO ACUAL__________________\n";
				cout<<"                    CANTIDAD     TOTAL";	
				cout<<"\n";	
				cout<<"\n Moneda de: "<< moneda_1<<"          "<<saldo_cantidad_moneda_1<<"         "<<saldo_total_moneda_1;
				cout<<"\n Moneda de: "<< moneda_2<<"          " <<saldo_cantidad_moneda_2<<"         "<<saldo_total_moneda_2;
				cout<<"\n Moneda de: "<< moneda_3<<"          "<<saldo_cantidad_moneda_3<<"         "<<saldo_total_moneda_3;
				cout<<"\n Total de monedas:        "<<saldo_cantidad_moneda_total<<"         "<<saldo_total_moneda_total;
				cout<<"\n Billete de: "<< billete_1<<"         "<<saldo_cantidad_billete_1<<"         "<<saldo_total_billete_1;
				cout<<"\n Billete de: "<< billete_2<<"         "<<saldo_cantidad_billete_2<<"         "<<saldo_total_billete_2;
				cout<<"\n Billete de: "<< billete_3<<"         "<<saldo_cantidad_billete_3<<"         "<<saldo_total_billete_3;
				cout<<"\n Billete de: "<< billete_4<<"         "<<saldo_cantidad_billete_4<<"         "<<saldo_total_billete_4;
				cout<<"\n Billete de: "<< billete_5<<"         "<<saldo_cantidad_billete_5<<"         "<<saldo_total_billete_5;
				cout<<"\n Total de billetes:       "<<saldo_cantidad_billete_total<<"         "<<saldo_total_billete_total;
				cout<<"\n";
				cout<<"\n TOTAL DEL DINERO  ------------->  "<<(saldo_total_billete_total+saldo_total_moneda_total);
				cout<<"\n";
				cout<<"\n";
				system("pause");
				accion_carga=false;
			break;
					
			default:
				system("cls");
				cout<<"ERROR: La accion escogida no es valida\n";
				system("pause");
				
			break;
				
		}	
		
		saldo_cantidad_moneda_total_cargar =(saldo_cantidad_moneda_1_cargar+saldo_cantidad_moneda_2_cargar+saldo_cantidad_moneda_3_cargar) ;
		saldo_total_moneda_total_cargar =((saldo_cantidad_moneda_1_cargar*moneda_1)+(saldo_cantidad_moneda_2_cargar*moneda_2)+(saldo_cantidad_moneda_3_cargar*moneda_3)) ;
		
		saldo_cantidad_billete_total_cargar =(saldo_cantidad_billete_1_cargar+saldo_cantidad_billete_2_cargar+saldo_cantidad_billete_3_cargar+saldo_cantidad_billete_4_cargar+saldo_cantidad_billete_5_cargar) ;
		saldo_total_billete_total_cargar =((saldo_cantidad_billete_1_cargar*billete_1)+(saldo_cantidad_billete_2_cargar*billete_2)+(saldo_cantidad_billete_3_cargar*billete_3)+(saldo_cantidad_billete_4_cargar*billete_4)+(saldo_cantidad_billete_5_cargar*billete_5)) ;

	
	}
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
