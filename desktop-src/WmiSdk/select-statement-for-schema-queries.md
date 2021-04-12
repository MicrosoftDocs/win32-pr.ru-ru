---
description: Запросы данных схемы используют инструкцию SELECT со следующим синтаксисом для запросов данных.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Инструкция SELECT для запросов схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272218"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="3757a-103">Инструкция SELECT для запросов схемы</span><span class="sxs-lookup"><span data-stu-id="3757a-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="3757a-104">Запросы данных схемы используют инструкцию SELECT со следующим синтаксисом для [запросов данных](select-statement-for-data-queries.md).</span><span class="sxs-lookup"><span data-stu-id="3757a-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="3757a-105">Разница заключается в использовании специального класса с именем «meta \_ Class», который определяет запрос как запрос схемы.</span><span class="sxs-lookup"><span data-stu-id="3757a-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="3757a-106">В следующем примере запрашиваются все определения классов, которые находятся в текущем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="3757a-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="3757a-107">Запросы схемы поддерживают только " \* ".</span><span class="sxs-lookup"><span data-stu-id="3757a-107">Schema queries only support "\*".</span></span> <span data-ttu-id="3757a-108">Чтобы ограничить область возвращаемых определений, поставщик может добавить предложение WHERE, указывающее конкретный класс.</span><span class="sxs-lookup"><span data-stu-id="3757a-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="3757a-109">В следующем примере показано, как добавить предложение WHERE, чтобы указать определенный класс.</span><span class="sxs-lookup"><span data-stu-id="3757a-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="3757a-110">Специальное свойство **, именуемое \_ \_** , определяет целевой класс для запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="3757a-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="3757a-111">Обратите внимание, что оператор ISA должен использоваться с **\_ \_ этим** свойством для запроса определений для подклассов целевого класса.</span><span class="sxs-lookup"><span data-stu-id="3757a-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="3757a-112">Предыдущий запрос возвращает определение для класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) и определений для всех его подклассов.</span><span class="sxs-lookup"><span data-stu-id="3757a-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="3757a-113">В следующем примере показано, как запросить определение класса для одного класса с помощью системного свойства **\_ \_ класса** .</span><span class="sxs-lookup"><span data-stu-id="3757a-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="3757a-114">Этот запрос эквивалентен вызову [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или методу [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) с параметром пути к объекту, установленным в значение "Win32 \_ LogicalDisk".</span><span class="sxs-lookup"><span data-stu-id="3757a-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="3757a-115">Следующий пример кода VBScript извлекает все дочерние классы класса WMI верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="3757a-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="3757a-116">\_ \_ Системное свойство WMI династию содержит имя класса верхнего уровня, производным от которого является класс, который можно использовать для получения всех классов в пространстве имен, производном от класса верхнего уровня, включая этот класс.</span><span class="sxs-lookup"><span data-stu-id="3757a-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


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



<span data-ttu-id="3757a-117">Следующий сценарий VBScript получает непосредственные дочерние классы для класса WMI.</span><span class="sxs-lookup"><span data-stu-id="3757a-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


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



<span data-ttu-id="3757a-118">Следующий сценарий VBScript Извлекает классы верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="3757a-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="3757a-119">Для всех классов верхнего уровня в пространстве имен WMI \_ \_ системное свойство суперкласса имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="3757a-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="3757a-120">Таким образом, можно получить классы верхнего уровня, выполнив поиск пустого суперкласса.</span><span class="sxs-lookup"><span data-stu-id="3757a-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
