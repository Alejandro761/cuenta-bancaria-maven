# Cuenta bancaria — Maven

**Autor:** Alejandro Elías Castañeda Ibarra

## Cómo construir y correr

    ./mvnw clean package
    java -jar target/cuenta-bancaria-maven-1.0.0.jar

## Qué hay en este proyecto

| Qué | Dónde |
|---|---|
| El programa (estado de cuenta en texto y en JSON) | `src/main/java/com/academia/banco/App.java` |
| Las pruebas | `src/test/java/com/academia/banco/` |
| La evidencia de cada mini-práctica | `evidencia/` |
| Los 5 errores de Maven que encontré | `evidencia/errores-maven.md` |

## Boleto de salida

1. ¿Qué diferencia hay entre `./mvnw package` y `./mvnw install`?

Ambos compilan y generan el .jar, package lo deja en la carpeta del proyecto (target/) e install tanto en el proyecto como en una ruta global para que sea consumido por otros proyectos.

2. ¿Por qué `compile` pasó pero `java -jar` falló en la MP-3?

Porque el compilador recibe los .jar de jackson, pero java -jar solo trae las clases sin jackson.

3. En tu proyecto de Spring Boot, ¿de dónde sale la versión de una dependencia que no tiene `<version>`?

En el archivo maven-wrapper.properties.

4. ¿Qué va en `settings.xml` y no en `pom.xml`? ¿Por qué?

El pom vive en el proyecto, van las dependencias del mismo, es el que se sube a repositorios (como git). El settings contiene contraseñas y configuraciones delicadas, siempre se queda en local.