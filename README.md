# ALL-TABLES-IN-THE-DATABASE
The database is composed of the following tables:

- persona

- entrenamientos

- detalle_entrenamiento

- ejercicios

- musculos

Below is a brief explanation of each table and how they relate to each other.

👤 Table persona

This table stores the people who participated in the project.

Main fields:

id_persona (PK)

nombre

Each person can have multiple training sessions registered.

🏋️ Table entrenamientos

This table records the days when a person attended the gym.

Main fields:

id_entrenamiento (PK)

id_persona (FK)

fecha

Relationship:

One training session belongs to one person.

One person can have multiple training sessions.

📋 Table detalle_entrenamiento

This table stores the exercises performed in each training session and the number of repetitions.

Main fields:

id_detalle (PK)

id_entrenamiento (FK)

id_ejercicio (FK)

repeticiones

Relationship:

One training session can include multiple exercises.

Each record specifies which exercise was performed and how many repetitions were completed.

💪 Table ejercicios

This table contains the available exercises.

Main fields:

id_ejercicio (PK)

nombre

id_musculo (FK)

Relationship:

Each exercise targets a specific muscle.

One muscle can be associated with multiple exercises.

🦵 Table musculos

This table contains the muscles that can be trained.

Main fields:

id_musculo (PK)

nombre

🔗 Relationship Summary

persona 1:N entrenamientos

entrenamientos 1:N detalle_entrenamiento

ejercicios 1:N detalle_entrenamiento

musculos 1:N ejercicios
