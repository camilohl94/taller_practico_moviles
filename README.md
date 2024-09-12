# taller_practico_moviles


## Crea una tabla llamada Contactos con los siguientes campos:
CREATE TABLE "Contactos" (
	"id"	INTEGER NOT NULL,
	"nombre"	TEXT NOT NULL,
	"telefono"	TEXT NOT NULL,
	PRIMARY KEY("id" AUTOINCREMENT)
);

## Amplía la tabla Contactos creada en el ejercicio 1 agregando los siguientes campos:

CREATE TABLE "Contactos" (
	"id"	INTEGER NOT NULL,
	"nombre"	TEXT NOT NULL,
	"telefono"	TEXT NOT NULL,
	"email"	TEXT NOT NULL,
	"direccion"	TEXT NOT NULL,
	"fecha_nacimiento"	TEXT NOT NULL,
	PRIMARY KEY("id" AUTOINCREMENT)
);

## inserta al menos 5 registros en la tabla Contactos con diferentes datos. Asegúrate de incluir los siguientes campos:
INSERT INTO "Contactos" ("nombre","telefono","email","direccion","fecha_nacimiento")
VALUES ("John Doe","1234567890","john.doe@example.com","123 Main Street","1990-05-15");

INSERT INTO "Contactos" ("nombre","telefono","email","direccion","fecha_nacimiento")
VALUES ("Jane Smith","9876543210","jane.smith@example.com","456 Elm Street","1985-09-20");

INSERT INTO "Contactos" ("nombre","telefono","email","direccion","fecha_nacimiento")
VALUES ("Bob Johnson","5551234567","bob.johnson@example.com","789 Oak Street","1978-12-01");

INSERT INTO "Contactos" ("nombre","telefono","email","direccion","fecha_nacimiento")
VALUES ("Alice Williams","3216549870","alice.williams@example.com","789 Oak Street","1992-07-11");

INSERT INTO "Contactos" ("nombre","telefono","email","direccion","fecha_nacimiento")
VALUES ("Michael Brown","6543217890","michael.brown@example.com","202 Pine Street","1988-03-25");


## Consulta 1: Selecciona todos los contactos que tengan el nombre "John Doe".

SELECT * FROM Contactos WHERE nombre ="John Doe"

## Selecciona todos los contactos cuyo teléfono empiece con "123".

SELECT * from Contactos where telefono like "123%"

## Selecciona todos los contactos ordenados por fecha_nacimiento de más reciente a más antiguo.

SELECT * from Contactos ORDER by fecha_nacimiento DESC

![Texto alternativo](URL-de-la-imagen)

## Creación de una Interfaz Simple en Android
### Crea una interfaz de usuario en un archivo activity_main.xml que incluya un TextView para mostrar un nombre y un Button para cambiar el nombre al hacer clic.
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">


    <TextView
        android:id="@+id/textViewName"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="John Doe"
        android:textSize="24sp"
        android:textColor="@android:color/black"
        android:layout_marginBottom="20dp"/>


    <Button
        android:id="@+id/buttonChangeName"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Cambiar Nombre"/>
</LinearLayout>

## Formulario de Registro Simple con LinearLayout
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">


    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:padding="16dp"
        android:gravity="center"
        android:id="@+id/editText_name"
        android:hint="Ingresa el nombre"
        android:inputType="text"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:padding="16dp"
        android:gravity="center"
        android:id="@+id/ediText_correo"
        android:hint="Ingresa tu correo electrónico"
        android:inputType="textEmailAddress"/>

    <Button
        android:id="@+id/buttonChangeName"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Registrar"/>
</LinearLayout>


