# Practica3
## Etiquetar commits y ver diferencias
En primer lugar actualizaremos la rama main con el comando ```git pull origin main```

![image1](https://user-images.githubusercontent.com/114931679/204143537-2fa07fb6-8257-435d-bca5-4d4b93a4c6ed.png)

### Empezaremos por utilizar el comando git tag, mediante el cual daremos un nombre especial (etiqueta) a un commit determinado.
Etiquetaremos el primer y cuarto commit haciendo ```git tag -a nombre_etiqueta -m "Mensaje" commit_a_etiquetar```

![image2](https://user-images.githubusercontent.com/114931679/204144040-d0ee5e0a-ed9f-4383-8998-e1b9a958d5dc.png)

Por lo tanto, esto se refleja de la siguiente manera:

![image3](https://user-images.githubusercontent.com/114931679/204144114-72cffd3f-9803-46ec-9b29-e312ca8ce1de.png)

Al asignarle estas dos etiquetas a estos commits, se nos facilita acceder a ellos ya que no hay que tipear tanto.
Es decir, es más cómodo usar _**git checkout v2.0**_ que _**git checkout b863211**_

A continuación, volvemos al último commit mediante el comando ```git checkout master```

![image4](https://user-images.githubusercontent.com/114931679/204145335-6c7f43b2-999f-4a57-9953-ca2d42acfa63.png)

### Ahora estudiaremos lo que realiza el comando git show.
Si lo ejecutamos cuanto estamos en la rama master, se visualiza de la siguiente manera:

![image5](https://user-images.githubusercontent.com/114931679/204145941-54770aed-e5d7-40b0-a766-c20df2d5b18a.png)

Ahora bien, si cambiamos la posición del HEAD apuntando a la posición donde se encuentran las etiquetas v1.0 y v2.0 definidas previamente, con el comando ```git show v2.0``` se visualiza así:

![image6](https://user-images.githubusercontent.com/114931679/204146183-85e3fc86-1e27-40d2-bdc9-f8e9ac2086b5.png)

#### Se observa que las lineas eliminidas aparecen en rojo, con un signo - delante y las añadidas en verde con un signo + delante.

### Por último trabajaremos con el comando git diff
De este modo se pueden observar los cambios realizados a lo largo de varios commits. Tenemos que escribir: ```git diff v1.0..v2.0```

![image7](https://user-images.githubusercontent.com/114931679/204148092-798799a3-34f2-49be-8997-24c3f8303663.png)
![image8](https://user-images.githubusercontent.com/114931679/204148106-c831319c-5558-4dfc-a455-3c9442270caf.png)

Ahora ejecutaremos la misma instrucción pero con el comando ```git show v1.0..v2.0```

![image9](https://user-images.githubusercontent.com/114931679/204148421-94b2f1fe-b58b-4bd4-8c6d-c25e855c9be1.png)
![image10](https://user-images.githubusercontent.com/114931679/204149227-49c4293e-48e0-4d68-aeaf-5f813090ab13.png)

La conclusión que sacamos es que al ejecutar _**git show**_ se pueden pasar uno o varios commits, y se mostrará la información del commit individualmente  respecto al anterior.

En cambio, si ejecutamos _**git diff**_, por lo general, se tendrán que pasar dos archivos para compararlos en el rango correspondiente. Y de esta manera, se verán los cambios en el rango descrito.





















