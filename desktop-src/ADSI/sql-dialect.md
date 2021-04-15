---
title: Диалект SQL
description: Диалект SQL, производный от язык SQL, использует выражения, предназначенные для чтения, для определения инструкций запроса.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- ИНТЕРФЕЙС для диалектов SQL
- диалекты ADSI, диалект SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654100"
---
# <a name="sql-dialect"></a>Диалект SQL

Диалект SQL, производный от язык SQL, использует выражения, предназначенные для чтения, для определения инструкций запроса. Используйте инструкцию SQL-запроса со следующими интерфейсами поиска ADSI:

-   Интерфейсы [объектов данных ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , которые являются интерфейсами автоматизации, использующими OLE DB.
-   [OLE DB](searching-with-ole-db.md), который представляет собой набор интерфейсов C/C++ для запросов к базам данных.

Для инструкций SQL требуется следующий синтаксис.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



В следующей таблице перечислены ключевые слова инструкции SQL Query.



| Ключевое слово  | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Задает разделенный запятыми список атрибутов, которые необходимо получить для каждого объекта. Если указать \* , запрос извлекает только путь к каждому объекту.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Указывает путь к основному элементу поиска. Например, путь к контейнеру пользователей в домене Active Directory может иметь значение "LDAP://кН = Users, DC = Fabrikam, DC = COM". Имейте в виду, что путь заключается в пару одинарных кавычек (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Необязательное ключевое слово, указывающее фильтр запроса.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Необязательное ключевое слово, которое создает сортировку на стороне сервера, если сервер поддерживает управление сортировкой LDAP. Active Directory поддерживает элемент управления Sort, но он может повлиять на производительность сервера, особенно если результирующий набор имеет большой размер. Список сортировки — это разделенный запятыми список атрибутов, по которым выполняется сортировка. Имейте в виду, что Active Directory поддерживает только один ключ сортировки. Для задания порядка сортировки по возрастанию или убыванию можно использовать необязательные ключевые слова ASC и DESC. значение по умолчанию — Ascending. Ключевое слово ORDER BY переопределяет любой ключ сортировки, указанный с помощью свойства Sort для объекта команды ADO. |



 

> [!Note]  
> В случаях, когда используется многобайтовый набор символов, то если поиск выполняется ADO с использованием диалекта SQL, то обратная косая черта не может использоваться для экранирования символов. Вместо этого необходимо использовать escape-последовательности, перечисленные в [специальных символах](search-filter-syntax.md) . Например, для инструкции, использующей синтаксис "samAccountName = \( Test", которая использует обратную косую черту, " \\ ", чтобы экранировать открывающую скобку "(", вместо нее следует заменить обратную косую чертой на специальный символ " \\ 28", как показано ниже: "SamAccountName = \\ 28Test".

 

Следующие инструкции запросов являются примерами диалекта SQL в ADSI.

Для поиска всех объектов группы.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Для поиска всех пользователей с фамилией, начинающейся с буквы H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



Формальная грамматика для запросов SQL определяется в следующем примере кода. Все ключевые слова не учитывают регистр.


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



Внутренние объединения SQL не поддерживаются поставщиком Active Directory OLE DB, но можно использовать SQL для объединения данных SQL и Active Directory. Дополнительные сведения см. [в разделе Создание разнородного объединения между SQL Server и Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Синтаксис фильтра поиска](search-filter-syntax.md)
</dt> <dt>

[Диалект LDAP](ldap-dialect.md)
</dt> <dt>

[Поиск с помощью интерфейса IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Поиск с помощью OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




