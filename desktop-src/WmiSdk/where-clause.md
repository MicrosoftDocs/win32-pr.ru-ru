---
description: Используйте предложение WHERE, чтобы ограничить область запроса данных, события или схемы.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Предложение WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703249"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="fca20-103">Предложение WHERE (WMI)</span><span class="sxs-lookup"><span data-stu-id="fca20-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="fca20-104">Используйте предложение WHERE, чтобы ограничить область запроса данных, события или схемы.</span><span class="sxs-lookup"><span data-stu-id="fca20-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="fca20-105">Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="fca20-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="fca20-106">Предложение WHERE состоит из свойства или ключевого слова, оператора и константы.</span><span class="sxs-lookup"><span data-stu-id="fca20-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="fca20-107">Все предложения WHERE должны указывать один из предопределенных операторов, которые включены в инструментарий управления Windows (WMI) (WQL) Language.</span><span class="sxs-lookup"><span data-stu-id="fca20-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="fca20-108">К инструкции SELECT можно добавить предложение WHERE, используя одну из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="fca20-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="fca20-109">где \* — запрашивается элемент, класс — это класс, в котором следует запрашивать, а константа, оператор и свойство — константа, оператор, свойство или ключевое слово для использования.</span><span class="sxs-lookup"><span data-stu-id="fca20-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="fca20-110">Дополнительные сведения об инструкции SELECT см. в статьях [инструкция SELECT для запросов данных](select-statement-for-data-queries.md), [инструкция SELECT для запросов событий](select-statement-for-event-queries.md)или [инструкция SELECT для запросов схемы](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="fca20-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="fca20-111">Значение константы должно иметь правильный тип для свойства.</span><span class="sxs-lookup"><span data-stu-id="fca20-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="fca20-112">Более того, оператор должен быть в списке допустимых [операторов WQL](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="fca20-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="fca20-113">Либо имя свойства, либо константа должны присутствовать в обеих сторонах оператора в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="fca20-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="fca20-114">В предложении WHERE можно использовать строковые литералы, например "NTFS".</span><span class="sxs-lookup"><span data-stu-id="fca20-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="fca20-115">Если вы хотите включить в строку следующие специальные символы, необходимо сначала выполнить escape-последовательность символа, добавив обратную косую черту ( \) :</span><span class="sxs-lookup"><span data-stu-id="fca20-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\):</span></span>

-   <span data-ttu-id="fca20-116">знака\\\)</span><span class="sxs-lookup"><span data-stu-id="fca20-116">backslash (\\\)</span></span>
-   <span data-ttu-id="fca20-117">двойные кавычки ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="fca20-117">double quotes (\\")</span></span>
-   <span data-ttu-id="fca20-118">одинарные кавычки ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="fca20-118">single quotes (\\')</span></span>

<span data-ttu-id="fca20-119">Нельзя использовать произвольные арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="fca20-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="fca20-120">Например, следующий запрос возвращает только экземпляры класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , представляющие диски NTFS:</span><span class="sxs-lookup"><span data-stu-id="fca20-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="fca20-121">Имена свойств не могут присутствовать на обеих сторонах оператора.</span><span class="sxs-lookup"><span data-stu-id="fca20-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="fca20-122">Следующий запрос является примером недопустимого запроса:</span><span class="sxs-lookup"><span data-stu-id="fca20-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="fca20-123">Для большинства случаев использования дескрипторов классов в предложении WHERE WMI помечает запрос как недопустимый и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fca20-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="fca20-124">Однако используйте оператор dot (.) для свойств типа **Object** в WMI.</span><span class="sxs-lookup"><span data-stu-id="fca20-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="fca20-125">Например, следующий запрос допустим, если свойство prop является допустимым свойством MyClass и имеет тип **Object**:</span><span class="sxs-lookup"><span data-stu-id="fca20-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="fca20-126">В тестах сравнения всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fca20-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="fca20-127">То есть следующие три оператора имеют **значение true**:</span><span class="sxs-lookup"><span data-stu-id="fca20-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="fca20-128">Можно создать запрос, включающий логические типы данных, но единственными допустимыми типами логических операндов являются типы =,! = и <> .</span><span class="sxs-lookup"><span data-stu-id="fca20-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="fca20-129">Значение **true** эквивалентно числу 1, а значение **false** эквивалентно числу 0.</span><span class="sxs-lookup"><span data-stu-id="fca20-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="fca20-130">Следующие примеры представляют собой запросы, которые сравнивают логическое значение со значениями **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="fca20-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



<span data-ttu-id="fca20-131">Следующие примеры имеют недопустимые запросы, пытающиеся использовать недопустимые операнды.</span><span class="sxs-lookup"><span data-stu-id="fca20-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="fca20-132">Несколько групп свойств, операторов и констант можно комбинировать в предложении WHERE с помощью логических операторов и вложенных выражений в скобках.</span><span class="sxs-lookup"><span data-stu-id="fca20-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="fca20-133">Каждая группа должна быть соединена с [операторами](wql-operators.md) and, or или not, как показано в следующих запросах.</span><span class="sxs-lookup"><span data-stu-id="fca20-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="fca20-134">Первый запрос получает все экземпляры класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , для свойства **Name** которых задано значение C или D:</span><span class="sxs-lookup"><span data-stu-id="fca20-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="fca20-135">Второй запрос извлекает диски с именем "C:" или "D:" только в том случае, если они имеют определенный объем свободного места и имеют файловые системы NTFS:</span><span class="sxs-lookup"><span data-stu-id="fca20-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="fca20-136">В этом примере показан запрос схемы с помощью предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="fca20-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="fca20-137">Класс meta класса \_ определяет это как запрос схемы, свойство, именуемое, \_ \_ определяет целевой класс запроса, а [оператор ISA](isa-operator-for-schema-queries.md) запрашивает определения для подклассов целевого класса.</span><span class="sxs-lookup"><span data-stu-id="fca20-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="fca20-138">Таким образом, предыдущий запрос возвращает определение класса Микласснаме и определения для всех его подклассов.</span><span class="sxs-lookup"><span data-stu-id="fca20-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="fca20-139">В следующем примере показан запрос данных с помощью [соединителей оператора с предложением](associators-of-statement.md) WHERE:</span><span class="sxs-lookup"><span data-stu-id="fca20-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="fca20-140">В следующем примере показан запрос схемы, использующий СОЕДИНИТЕЛи и где:</span><span class="sxs-lookup"><span data-stu-id="fca20-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="fca20-141">Следующий пример представляет собой запрос данных, использующий [ссылки на инструкцию](references-of-statement.md) и где:</span><span class="sxs-lookup"><span data-stu-id="fca20-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="fca20-142">Последний пример — запрос схемы, в котором используются ссылки и где:</span><span class="sxs-lookup"><span data-stu-id="fca20-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="fca20-143">Помимо формата [DateTime](date-and-time-format.md) WMI, предложение WHERE языка WQL поддерживает несколько других форматов даты и времени:</span><span class="sxs-lookup"><span data-stu-id="fca20-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="fca20-144">Форматы даты, поддерживаемые WQL</span><span class="sxs-lookup"><span data-stu-id="fca20-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="fca20-145">Поддерживаемые форматы времени WQL</span><span class="sxs-lookup"><span data-stu-id="fca20-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
