---
description: Извлекает все экземпляры, связанные с определенным исходным экземпляром.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: СОЕДИНИТЕЛи оператора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347635"
---
# <a name="associators-of-statement"></a><span data-ttu-id="65fb5-103">СОЕДИНИТЕЛи оператора</span><span class="sxs-lookup"><span data-stu-id="65fb5-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="65fb5-104">СОЕДИНИТЕЛи оператора получают все экземпляры, связанные с определенным исходным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="65fb5-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="65fb5-105">Получаемые экземпляры называются конечными точками.</span><span class="sxs-lookup"><span data-stu-id="65fb5-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="65fb5-106">Каждая конечная точка возвращается столько раз, сколько существует связей между ней и исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="65fb5-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="65fb5-107">Например, предположим, что существуют экземпляры A, B, X и Y. Существуют два экземпляра ассоциаций, один из которых связывает A и X и другой, связывающий B и Y. Следующий запрос возвращает одну конечную точку X:</span><span class="sxs-lookup"><span data-stu-id="65fb5-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="65fb5-108">Однако если существует другая ассоциация, связывающая A и X, то приведенный выше запрос возвращает две конечные точки X.</span><span class="sxs-lookup"><span data-stu-id="65fb5-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="65fb5-109">Базовый синтаксис для СОЕДИНИТЕЛей оператора:</span><span class="sxs-lookup"><span data-stu-id="65fb5-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="65fb5-110">Обратите внимание, что фигурные скобки являются частью синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="65fb5-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="65fb5-111">Для Обжектпас можно использовать любой допустимый путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="65fb5-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="65fb5-112">Токены в пути к объекту не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="65fb5-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="65fb5-113">Например, запрос в следующем списке возвращает экземпляры, связанные с указанным логическим диском:</span><span class="sxs-lookup"><span data-stu-id="65fb5-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="65fb5-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="65fb5-116">Как и в случае с [инструкцией SELECT](select-statement-for-data-queries.md), соединители оператора могут включать [предложение WHERE](where-clause.md), но предложение WHERE для соединителей оператора очень отличается от предложения SELECT статементвхере.</span><span class="sxs-lookup"><span data-stu-id="65fb5-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="65fb5-117">[Предложение WHERE](where-clause.md) для соединителей оператора может включать одно или несколько из следующих стандартных ключевых слов и их значений:</span><span class="sxs-lookup"><span data-stu-id="65fb5-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



