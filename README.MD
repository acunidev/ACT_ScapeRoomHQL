### En el projecte tens tambe el docker-compose.yml que he utilitzat per crear el docker.

Hibernate: select count(m1_0.idModulo) from Modulo m1_0</br>
Hibernate: select distinct e1_0.idModul from Examen e1_0 where e1_0.idModul>0</br>
Hibernate: select round(avg(e1_0.nota),0) from Examen e1_0 join Modulo m1_0 on 1 where m1_0.idModulo=e1_0.idModul and m1_0.nombre like '%PRG%'</br>
Hibernate: select a1_0.idAlumno,a1_0.apellidos,a1_0.edad,a1_0.nombre,a1_0.repetidor from Alumno a1_0 where a1_0.apellidos like '%z%'</br>
### El código descubierto es : 6473
```java
    public static int codigo1() {
        //TO-DO
        Query query = session1.createQuery("SELECT COUNT(m.idModulo) from ModuloEntity m");
        long x  = (long) query.getResultList().get(0);
        return (int)x;
    }
    public static int codigo2() {
        //TO-DO
        Query query = session1.createQuery("SELECT DISTINCT (e.idModul) from ExamenEntity e where e.idModul > 0");
        int x  = query.getResultList().size();
        return x; }
    public static int codigo3() {
        //TO-DO
        Query query = session1.createQuery("SELECT ROUND(AVG(e.nota),0) FROM ExamenEntity e JOIN ModuloEntity m WHERE m.id = e.idModul AND m.nombre LIKE '%PRG%'");
        double result = (double) query.getResultList().get(0);
        return (int) result;
    }
    public static int codigo4() {
        //TO-DO0
        Query query =  session1.createQuery("SELECT (e) FROM AlumnoEntity e WHERE e.apellidos LIKE '%z%'");
        int x  = query.getResultList().size();
        return x;
    }

```