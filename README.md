# Composicion#C
Se muestra la relación de composición dentro de UML
using System

public class Computadora
{
    //composición
    private Procesador procesador;
    //constructor
    public Computadora()
    {
   procesador = new Procesador();
   procesador.Marca="AMD";
    }
    public void Encender()
    {
        Console.WriteLine("La computadora esta encendida");
        procesador.MostrarMarca();
    }
}
public class Procesador
{
    public string Marca {get;set;}
    public void MostrarMarca()=>Console.WriteLine($"Procesador Marca {Marca}");
}
public class Program
{
    static void Main()
    {
       Computadora pc = new Computadora();
       pc.Encender();
    }
}
