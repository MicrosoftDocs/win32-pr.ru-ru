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
# <a name="sql-dialect"></a><span data-ttu-id="51f05-105">Диалект SQL</span><span class="sxs-lookup"><span data-stu-id="51f05-105">SQL Dialect</span></span>

<span data-ttu-id="51f05-106">Диалект SQL, производный от язык SQL, использует выражения, предназначенные для чтения, для определения инструкций запроса.</span><span class="sxs-lookup"><span data-stu-id="51f05-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="51f05-107">Используйте инструкцию SQL-запроса со следующими интерфейсами поиска ADSI:</span><span class="sxs-lookup"><span data-stu-id="51f05-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="51f05-108">Интерфейсы [объектов данных ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , которые являются интерфейсами автоматизации, использующими OLE DB.</span><span class="sxs-lookup"><span data-stu-id="51f05-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="51f05-109">[OLE DB](searching-with-ole-db.md), который представляет собой набор интерфейсов C/C++ для запросов к базам данных.</span><span class="sxs-lookup"><span data-stu-id="51f05-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="51f05-110">Для инструкций SQL требуется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="51f05-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="51f05-111">В следующей таблице перечислены ключевые слова инструкции SQL Query.</span><span class="sxs-lookup"><span data-stu-id="51f05-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="51f05-112">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="51f05-112">Keyword</span></span>  | <span data-ttu-id="51f05-113">Описание</span><span class="sxs-lookup"><span data-stu-id="51f05-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f05-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="51f05-114">SELECT</span></span>   | <span data-ttu-id="51f05-115">Задает разделенный запятыми список атрибутов, которые необходимо получить для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="51f05-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="51f05-116">Если указать \* , запрос извлекает только путь к каждому объекту.</span><span class="sxs-lookup"><span data-stu-id="51f05-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="51f05-117">FROM</span><span class="sxs-lookup"><span data-stu-id="51f05-117">FROM</span></span>     | <span data-ttu-id="51f05-118">Указывает путь к основному элементу поиска.</span><span class="sxs-lookup"><span data-stu-id="51f05-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="51f05-119">Например, путь к контейнеру пользователей в домене Active Directory может иметь значение "LDAP://кН = Users, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="51f05-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="51f05-120">Имейте в виду, что путь заключается в пару одинарных кавычек (').</span><span class="sxs-lookup"><span data-stu-id="51f05-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="51f05-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="51f05-121">WHERE</span></span>    | <span data-ttu-id="51f05-122">Необязательное ключевое слово, указывающее фильтр запроса.</span><span class="sxs-lookup"><span data-stu-id="51f05-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="51f05-123">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="51f05-123">ORDER BY</span></span> | <span data-ttu-id="51f05-124">Необязательное ключевое слово, которое создает сортировку на стороне сервера, если сервер поддерживает управление сортировкой LDAP.</span><span class="sxs-lookup"><span data-stu-id="51f05-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="51f05-125">Active Directory поддерживает элемент управления Sort, но он может повлиять на производительность сервера, особенно если результирующий набор имеет большой размер.</span><span class="sxs-lookup"><span data-stu-id="51f05-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="51f05-126">Список сортировки — это разделенный запятыми список атрибутов, по которым выполняется сортировка.</span><span class="sxs-lookup"><span data-stu-id="51f05-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="51f05-127">Имейте в виду, что Active Directory поддерживает только один ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="51f05-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="51f05-128">Для задания порядка сортировки по возрастанию или убыванию можно использовать необязательные ключевые слова ASC и DESC. значение по умолчанию — Ascending.</span><span class="sxs-lookup"><span data-stu-id="51f05-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="51f05-129">Ключевое слово ORDER BY переопределяет любой ключ сортировки, указанный с помощью свойства Sort для объекта команды ADO.</span><span class="sxs-lookup"><span data-stu-id="51f05-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="51f05-130">В случаях, когда используется многобайтовый набор символов, то если поиск выполняется ADO с использованием диалекта SQL, то обратная косая черта не может использоваться для экранирования символов.</span><span class="sxs-lookup"><span data-stu-id="51f05-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="51f05-131">Вместо этого необходимо использовать escape-последовательности, перечисленные в [специальных символах](search-filter-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="51f05-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="51f05-132">Например, для инструкции, использующей синтаксис "samAccountName = \( Test", которая использует обратную косую черту, " \\ ", чтобы экранировать открывающую скобку "(", вместо нее следует заменить обратную косую чертой на специальный символ " \\ 28", как показано ниже: "SamAccountName = \\ 28Test".</span><span class="sxs-lookup"><span data-stu-id="51f05-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="51f05-133">Следующие инструкции запросов являются примерами диалекта SQL в ADSI.</span><span class="sxs-lookup"><span data-stu-id="51f05-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="51f05-134">Для поиска всех объектов группы.</span><span class="sxs-lookup"><span data-stu-id="51f05-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="51f05-135">Для поиска всех пользователей с фамилией, начинающейся с буквы H.</span><span class="sxs-lookup"><span data-stu-id="51f05-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="51f05-136">Формальная грамматика для запросов SQL определяется в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="51f05-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="51f05-137">Все ключевые слова не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="51f05-137">All keywords are case-insensitive.</span></span>


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



<span data-ttu-id="51f05-138">Внутренние объединения SQL не поддерживаются поставщиком Active Directory OLE DB, но можно использовать SQL для объединения данных SQL и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="51f05-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="51f05-139">Дополнительные сведения см. [в разделе Создание разнородного объединения между SQL Server и Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="51f05-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51f05-140">См. также</span><span class="sxs-lookup"><span data-stu-id="51f05-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51f05-141">Синтаксис фильтра поиска</span><span class="sxs-lookup"><span data-stu-id="51f05-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="51f05-142">Диалект LDAP</span><span class="sxs-lookup"><span data-stu-id="51f05-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="51f05-143">Поиск с помощью интерфейса IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="51f05-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="51f05-144">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="51f05-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="51f05-145">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="51f05-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




