# Errores de Maven que encontré

| Queja | La línea clave que dijo Maven | La causa | Cómo lo arreglé |
|---|---|---|---|
| 1 | 27 | El tag de una dependencia no estaba cerrado con dependency | Corregí ese error, en vez de dependencia puse dependency |
| 2 | 14 | La versión de java está en 21 | Borre esa versión y puse la 17, el cuál es la versión instalada en la máquina |
| 3 | 18 | La versión 2.22.30 para jackson-databind no existe | Puse una versión válida: 2.22.3 |
| 4 | 27 | El scope de jackson está puesto solo en test, por lo tanto el main no la encuentra | Borrar el scope, automáticamente lo encontrara tanto test como main |
| 5 | 45 | El mainClass tenia Aplicacion, el cual no tiene el método main y tampoco existe | Lo corregí poniendo App, el cual contiene el método main |