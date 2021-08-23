---
title: SQL Указанный
description: диалект SQL, производный от язык SQL, использует выражения, предназначенные для чтения, для определения инструкций запроса.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL Диалекты ADSI
- диалекты ADSI, диалект SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7483a5e3785f410e6c2fd875122ba24618a82b70d1ed6dc9a85105ae4e8dcfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262054"
---
# <a name="sql-dialect"></a>SQL Указанный

диалект SQL, производный от язык SQL, использует выражения, предназначенные для чтения, для определения инструкций запроса. используйте инструкцию запроса SQL со следующими интерфейсами поиска ADSI:

-   интерфейсы [объектов данных ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , которые являются интерфейсами автоматизации, использующими OLE DB.
-   [OLE DB](searching-with-ole-db.md), который представляет собой набор интерфейсов C/C++ для запросов к базам данных.

для SQL инструкций требуется следующий синтаксис.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



в следующей таблице перечислены ключевые слова инструкции запроса SQL.



| Ключевое слово  | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Задает разделенный запятыми список атрибутов, которые необходимо получить для каждого объекта. Если указать \* , запрос извлекает только путь к каждому объекту.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Указывает путь к основному элементу поиска. Например, путь к контейнеру пользователей в домене Active Directory может иметь значение "LDAP://кН = Users, DC = Fabrikam, DC = COM". Имейте в виду, что путь заключается в пару одинарных кавычек (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Необязательное ключевое слово, указывающее фильтр запроса.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Необязательное ключевое слово, которое создает сортировку на стороне сервера, если сервер поддерживает управление сортировкой LDAP. Active Directory поддерживает элемент управления Sort, но он может повлиять на производительность сервера, особенно если результирующий набор имеет большой размер. Список сортировки — это разделенный запятыми список атрибутов, по которым выполняется сортировка. Имейте в виду, что Active Directory поддерживает только один ключ сортировки. Для задания порядка сортировки по возрастанию или убыванию можно использовать необязательные ключевые слова ASC и DESC. значение по умолчанию — Ascending. Ключевое слово ORDER BY переопределяет любой ключ сортировки, указанный с помощью свойства Sort для объекта команды ADO. |



 

> [!Note]  
> в случаях, когда используется многобайтовый набор символов, поиск выполняется ADO с помощью SQL диалекта, а обратная косая черта не может использоваться для экранирования символов. Вместо этого необходимо использовать escape-последовательности, перечисленные в [специальных символах](search-filter-syntax.md) . Например, для инструкции, использующей синтаксис "samAccountName = \( Test", которая использует обратную косую черту, " \\ ", чтобы экранировать открывающую скобку "(", вместо нее следует заменить обратную косую чертой на специальный символ " \\ 28", как показано ниже: "SamAccountName = \\ 28Test".

 

следующие инструкции запроса являются примерами SQL диалекта в ADSI.

Для поиска всех объектов группы.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Для поиска всех пользователей с фамилией, начинающейся с буквы H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



формальная грамматика для SQL запросов определяется в следующем примере кода. Все ключевые слова не учитывают регистр.


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



SQL внутренние объединения не поддерживаются поставщиком Active Directory OLE DB, но для объединения SQL и Active Directory данных можно использовать SQL. дополнительные сведения см. [в разделе создание разнородного объединения между SQL Server и Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Синтаксис фильтра поиска](search-filter-syntax.md)
</dt> <dt>

[Диалект LDAP](ldap-dialect.md)
</dt> <dt>

[Поиск с помощью интерфейса IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Поиск с помощью OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




