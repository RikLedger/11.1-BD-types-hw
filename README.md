# Домашнее задание к занятию 11.1. «Базы данных, их типы» - `Горбачев Олег`

---

### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 

---
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков.
СУБД должна гарантировать целостность и чёткую структуру данных.


*"гарантировать целостность и чёткую структуру данных" - реляционная субд.*

---

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к 
маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? 
СУБД должны быть гибкими и быстрыми.


*Подойдет графовая СУБД, либо реляционная.*

---

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу 
и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.


*Подойдет документная СУБД.*

---

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов 
по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать
со связями.


*Можно использовать колоночную СУБД, возможно что будет производительнее, чем реляционная.*

*Все задачи можно решить, используя реляционную СУЬД - PostgreSQL.*

---

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы 
транзакция завершилась успешно. Ориентируйтесь на шесть действий.

*Приведите ответ в свободной форме.*

*- Начало транзакции.*
*- Определение суммы, на которую будет пополнен счёт.*
*- Проверка баланса пополняемого счёта.*
*- Пополнение баланса на определённую сумму.*
*- Сохранение баланса полполняемого счёта.* 
*- Окончание транзакции.*

*Начало транзакции - start transaction или автоматически, по факту первой изменяющей операции. Окончание транзакции - commit. Применимо ко всем транзакциям.*

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 

Приведите ответ в свободной форме.

*- стандартизированный язык запросов*
*- атомарность*
*- согласованность*
*- изоляция*
*- долговечность* 

---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу 
выделено 1000 машин. 

На основе какого критерия будете выбирать тип СУБД и какая модель *распределённых вычислений* 
здесь справится лучше всего и почему?

Приведите ответ в свободной форме.

*Буду опираться на необходимость поддержки транзакций. Колоночная или реляционная СУБД.*
*Если более важна целостность данных, запросы осуществляемые к субд не слишком сложные, а количество строк относительно небольшое - реляционная СУБД.*
*Если более важно быстродействие, запросы осуществляемые к субд - сложные, а количество стро исчисляется сотнями тысяч - колоночная СУБД.*

---
