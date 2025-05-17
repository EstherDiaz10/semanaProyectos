<img src="./Logo.png" alt="Imagen" width="100"/>

# Soluciones de Desarrollo Dinamicas
## Gestión de franquicia de gimnasios

## Índice

1. [Integrantes proyecto](#integrantes-del-proyecto)
2. [Tecnologías utilizadas](#tecnologías-utilizadas)
3. [Subsistemas](#subsistemas)
4. [Funcionalidades implementadas](#funcionalidades-implementadas-por-subsistema)
5. [Demostración código java](#demostración-código-java)

## Integrantes del proyecto

- Esther Díaz [perfil](https://github.com/EstherDiaz10)
- Silvia Perea [perfil](https://github.com/Silchartur)
- David Llorens [perfil](https://github.com/Dalloher)
- Daniela Matei [perfil](https://github.com/daniela-matei)

## Tecnologías utilizadas

-  **Java** :coffee:
-  **MySQL** :globe_with_meridians:
-  **Bootstrap** :desktop_computer:	
-  **Git** :two_men_holding_hands:

## Subsistemas

- Subsistema 1. Gestión de clientes y suscriptores. Autora: [Silvia](https://github.com/Silchartur)
- Subsistema 2. Gestión de entrenadores y empleado. Autor: [David](https://github.com/Dalloher)
- Subsistema 3. Programación y control de clases. Autora: [Esther](https://github.com/EstherDiaz10)
- Subsistema 4. Gestión de equipos e instalaciones. Autora: [Daniela](https://github.com/daniela-matei)

## Funcionalidades implementadas por subsistema

<table style="border-collapse: collapse; width: 100%; font-size: 1em;">
  <thead>
    <tr style="border: 1px solid black;">
      <th style="border: 1px solid black; padding: 5px;">Subsistema</th>
      <th style="border: 1px solid black; padding: 5px;">Funcionalidad principal</th>
      <th style="border: 1px solid black; padding: 5px;">Autor</th>
      <th style="border: 1px solid black; padding: 5px;">Estado</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border: 1px solid black;">
      <td style="border: 1px solid black; padding: 5px;">Gestión de clientes y suscriptores</td>
      <td style="border: 1px solid black; padding: 5px;">Visualizar y gestionar suscripciones</td>
      <td style="border: 1px solid black; padding: 5px;">Silvia Perea</td>
      <td style="border: 1px solid black; padding: 5px;">Completado</td>
    </tr>
    <tr style="border: 1px solid black;">
      <td style="border: 1px solid black; padding: 5px;">Gestión de empleados</td>
      <td style="border: 1px solid black; padding: 5px;">Buscar, registrar y editar entrenadores</td>
      <td style="border: 1px solid black; padding: 5px;">David Llorens</td>
      <td style="border: 1px solid black; padding: 5px;">Completado</td>
    </tr>
    <tr style="border: 1px solid black;">
      <td style="border: 1px solid black; padding: 5px;">Control de clases</td>
      <td style="border: 1px solid black; padding: 5px;">Visualizar, gestionar y editar clases</td>
      <td style="border: 1px solid black; padding: 5px;">Esther Díaz</td>
      <td style="border: 1px solid black; padding: 5px;">Completado</td>
    </tr>
    <tr style="border: 1px solid black;">
      <td style="border: 1px solid black; padding: 5px;">Gestión de instalaciones</td>
      <td style="border: 1px solid black; padding: 5px;">Gestionar y controlar instalaciones</td>
      <td style="border: 1px solid black; padding: 5px;">Daniela Matei</td>
      <td style="border: 1px solid black; padding: 5px;">Completado</td>
    </tr>
  </tbody>
</table>

## Demostración código java
#### Programación y control de clases. Función mostrar clases del cliente

```java
public void mostrarClasesCliente(Cliente cliente) {

      for (Clase c: clases) {

          if(c.getClientesInscritos().contains(cliente)) {
              System.out.println(c);
              System.out.println("-----------------------------------");
          }
      }
}
```

#### Gestión de clientes y suscriptores. Función mostrar suscripciones

```java
public void mostrarSuscripciones() {
      boolean encontrado = false;  
      for (Cliente cliente : clientes) {
            
          if (cliente.getSuscripcion() != null) {
              System.out.println(cliente.getNombre() + " tiene una suscripción de tipo: "
                      + cliente.getSuscripcion().getNombre());  
              encontrado = true; 
          }
      }

      if (!encontrado) {
          System.out.println("No hay suscripciones activas en el sistema.");
      }
}
```

#### Gestión de entrenadores y empleados. Función buscar trabajador

```java
public static int buscarTrabajador(ArrayList<Encargado> aCargoDe, String nombre, int id) {
      int i = 0, pos = -1;
      while (i < aCargoDe.size() && pos == -1) {
          if (aCargoDe.get(i).getNombre().equals(nombre) && aCargoDe.get(i).getId() == id) {
              pos = i;
          } else {
              i++;
          }
      }
      return pos;
}
```

#### Gestión de equipos e instalaciones. Constructor instalación

```java
public Instalacion(double id,String tipo, String estado){
      this.id = id;
      this.tipo = tipo;
      this.estado = estado;
}
```

> [!NOTE]
> Esta aplicación aún se encuentra en desarrollo. Algunas funcionalidades pueden cambiar en el futuro.

#### [Enlace a la web del centro](https://portal.edu.gva.es/iesfontdesantlluis/)
