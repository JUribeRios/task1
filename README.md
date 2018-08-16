#include <iostream>
#include <math.h>

using namespace std;

#define alpha 1.24
#define pi 3.1416
unsigned int var;

void calcParabolico(void);
void print_results(void);
void otros_calculos(void);


int main()
{
    unsigned short int des = 5;
    
    var = 100;

    var += des;

    //Calculando los parametros en la Tierra con g = 9.8 m/s*s
    calcParabolico();
    print_results();

    //Calculando los parametros en la Luna con g = 1.62 m/s*s
    calcParabolico();
    print_results();


    return 0;
}

void calcParabolico(void)
{
    const float g = 9.8;
    char vx0, vy0, x, y, vx, vy,v0,t,y0;
    

    vx0 = v0 * cos(alpha);
    vy0 = v0 * sin(alpha);

    vx = vx0;
    vy = vy0-g*t;

    x = vx*t;
    y = y0+vy0*t-(g*pow(t,2)/2);
}

void print_results(void)
{char vy,x,vx,y;
    std::cout<<"Los resultados del calculo parabolico son: "<<std::endl;
    std::cout<<"Velocidad en x: "<<vx<<", ";
    std::cout<<"Velocidad en y: "<<vy<<", ";
    std::cout<<"Posicion en x: "<<x<<", ";
    std::cout<<"Posicion en y: "<<y<<std::endl;
}

void otros_calculos(void)
{
    int R,wL,G,wC;
    float w,frecuenciaangular;
    int x,a,b,c,B,betacero,Z0;
    float f;
    double mu = 0.00000125664;
    double epsi = 0.00000000000088542;

    // Serie simple (1/[(x^2) + (x+1)]) para x entre 1 y 199
   for( x=1; x<200; x++)
       // Agregue aqui la formula

     //Volumen de la esfera 
     // Agregue aqui la formula

    //Raices de la ecuacion (3*x^2) + (5*x) + 8  = 0 
      //Agregue aqui la formula

   // Impedancia tipica de una linea de transmision
      Z0 = ((R+wL)/(G+wC))^(1/2);
      f=10000;
      w = frecuenciaangular = 2*pi*f; 
        //Agregue aqui la formula

     //Constante de fase de una fibra optica
      B = ((((a^2)-(b^2))*c+(b^2))^(1/2))*betacero;
      betacero = w*(mu*epsi)^(1/2);
      f=5000000;
      w = frecuenciaangular = 2*pi*f;
      

}
