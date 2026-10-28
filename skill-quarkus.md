# Skill quarkus-best-practices
### Copiar el siguiente Prompt para crear el skill una vez ejecutado el comando $skill-creator:

```
1. Skill name: ‘quarkus-best-practices’ 
2. Create new Skill, description: que Genere un proyecto con la estructura de quarkus con capas de controllers, services, repository y models.
3. Location for skill folder, crealo dentro del directorio del proyecto ‘.claude/skills‘
4. Specific Instructions:
    - Genera el proyecto usando la herramienta oficial desde Quarkus Code: https://code.quarkus.io
    - usa java version 25
    - usa quarkus 3.40.1 LTS o superior disponible revisar en documentación de quarkus en quarkus.io
    - usa configuracion basada en properties: application.properties
    - usa packaging jar
    - usa maven como package manager
    - group-id de maven com.andres.course.claude.quarkus
    - nombre del proyecto o artifact-id maven mismo que el directorio workspace del proyecto
    - package base de quarkus com.andres.course.claude.quarkus.{artifactId}.app
    - revisar e incluir dependencias base, quarkus-rest-jackson (Quarkus REST Jackson), quarkus-arc, quarkus-hibernate-validator, quarkus-smallrye-openapi (SmallRye OpenAPI)
    - Habilitar Live Coding, Hot Reload y Dev UI mediante Quarkus Dev Mode
    - incluir Maven Wrapper (mvnw) en folder `.mvn` y ejecutable `./mvnw` y `./mvnw.cmd`
    - arquitectura repository/service/controller
    - crear estructura base con packages models, controllers, repositories y services
    - `controller`: expone únicamente puntos finales REST, valida la entrada, delega a servicios y devuelve DTO
    - `service`: contiene lógica de negocios, organiza repositorios y convierte entre entidades y DTO
    - repositorios como interfaces que extienden PanacheRepository.
    - para dto usar record en vez de class, excluir campos sensibles como password, created_at, updated_at, create_at, update_at, usar mismo dto request y response
    - Agregue clase Mapper, un mapeador para que el servicio pueda convertir entre DTO y entidades explícitamente. mapper convert `entity -> dto` and `dto -> entity`
    - Cuando necesite iniciar la aplicación localmente con Maven, siempre prefiera `./mvnw quarkus:dev` como comando de ejecución predeterminado.
    - registrar en CLAUDE.md: Available skills y Skill trigger rules, si no existe lo creas
    - Persistencia con Hibernate ORM, Panache (quarkus-hibernate-orm-panache) y PostgreSQL (quarkus-jdbc-postgresql).
5. Activation Triggers: cuando el usuario pide crear una API básica para `quarkus`. Tambien cuando el usuario pida crear o agregar o modificar un entity, repository, service o controller de quarkus.

```
