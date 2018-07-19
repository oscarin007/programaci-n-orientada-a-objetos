# programaci-n-orientada-a-objetos-calculadora
//PROGRAM.CS
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace operaciones
{
    class Program
    {
        static void Main(string[] args)
        {
            string n1, n2;
            
            Console.Write(" ");
            n1 = Console.ReadLine();
            Console.Write(" ");
            n2 = Console.ReadLine();

            operaciones objOpera = new operaciones(n1, n2);
            double suma,resta,multiplicacion, division, raiz;
            suma = objOpera.getSuma();
            Console.WriteLine("{0} suma ", suma);
            Console.ReadKey();

            resta = objOpera.getResta();
            Console.WriteLine("{0} resta ", resta);
            Console.ReadKey();

            multiplicacion = objOpera.getMultiplicacion();
            Console.WriteLine("{0} multiplicacion ", multiplicacion);
            Console.ReadKey();

            division = objOpera.getDivision();
            Console.WriteLine("{0} division ", division);
            Console.ReadLine();
            Console.ReadKey();

            raiz = objOpera.getRaiz();
            Console.WriteLine("{0} raiz ", raiz);
            Console.ReadLine();
            Console.ReadKey();
        }   
    }
}

//operaciones.cs

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace operaciones
{
    class operaciones
    {
        public int num1;
        public int num2;
        public operaciones(string nu1, string nu2)
        {
            num1 = int.Parse(nu1);
            num2 = int.Parse(nu2);

        }
        public double getSuma()
        {
            double xsuma;
            xsuma = num1 + num2;
            return xsuma;
            //Console.WriteLine("La suma es:");
        }
        public double getResta()
        {
            double xresta;
            xresta = num1 - num2;
            return xresta;
            //Console.WriteLine("La resta es:");
        }
        public double getMultiplicacion()
        {
            double xmultiplicacion;
            xmultiplicacion = num1 * num2;
            return xmultiplicacion;
            //Console.WriteLine("La multiplicacion es:");
        }
        public double getDivision()
        {
            double xdivision;
            xdivision = num1 / num2;
            return xdivision;
            //Console.WriteLine("La division es:");
        }
        public double getRaiz()
        {
            double xraiz;
            xraiz = num1 ^ (1 / 2);
            return xraiz;
            //Console.WriteLine("La division es:");
        }
    }
}