<span data-ttu-id="65fb5-118">Обратите внимание, что необязательные вложенные предложения не разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="65fb5-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="65fb5-119">Ключевое слово **ассоккласс** указывает, что возвращенные конечные точки должны быть связаны с источником через указанный класс или один из его производных классов.</span><span class="sxs-lookup"><span data-stu-id="65fb5-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="65fb5-120">Например, запрос в следующем списке возвращает только конечные точки, связанные с источником с помощью класса ассоциации [**Win32 \_ системдевицес**](/windows/desktop/CIMWin32Prov/win32-systemdevices) или любого из его производных классов:</span><span class="sxs-lookup"><span data-stu-id="65fb5-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="65fb5-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="65fb5-123">Ключевое слово **классдефсонли** указывает, что предложение возвращает результирующий набор объектов определения класса, а не фактических экземпляров классов.</span><span class="sxs-lookup"><span data-stu-id="65fb5-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="65fb5-124">Эти объекты являются определениями классов, к которым принадлежат экземпляры конечных точек.</span><span class="sxs-lookup"><span data-stu-id="65fb5-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="65fb5-125">Например, запрос, приведенный в следующем списке, возвращает определения для [**\_ каталога Win32**](/windows/desktop/CIMWin32Prov/win32-directory) и [**классов \_ Win32 ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :</span><span class="sxs-lookup"><span data-stu-id="65fb5-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="65fb5-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="65fb5-128">Ключевые слова **классдефсонли** и **ресулткласс** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="65fb5-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="65fb5-129">Их использование вместе приводит к ошибке недопустимого запроса.</span><span class="sxs-lookup"><span data-stu-id="65fb5-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="65fb5-130">Ключевое слово **рекуиредассоккуалифиер** указывает, что возвращенные конечные точки должны быть связаны с исходным объектом через класс ассоциации, включающий указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="65fb5-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="65fb5-131">Этот тип фильтрации используется для исключения широкого спектра конечных точек, если конечные точки не связаны с целевым объектом через определенный набор классов связей с тегами.</span><span class="sxs-lookup"><span data-stu-id="65fb5-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="65fb5-132">Например, запрос в следующем списке возвращает экземпляры конечной точки, если класс ассоциации содержит квалификатор с именем **Association**.</span><span class="sxs-lookup"><span data-stu-id="65fb5-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="65fb5-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="65fb5-135">Ключевое слово **рекуиредкуалифиер** указывает, что возвращаемые конечные точки, связанные с исходным объектом, должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="65fb5-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="65fb5-136">Ключевое слово **рекуиредкуалифиер** можно использовать для включения определенных типов экземпляров в результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="65fb5-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="65fb5-137">Например, запрос в следующем списке возвращает экземпляры конечных точек, которые включают квалификатор с именем [**locale**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="65fb5-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="65fb5-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="65fb5-140">Ключевое слово **ресулткласс** указывает, что возвращаемые конечные точки, связанные с исходным объектом, должны принадлежать к указанному классу или быть производным от него.</span><span class="sxs-lookup"><span data-stu-id="65fb5-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="65fb5-141">Например, запрос в следующем списке возвращает экземпляры конечной точки, которые являются производными от класса [**\_ каталога CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :</span><span class="sxs-lookup"><span data-stu-id="65fb5-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="65fb5-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="65fb5-144">Ключевые слова **классдефсонли** и **ресулткласс** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="65fb5-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="65fb5-145">Их использование вместе приводит к ошибке недопустимого запроса.</span><span class="sxs-lookup"><span data-stu-id="65fb5-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="65fb5-146">Ключевое слово **ресултроле** указывает, что возвращаемые конечные точки должны играть определенную роль в их связи с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="65fb5-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="65fb5-147">Роль определяется указанным свойством, ссылочным свойством типа [ref](references.md). Например, ключевое слово **ресултроле** можно использовать для получения всех конечных точек, имеющих свойство **GroupComponent** в связи с исходным объектом, как показано в следующем запросе.</span><span class="sxs-lookup"><span data-stu-id="65fb5-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="65fb5-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="65fb5-150">Ключевое слово **Role** указывает, что возвращенные конечные точки участвуют в связи с исходным объектом, в котором исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="65fb5-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="65fb5-151">Роль определяется указанным свойством, ссылочным свойством типа **ref**. Например, ключевое слово **Role** можно использовать для получения всех конечных точек, связанных с исходным объектом, имеющим свойство **GroupComponent** , как показано в следующем запросе.</span><span class="sxs-lookup"><span data-stu-id="65fb5-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="65fb5-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор</span><span class="sxs-lookup"><span data-stu-id="65fb5-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="65fb5-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты</span><span class="sxs-lookup"><span data-stu-id="65fb5-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="65fb5-154">Сложные запросы не могут использовать "and" или "or" для разделения ключевых слов для СОЕДИНИТЕЛей и [ссылок на](references-of-statement.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="65fb5-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="65fb5-155">Более того, знак равенства является единственным допустимым оператором, который может использоваться в таких запросах.</span><span class="sxs-lookup"><span data-stu-id="65fb5-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="65fb5-156">Например, допустим следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="65fb5-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="65fb5-157">Следующие примеры недопустимы.</span><span class="sxs-lookup"><span data-stu-id="65fb5-157">The next examples are not valid.</span></span> <span data-ttu-id="65fb5-158">В первом примере не используется знак равенства, а во втором примере по ошибке предпринимается попытка использовать ключевое слово **и** .</span><span class="sxs-lookup"><span data-stu-id="65fb5-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
