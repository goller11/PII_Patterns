# Ejercicios de DIP, ISP, SRP
## Ejercicio 1 

**DIP:** No se cumple tal principio dado que no hay ninguna dependencia entre las distintas clases (BaseDeDatos y AnlizadorDatos), por lo tanto, tal como se vió en clase, es necesario crear una interfaz que contenga el método empleado en AnlizadorDatos, el cual es ListarDatos().

**ISP:** 

**SRP:** Se cumple tal principio, esto se debe a que no existe más de una razón de cambio en la clase a analizar.

## Ejercicio 2
//Objeto que representa un dato de la base de datos.
class DataBaseObject {
    public string Descripcion { get; }
}

//Base de datos.
class BaseDeDatos : IDataBase {
    public DataBaseObject ObtenerDato (string clave) {
        //Devuelve el dato correspondiente a la clave
    }
    public void GrabarDato (string clave, DataBaseObject dato) {
        //Graba el dato en la base de datos, bajo la clave dada
    }
    public String[] ListarClaves () {
        //Devuelve un String[] con todas las claves
    }
    public String[] ListarDescripcionDatos () {
        //Devuelve un String[] con la descripción de todas los 
        //datos almacenados en  la base
    }

}
class AnlizadorDatos {
    private BaseDeDatos baseDatos { get; set; }
    public void Analizar () {
        foreach (IDataBase DBObj in baseDatos.ListarDatos ()) {
            if (CumpleCondicion (DBObj)) {
                MensajeUno ();
            } else {
                MensajeDos ();
            }
        }
    }
    public bool Cumplecondicion (DataBaseObject DBobj) {
        //Devuelve true si se cumple una cierta condición
    }
    public void MensajeUno () { /*Mensaje predeterminado*/ }
    public void MensajeDos () { /*Mensaje predeterminado*/ }
}

interface IDataBase {

    public DataBaseObject[] ListarDatos ();
}
## Ejercicio 3 

```cs
////Insertar el código corregido. El ejercicio 2 y 3 pueden ser resueltos de forma conjunta

```