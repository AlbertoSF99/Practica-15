# Práctica 15 - Creación de una alerta para Azure Monitor

## Innovaccion Virtual (VII Edición) #IAWizards

### Semana 3 - Sesión 7

En esta práctica se creó una máquina virtual a la cual se le agregó una regla por medio de Azure Monitor para que informara cuando la CPU pasara de cierto porcentaje de uso.

--------------------------------------------------------

#### Requerimientos 
- Cuenta de Azure con suscripción.
- Tener instalado [Microsoft Remote Desktop](https://apps.microsoft.com/store/detail/escritorio-remoto-de-microsoft/9WZDNCRFJ3PS?hl=es-mx&gl=MX)

---------------------------------------------------------

#### Pasos a seguir

1. En portal.azure.com creamos una máquina virtual.

2. Una vez habiéndose creado la máquina virtual, accedemos a esta, le damos en ‘Conectar’ y descargamos el archivo RDP.

![P15I1](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2001.PNG)

![P15I2](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2002.PNG)

3. Ejecutamos el programa con Remote Desktop y proporcionamos los datos de la cuenta con la que creamos el recurso.

![P15I3](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2003.PNG)

4. En el portal de Azure, buscamos ‘Monitor’ y nos vamos al apartado de ‘Métricas’ y seleccionamos el grupo de recursos de interés, así como el recurso que se quiera monitorear, y le damos en ‘Aplicar’.

![P15I4](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2004.PNG)

5. Seguidamente, en el apartado de ‘Métrica’ se puede seleccionar la métrica que se desea trackear, por ejemplo, Porcentage CPU. También puede guardarse esta métrica en el panel al darle en la opción ‘Guardar en el panel’ y en ‘Anclar al panel’, de esta manera, se puede ver esta métrica en el entorno de Azure.

![P15I5](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2005.PNG)

![P15I6](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2006.PNG)

6. Ahora nos trasladamos al apartado de ‘Alertas’ y le damos a ‘Crear’ y en ‘Regla de alertas’. En el apartado de ‘Filtrar por tipo de recurso’ elegimos el recurso que se planea monitorear (en este caso, virtual machine) y escogemos la VM previamente creada. Seleccionamos la suscripción a usar y damos en ‘Listo’. Vamos ahora al apartado de ‘Reglas de alertas’ y en la alerta de uso de CPU le damos en ‘Seleccionar grupos de acciones’ y escogemos la acción correspondiente.

![P15I7](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2007.PNG)

![P15I8](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2008.PNG)

![P15I9](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2009.PNG)

7. En el apartado de ‘Condición’, en el buscador de ‘Buscar por nombre de señal’ podemos encontrar el tipo de trackeo a usar (Porcentage CPU). Al darle click a este trackeo, podremos establecer el ‘Valor del umbral’, es decir, el valor al cual el uso de CPU hará saltar la alerta (como ejemplo se usará un valor de 40) y en la ‘Granualidad de agregación (periodo)’ se tendrá el tiempo con el cual se estará monitoreando. Al finalizar se le da en ‘Listo’ y en ‘Crear’. Si salta error por falta de datos, llenamos los datos solicitados para proceder a crearlo.

![P15I10](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2010.PNG)

8. Regresamos al apartado de ‘Métricas’, elegimos el grupo de recursos y el recurso (VM) que se va a monitorear. Buscamos la métrica ‘Porcentage CPU’ y esperamos un rato a que cargue los datos. Una vez las condiciones se cumplan, la alerta saltará y llegará en forma de correo.

![P15I11](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2011.PNG)

![P15I12](https://github.com/AlbertoSF99/Practica-15/blob/main/Images/Sesi%C3%B3n%207%20-%20P15%2012.PNG)
