### Bloque 1

##### Consultas

1.  Listar los nombres de los usuarios

    ```sql
    # Solucion en 'sql'
     select nombre from tblUsuarios;
    ```

2.  Calcular el saldo máximo de los usuarios de sexo “Mujer”

    ```sql
     # Solucion en 'sql'
     select nombre ,   max(saldo) from tblusuarios where sexo = 'M';

    ```

3.  Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

    ```sql
          # Solucion en 'sql'
          select nombre,telefono from tblUsuarios Where marca = "NOKIA" Or marca = "BLACKBERRY" Or marca="SONY";

    ```

4.  Contar los usuarios sin saldo o inactivos

    ```sql
     # Solucion en 'sql'
     select   COUNT(*) as usuarios from tblusuarios where saldo =0 or activo = false;
    ```

5.  Listar el login de los usuarios con nivel 1, 2 o 3

         ```sql
          # Solucion en 'sql'
          select usuario from tblusuarios where nivel = 1 or nivel = 2 or nivel = 3 ;

    ```

    ```

6.  Listar los números de teléfono con saldo menor o igual a 300

    ```sql
     # Solucion en 'sql'
     SELECT telefono FROM tblUsuarios WHERE (saldo <= 300);
    ```

7.  Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

    ```sql
     # Solucion en 'sql'
    select sum(saldo) as cantidad from tblusuarios where compañia = 'NEXTEL';
    ```

8.  Contar el número de usuarios por compañía telefónica

         ```sql
          # Solucion en 'sql'
          select compañia, count(idx) as cantidad from tblusuarios group by compañia;

    ```

    ```

9.  Contar el número de usuarios por nivel

         ```sql
          # Solucion en 'sql'
          select nivel, count(idx) as cantidad from tblusuarios group by nivel;

    ```

    ```

10. Listar el login de los usuarios con nivel 2

          ```sql
           # Solucion en 'sql'
           select nivel, count(idx) as cantidad from tblusuarios where nivel = 2;

          ```

11. Mostrar el email de los usuarios que usan gmail

    ```sql
     # Solucion en 'sql'
     select email from tblusuarios where email like "%gmail%";
    ```

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

    ```sql
     # Solucion en 'sql'
         select nombre , telefono from tblusuarios where marca in ('LG' , 'MOTOROLA' ,'SAMSUNG');
    ```

---

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

   ```sql
    # Solucion en 'sql'
    select nombre , telefono from tblusuarios where marca not in ('LG','SAMSUNG');
   ```

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

   ```sql
    # Solucion en 'sql'
    select nombre, email, telefono from tblUsuarios where compañia = "IUSACELL";
   ```

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

   ```sql
    # Solucion en 'sql'
    select nombre, email, telefono from tblUsuarios where compañia not in ("IUSACELL");
   ```

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

   ```sql
    # Solucion en 'sql'
    select avg(saldo) as promedio from tblusuarios where marca = 'NOKIA';
   ```

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

   ```sql
    # Solucion en 'sql'
    select usuario , email from tblusuarios where compañia in ('IUSACELL','AXEL');
   ```

6. Mostrar el email de los usuarios que no usan yahoo

   ```sql
    # Solucion en 'sql'
    select email from tblUsuarios where email NOT LIKE ("%yahoo%");
   ```

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

   ```sql
    # Solucion en 'sql'
    select usuario , email from tblusuarios where compañia not in ('IUSACELL','TELCEL');
   ```

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

   ```sql
    # Solucion en 'sql'
    select usuario , email from tblusuarios where compañia not in ('UNEFON');

   ```

9. Listar las diferentes marcas de celular en orden alfabético descendentemente

   ```sql
    # Solucion en 'sql'
    select marca from tblusuarios order by marca desc ;
   ```

10. Listar las diferentes compañias en orden alfabético aleatorio

    ```sql
     # Solucion en 'sql'
     select compañia from tblusuarios ;
    ```

11. Listar el login de los usuarios con nivel 0 o 2

    ```sql
     # Solucion en 'sql'
     select nivel, nombre, email from tblUsuarios where nivel IN (0,2) order by nivel;
    ```

12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

    ```sql
     # Solucion en 'sql'
     select marca, AVG(saldo) AS saldo_promedio from tblUsuarios where marca = "LG" group by marca;
    ```

---

### Bloque 3

##### Consultas

1.  Listar el login de los usuarios con nivel 1 o 3

    ```sql
     # Solucion en 'sql'
    select usuario , email from tblusuarios where nivel in(1,3);
    ```

2.  Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

    ```sql
     # Solucion en 'sql'
     select nombre, telefono from tblUsuarios where not marca = "BLACKBERRY";
    ```

3.  Listar el login de los usuarios con nivel 3

    ```sql
     # Solucion en 'sql'
     select usuario , email from tblusuarios where nivel in(3);
    ```

4.  Listar el login de los usuarios con nivel 0

    ```sql
     # Solucion en 'sql'
     select usuario , email from tblusuarios where nivel in(0);
    ```

5.  Listar el login de los usuarios con nivel 1

    ```sql
     # Solucion en 'sql'
     select usuario , email from tblusuarios where nivel in(1);
    ```

6.  Contar el número de usuarios por sexo

         ```sql
          # Solucion en 'sql'
          select sexo ,  count(idx) as usuarios from tblusuarios group by sexo;

    ```

    ```

