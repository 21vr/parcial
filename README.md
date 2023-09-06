Imports System

Module Program
    Sub Main()
        Console.WriteLine("Programa de Gentilicios y Especies")
        Console.WriteLine("------------------------------")

        Dim paises() As String = {"El Salvador", "México", "Argentina", "España", "Francia", "Italia", "Alemania", "Brasil"}
        Dim gentilicios() As String = {"salvadoreño", "mexicano", "argentino", "español", "francés", "italiano", "alemán", "brasileño"}
        Dim animales() As String = {"Lobo", "Tigre", "Águila", "Ballena", "Canguro", "León", "Delfín", "Cocodrilo"}
        Dim especies() As String = {"Canina", "Panthera tigris", "Aquila chrysaetos", "Balaenoptera", "Macropodidae", "Panthera leo", "Delphinidae", "Crocodylus"}

        Console.WriteLine("Elija una opción:")
        Console.WriteLine("1. Gentilicios")
        Console.WriteLine("2. Especies de Animales")
        Dim opcion As Integer = Console.ReadLine()

        If opcion = 1 Then
            Console.WriteLine("Ingrese un país:")
            Dim paisBuscado As String = Console.ReadLine()
            Dim encontrado As Boolean = False
            For i As Integer = 0 To paises.Length - 1
                If String.Compare(paisBuscado, paises(i), StringComparison.OrdinalIgnoreCase) = 0 Then
                    Console.WriteLine("El gentilicio de " & paisBuscado & " es " & gentilicios(i))
                    encontrado = True
                    Exit For
                End If
            Next
            If Not encontrado Then
                Console.WriteLine("No se encontró el país ingresado.")
            End If
        ElseIf opcion = 2 Then
            Console.WriteLine("Ingrese una especie de animal:")
            Dim especieBuscada As String = Console.ReadLine()
            Dim encontrado As Boolean = False
            For i As Integer = 0 To especies.Length - 1
                If String.Compare(especieBuscada, especies(i), StringComparison.OrdinalIgnoreCase) = 0 Then
                    Console.WriteLine("El animal de especie " & especieBuscada & " es " & animales(i))
                    encontrado = True
                    Exit For
                End If
            Next
            If Not encontrado Then
                Console.WriteLine("No se encontró la especie de animal ingresada.")
            End If
        Else
            Console.WriteLine("Opción no válida.")
        End If

        Console.WriteLine("Ejecución del programa ha terminado.")

        ' Mostrar los nombres de los estudiantes
        Console.WriteLine("Nombres de los estudiantes:")
        Console.WriteLine("1. Javier Alexander Naranjo Moz")
        Console.WriteLine("2. Francisco Andrés García Mena")
    End Sub
End Module

