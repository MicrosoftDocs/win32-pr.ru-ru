---
description: Предоставляет функции доступа семисинчронаус и пример кода для выполнения вызова метода семисинчронаус.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Вызов Семисинчронаус с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693323"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="f5a89-103">Вызов Семисинчронаус с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="f5a89-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="f5a89-104">Некоторые методы WMI могут возвращать большие коллекции, что приводит к зависанию сценариев.</span><span class="sxs-lookup"><span data-stu-id="f5a89-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="f5a89-105">В скрипте по умолчанию используется семисинчронаус Access, а инструментарий управления Windows (WMI) (WMI) задает **вбемфлагретурниммедиатели** для вызовов, которые могут возвращать коллекции больших объектов, такие как следующие методы [**SwbemServices**](swbemservices.md) : [**инстанцесоф**](swbemservices-instancesof.md), [**субклассесоф**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**ассоЦиаторсоф**](swbemservices-associatorsof.md)и [**ReferencesTo**](swbemservices-referencesto.md).</span><span class="sxs-lookup"><span data-stu-id="f5a89-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="f5a89-106">Семисинчронаус Access, использующий **вбемфлагретурниммедиатели** , заданный в параметре *ифлагс* , также является значением по умолчанию для вызовов, которые могут возвращать наборы больших объектов для следующих методов [**SWbemObject**](swbemobject.md) : [**\_ экземпляров**](swbemobject-instances-.md), [**подклассов \_**](swbemobject-subclasses-.md), [**соединителей \_**](swbemobject-associators-.md)и [**ссылок \_**](swbemobject-references-.md).</span><span class="sxs-lookup"><span data-stu-id="f5a89-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="f5a89-107">Чтобы уменьшить использование ресурсов памяти инструментария WMI при обработке большой коллекции объектов, включите значение **вбемфлагфорвардонли** в параметр *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="f5a89-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="f5a89-108">Использование **вбемфлагфорвардонли** заставляет Инструментарий WMI создать перечислитель только для перенаправления, который не допускает повторного поворота коллекции и доступа к элементам.</span><span class="sxs-lookup"><span data-stu-id="f5a89-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="f5a89-109">Инструментарий WMI исключает память для каждого объекта, так как оператор **for each** обрабатывает объект.</span><span class="sxs-lookup"><span data-stu-id="f5a89-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="f5a89-110">Нельзя вызвать метод **Count** для коллекции, если установлен флаг **вбемфлагфорвардонли** для вызова, который получил коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f5a89-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="f5a89-111">Обратите внимание, что параметр *ифлагс* имеет значение **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли** по умолчанию для метода [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="f5a89-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="f5a89-112">Следующая процедура описывает, как использовать VBScript для выполнения вызова семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="f5a89-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="f5a89-113">**Создание вызова семисинчронаус в VBScript**</span><span class="sxs-lookup"><span data-stu-id="f5a89-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="f5a89-114">Задайте для параметра *ифлагс* значение [вбемфлагретурниммедиатели](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="f5a89-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="f5a89-115">Сделайте нормальный синхронный вызов для [**SWbemServices.Exeккуери**](swbemservices-execquery.md) или [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) с помощью значения *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="f5a89-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="f5a89-116">Если требуется обрабатывать объекты, возвращаемые вызовом в виде коллекции, используйте синтаксис перечисления, такой как VBScript **для каждого из них**.</span><span class="sxs-lookup"><span data-stu-id="f5a89-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="f5a89-117">При возвращении каждого объекта он обрабатывается как следующий элемент в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f5a89-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="f5a89-118">Создайте однопроходный перечислитель, объединив значение **вбемфлагретурниммедиатели** со значением **вбемфлагфорвардонли**.</span><span class="sxs-lookup"><span data-stu-id="f5a89-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="f5a89-119">Десятичное значение этой операции или равно 48.</span><span class="sxs-lookup"><span data-stu-id="f5a89-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="f5a89-120">Эти константы определены в библиотеке типов wbemdisp. tlb для Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f5a89-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="f5a89-121">Большинство языков сценариев используют числовое значение или определяют константу.</span><span class="sxs-lookup"><span data-stu-id="f5a89-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="f5a89-122">Дополнительные сведения см. в разделе [вбемфлаженум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="f5a89-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="f5a89-123">В следующем примере кода показано, как выполнить вызов метода семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="f5a89-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="f5a89-124">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f5a89-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="f5a89-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f5a89-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5a89-126">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="f5a89-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



