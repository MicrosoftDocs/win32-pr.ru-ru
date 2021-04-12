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
# <a name="associators-of-statement"></a>СОЕДИНИТЕЛи оператора

СОЕДИНИТЕЛи оператора получают все экземпляры, связанные с определенным исходным экземпляром. Получаемые экземпляры называются конечными точками. Каждая конечная точка возвращается столько раз, сколько существует связей между ней и исходным объектом. Например, предположим, что существуют экземпляры A, B, X и Y. Существуют два экземпляра ассоциаций, один из которых связывает A и X и другой, связывающий B и Y. Следующий запрос возвращает одну конечную точку X:


```sql
ASSOCIATORS OF {A}
```



Однако если существует другая ассоциация, связывающая A и X, то приведенный выше запрос возвращает две конечные точки X.

Базовый синтаксис для СОЕДИНИТЕЛей оператора:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Обратите внимание, что фигурные скобки являются частью синтаксиса. Для Обжектпас можно использовать любой допустимый путь к объекту. Токены в пути к объекту не могут содержать пробелы. Например, запрос в следующем списке возвращает экземпляры, связанные с указанным логическим диском:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Как и в случае с [инструкцией SELECT](select-statement-for-data-queries.md), соединители оператора могут включать [предложение WHERE](where-clause.md), но предложение WHERE для соединителей оператора очень отличается от предложения SELECT статементвхере.

[Предложение WHERE](where-clause.md) для соединителей оператора может включать одно или несколько из следующих стандартных ключевых слов и их значений:


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



Обратите внимание, что необязательные вложенные предложения не разделяются запятыми.

Ключевое слово **ассоккласс** указывает, что возвращенные конечные точки должны быть связаны с источником через указанный класс или один из его производных классов. Например, запрос в следующем списке возвращает только конечные точки, связанные с источником с помощью класса ассоциации [**Win32 \_ системдевицес**](/windows/desktop/CIMWin32Prov/win32-systemdevices) или любого из его производных классов:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Ключевое слово **классдефсонли** указывает, что предложение возвращает результирующий набор объектов определения класса, а не фактических экземпляров классов. Эти объекты являются определениями классов, к которым принадлежат экземпляры конечных точек. Например, запрос, приведенный в следующем списке, возвращает определения для [**\_ каталога Win32**](/windows/desktop/CIMWin32Prov/win32-directory) и [**классов \_ Win32 ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Ключевые слова **классдефсонли** и **ресулткласс** являются взаимоисключающими. Их использование вместе приводит к ошибке недопустимого запроса.

Ключевое слово **рекуиредассоккуалифиер** указывает, что возвращенные конечные точки должны быть связаны с исходным объектом через класс ассоциации, включающий указанный квалификатор. Этот тип фильтрации используется для исключения широкого спектра конечных точек, если конечные точки не связаны с целевым объектом через определенный набор классов связей с тегами. Например, запрос в следующем списке возвращает экземпляры конечной точки, если класс ассоциации содержит квалификатор с именем **Association**.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Ключевое слово **рекуиредкуалифиер** указывает, что возвращаемые конечные точки, связанные с исходным объектом, должны включать указанный квалификатор. Ключевое слово **рекуиредкуалифиер** можно использовать для включения определенных типов экземпляров в результирующий набор. Например, запрос в следующем списке возвращает экземпляры конечных точек, которые включают квалификатор с именем [**locale**](swbemobjectpath-locale.md).

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Ключевое слово **ресулткласс** указывает, что возвращаемые конечные точки, связанные с исходным объектом, должны принадлежать к указанному классу или быть производным от него. Например, запрос в следующем списке возвращает экземпляры конечной точки, которые являются производными от класса [**\_ каталога CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Ключевые слова **классдефсонли** и **ресулткласс** являются взаимоисключающими. Их использование вместе приводит к ошибке недопустимого запроса.

Ключевое слово **ресултроле** указывает, что возвращаемые конечные точки должны играть определенную роль в их связи с исходным объектом. Роль определяется указанным свойством, ссылочным свойством типа [ref](references.md). Например, ключевое слово **ресултроле** можно использовать для получения всех конечных точек, имеющих свойство **GroupComponent** в связи с исходным объектом, как показано в следующем запросе.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

Ключевое слово **Role** указывает, что возвращенные конечные точки участвуют в связи с исходным объектом, в котором исходный объект играет определенную роль. Роль определяется указанным свойством, ссылочным свойством типа **ref**. Например, ключевое слово **Role** можно использовать для получения всех конечных точек, связанных с исходным объектом, имеющим свойство **GroupComponent** , как показано в следующем запросе.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Выбор
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Результаты
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Сложные запросы не могут использовать "and" или "or" для разделения ключевых слов для СОЕДИНИТЕЛей и [ссылок на](references-of-statement.md) инструкции. Более того, знак равенства является единственным допустимым оператором, который может использоваться в таких запросах. Например, допустим следующий запрос:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Следующие примеры недопустимы. В первом примере не используется знак равенства, а во втором примере по ошибке предпринимается попытка использовать ключевое слово **и** .

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
