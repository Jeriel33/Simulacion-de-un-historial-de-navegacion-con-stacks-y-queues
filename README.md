# Simulacion-de-un-historial-de-navegacion-con-stacks-y-queues
 1. Laboratorio Práctico  Título: "Simulación de un Historial de Navegación con Stacks y Queues"
🚀 ¿Qué hace el código?
Este programa muestra dos ejemplos prácticos usando estas estructuras:

Una pila (Stack) para simular un historial de páginas web visitadas.
Una cola (Queue) para simular páginas pendientes de visita.
using System;
using System.Collections.Generic;

class Program
{
	static void Main()
	{
		Stack<string> paginasVisitadas = new Stack<string>(); // esto es una pila
		Queue<string> paginasEnEspera = new Queue<string>();  // esto es una cola

		// agregando páginas visitadas
		paginasVisitadas.Push("pagina1.com");
		paginasVisitadas.Push("pagina2.com");
		paginasVisitadas.Push("pagina3.com");

		Console.WriteLine("Historial:");
		foreach (var pagina in paginasVisitadas)
			Console.WriteLine(pagina);

		// volviendo atrás
		paginasVisitadas.Pop(); // quitar última página visitada
		Console.WriteLine("\nDespués de ir atrás, estás en: " + paginasVisitadas.Peek());

		// agregando páginas en espera
		paginasEnEspera.Enqueue("pagina4.com");
		paginasEnEspera.Enqueue("pagina5.com");

		Console.WriteLine("\nPáginas en espera:");
		foreach (var pagina in paginasEnEspera)
			Console.WriteLine(pagina);

		// visitando página en espera
		string siguientePagina = paginasEnEspera.Dequeue(); // sacar primera página de la cola
		Console.WriteLine("\nVisitando página pendiente: " + siguientePagina);
	}
}