7.  Listar el login y teléfono de los usuarios con compañia telefónica AT&T

    ```sql
     # Solucion en 'sql'
      select nombre, email, telefono from tblUsuarios where compañia ="AT&T";

    ```

8.  Listar las diferentes compañias en orden alfabético descendentemente

    ```sql
     # Solucion en 'sql'
    select distinct compañia from tblUsuarios order by compañia desc;
    ```

9.  Listar el logn de los usuarios inactivos

    ```sql
     # Solucion en 'sql'
     select usuario , email from tblusuarios where activo = false;
    ```

10. Listar los números de teléfono sin saldo

    ```sql
     # Solucion en 'sql'
     select telefono, saldo from tblUsuarios where saldo = 0;
    ```

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

    ```sql
     # Solucion en 'sql'
     select nombre, saldo from tblUsuarios where sexo = 'H' order by saldo asc limit 1;
    ```

12. Listar los números de teléfono con saldo mayor a 300

    ```sql
     # Solucion en 'sql'
     select telefono, saldo from tblUsuarios where (saldo >= 300);
    ```

---

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

   ```sql
    # Solucion en 'sql'
    select marca, count(idx) as cantidad from tblUsuarios group by marca;
   ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

   ```sql
    # Solucion en 'sql'
    select nombre , telefono from tblusuarios where marca not in ('Lg');
   ```

3. Listar las diferentes compañias en orden alfabético ascendentemente

   ```sql
    # Solucion en 'sql'
    select distinct compañia from tblUsuarios order by compañia asc;
   ```

4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

   ```sql
    # Solucion en 'sql'
    select compañia, sum(saldo) AS saldo_total from tblUsuarios where compañia = 'UNEFON' group by compañia;
   ```

5. Mostrar el email de los usuarios que usan hotmail

   ```sql
    # Solucion en 'sql'
    select email from tblUsuarios where email  LIKE ("%hotmail%");
   ```

6. Listar los nombres de los usuarios sin saldo o inactivos

   ```sql
    # Solucion en 'sql'
    select   nombre as nombres from tblusuarios where saldo =0 or activo = false;
   ```

7. Listar el login y teléfono de los usuarios con compañia telefónicaIUSACELL o TELCEL

   ```sql
    # Solucion en 'sql'
    select nombre, email, telefono from tblUsuarios where compañia in ('TELCEL', 'IUSACELL');
   ```

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

   ```sql
    # Solucion en 'sql'
    select  distinct marca from  tblusuarios order by  marca asc ;
   ```

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

   ```sql
    # Solucion en 'sql'
    select  distinct marca from  tblusuarios ;
   ```

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

    ```sql
     # Solucion en 'sql'
     select  nombre , email , telefono from  tblusuarios where compañia in ('UNEFON','IUSACELL');
    ```

11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

    ```sql
     # Solucion en 'sql'
     select  nombre, telefono from  tblusuarios where marca not in ('MOTOROLA','NOKIA');
    ```

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

    ```sql
     # Solucion en 'sql'
     select compañia, sum(saldo) AS saldo_total from tblUsuarios where compañia = 'TELCEL' group by compañia;
    ```
