---
description: Запросы данных схемы используют инструкцию SELECT со следующим синтаксисом для запросов данных.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Инструкция SELECT для запросов схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd08cffa3fccc9a8cc2bf50452dcefcc1b7bfc0a62e512069b2db098bc6d13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315678"
---
# <a name="select-statement-for-schema-queries"></a>Инструкция SELECT для запросов схемы

Запросы данных схемы используют инструкцию SELECT со следующим синтаксисом для [запросов данных](select-statement-for-data-queries.md). Разница заключается в использовании специального класса с именем «meta \_ Class», который определяет запрос как запрос схемы.

В следующем примере запрашиваются все определения классов, которые находятся в текущем пространстве имен.


```sql
SELECT * FROM meta_class
```



Запросы схемы поддерживают только " \* ". Чтобы ограничить область возвращаемых определений, поставщик может добавить предложение WHERE, указывающее конкретный класс.

В следующем примере показано, как добавить предложение WHERE, чтобы указать определенный класс.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



Специальное свойство **, именуемое \_ \_** , определяет целевой класс для запроса схемы. Обратите внимание, что оператор ISA должен использоваться с **\_ \_ этим** свойством для запроса определений для подклассов целевого класса. Предыдущий запрос возвращает определение для класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) и определений для всех его подклассов.

В следующем примере показано, как запросить определение класса для одного класса с помощью системного свойства **\_ \_ класса** .


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Этот запрос эквивалентен вызову [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или методу [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) с параметром пути к объекту, установленным в значение "Win32 \_ LogicalDisk".

Следующий пример кода VBScript извлекает все дочерние классы класса WMI верхнего уровня. \_ \_ Системное свойство WMI династию содержит имя класса верхнего уровня, производным от которого является класс, который можно использовать для получения всех классов в пространстве имен, производном от класса верхнего уровня, включая этот класс.


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



Следующий сценарий VBScript получает непосредственные дочерние классы для класса WMI.


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



Следующий сценарий VBScript Извлекает классы верхнего уровня. Для всех классов верхнего уровня в пространстве имен WMI \_ \_ системное свойство суперкласса имеет значение null. Таким образом, можно получить классы верхнего уровня, выполнив поиск пустого суперкласса.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
