---
description: Используйте свойство Count объекта SWbemObjectSet, чтобы определить, сколько элементов находится в коллекции SWbemObjectSet. Это свойство доступно только для чтения.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Свойство SWbemObjectSet. Count (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703171"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="0d321-104">SWbemObjectSet. Count, свойство</span><span class="sxs-lookup"><span data-stu-id="0d321-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="0d321-105">Используйте свойство **Count** объекта [**SWbemObjectSet**](swbemobjectset.md) , чтобы определить, сколько элементов находится в коллекции **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="0d321-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="0d321-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0d321-106">This property is read-only.</span></span>

<span data-ttu-id="0d321-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0d321-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0d321-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0d321-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d321-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d321-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="0d321-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0d321-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0d321-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d321-111">Remarks</span></span>

<span data-ttu-id="0d321-112">При использовании параметра count необходимо соблюдать осторожность, так как инструментарий WMI не сохраняет непрерывное количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0d321-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="0d321-113">Если вы запрашиваете счетчик для коллекции, Инструментарий WMI не может мгновенно ответить на число. Вместо этого он должен буквально подсчитать элементы, перечисляя всю коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0d321-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="0d321-114">Для коллекции, которая содержит относительно несколько элементов, таких как службы, это перечисление, скорее всего, занимает меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="0d321-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="0d321-115">Однако подсчет количества событий в коллекции журналов событий может занять значительно больше времени.</span><span class="sxs-lookup"><span data-stu-id="0d321-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="0d321-116">А затем Предположим, что необходимо отобразить значения свойств для каждого события в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0d321-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="0d321-117">В этом случае Инструментарий WMI должен перечислять всю коллекцию во второй раз.</span><span class="sxs-lookup"><span data-stu-id="0d321-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="0d321-118">При попытке получить это свойство из объекта [**SWbemObjectSet**](swbemobjectset.md) , возвращаемого методом, в котором указанные флаги включены в флаг вбемфлагфорвардонли, возникнет ошибка вбемеррфаилед.</span><span class="sxs-lookup"><span data-stu-id="0d321-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0d321-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="0d321-119">Examples</span></span>

<span data-ttu-id="0d321-120">В большинстве случаев единственное, что вы будете делать с SWbemObjectSet, — перечисляет все объекты, содержащиеся в самой коллекции.</span><span class="sxs-lookup"><span data-stu-id="0d321-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="0d321-121">Однако счетчик количества, который может быть полезен при создании сценариев системного администрирования.</span><span class="sxs-lookup"><span data-stu-id="0d321-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="0d321-122">Как следует из названия, Count сообщает число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0d321-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="0d321-123">Например, этот скрипт извлекает коллекцию всех служб, установленных на компьютере, а затем отображает общее число найденных служб:</span><span class="sxs-lookup"><span data-stu-id="0d321-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="0d321-124">То, что делает число полезным, заключается в том, что он может сообщить вам, доступен ли конкретный экземпляр на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0d321-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="0d321-125">Например, этот скрипт получает коллекцию всех служб на компьютере с именем W3SVC.</span><span class="sxs-lookup"><span data-stu-id="0d321-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="0d321-126">Если значение счетчика равно 0 (и оно допустимо для коллекций, не имеющих экземпляров), это означает, что на компьютере не установлена служба W3SVC.</span><span class="sxs-lookup"><span data-stu-id="0d321-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="0d321-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0d321-127">Requirements</span></span>



| <span data-ttu-id="0d321-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0d321-128">Requirement</span></span> | <span data-ttu-id="0d321-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0d321-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d321-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d321-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d321-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d321-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d321-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d321-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d321-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d321-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d321-134">Header</span><span class="sxs-lookup"><span data-stu-id="0d321-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d321-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d321-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d321-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0d321-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d321-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d321-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d321-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0d321-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d321-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d321-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d321-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d321-140">CLSID</span></span><br/>                    | <span data-ttu-id="0d321-141">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="0d321-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="0d321-142">IID</span><span class="sxs-lookup"><span data-stu-id="0d321-142">IID</span></span><br/>                      | <span data-ttu-id="0d321-143">IID \_ исвбемобжектсет</span><span class="sxs-lookup"><span data-stu-id="0d321-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




