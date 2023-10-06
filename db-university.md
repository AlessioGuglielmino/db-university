<!-- seleziona tutti gli studenti che sono nati nel 1990 (160) -->

SELECT \* FROM `students` WHERE YEAR (`date_of_birth`) = '1990';

<!-- seleziona tutti i corsi con crediti maggiorni di 10 -->

SELECT \* FROM `courses` WHERE `cfu`>10;

<!-- tutti gli studenti con piu di 30 anni -->

SELECT \* FROM `students` WHERE `date_of_birth`<= '1992-10-06';

<!-- Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286) -->

SELECT \* FROM `courses` WHERE`period` = 'I semestre' AND `year`= 1;

<!-- Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21) -->

SELECT \* FROM `exams` WHERE `date` ='2020/06/20' AND time (`hour`) > '14%';

<!-- Selezionare tutti i corsi di laurea magistrale (38) -->

SELECT \* FROM `degrees` WHERE`level`= 'magistrale';

 <!-- Da quanti dipartimenti è composta l'università? (12) -->

SELECT COUNT(`id`)AS departments_number FROM `departments`;
SELECT \* FROM `departments` WHERE `id`>0;

<!-- Quanti sono gli insegnanti che non hanno un numero di telefono? (50) -->

SELECT \* FROM `teachers` WHERE `phone` IS NULL;
