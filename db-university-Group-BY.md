ESERCIZIO 1

<!--1 Contare quanti iscritti ci sono stati ogni anno -->

SELECT COUNT(\*) AS "NUMERO_RISULTATI",YEAR (`enrolment_date`) FROM `students` GROUP BY YEAR (`enrolment_date`);

ESERCIZIO 2

<!-- 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio -->

SELECT COUNT(\*) AS "NUMERO_INSEGNANTI",`office_address` FROM `teachers` GROUP BY `office_address`;

<!-- 3. Calcolare la media dei voti di ogni appello d'esame -->

ESERCIZIO 4

<!-- 4. Contare quanti corsi di laurea ci sono per ogni dipartimento -->

SELECT COUNT(\*) AS "corsi_laurea", `department_id` AS "NUMERO_DIPARTIMENTO"  
FROM `degrees`
GROUP BY `department_id`;
