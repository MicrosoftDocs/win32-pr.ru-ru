---
description: Объект Свбемрефрешер — это объект контейнера, который может обновлять данные для всех добавленных в него объектов. Набор добавленных объектов, каждый элемент, представленный экземпляром Свбемрефрешаблеитем, может рассматриваться как коллекция и перечисляться.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Объект Свбемрефрешер (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999937"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="7c0ea-104">Объект Свбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="7c0ea-104">SWbemRefresher object</span></span>

<span data-ttu-id="7c0ea-105">Объект **свбемрефрешер** — это объект контейнера, который может обновлять данные для всех добавленных в него объектов.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="7c0ea-106">Отдельные экземпляры и перечислители экземпляров можно добавлять в контейнер или удалять из него.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="7c0ea-107">Набор добавленных объектов, каждый элемент которого представлен экземпляром [**свбемрефрешаблеитем**](swbemrefreshableitem.md) , можно рассматривать как коллекцию и перечислить.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="7c0ea-108">Экземпляры WMI из любого класса можно добавить в объект **свбемрефрешер** .</span><span class="sxs-lookup"><span data-stu-id="7c0ea-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="7c0ea-109">Даже если поставщик данных экземпляра не является поставщиком высокой производительности, объект обновления по-прежнему может обновить данные в вызове [**обновления**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="7c0ea-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="7c0ea-110">Если данные передаются через высокопроизводительный поставщик, а свойство [**аутореконнект**](swbemrefresher-autoreconnect.md) имеет **значение true**, объект **свбемрефрешер** пытается восстановить разорванное соединение с поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="7c0ea-111">Этот объект может быть создан вызовом метода **CreateObject** VBScript.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="7c0ea-112">Операция обновления может быть выполнена путем вызова метода [**свбемрефрешер. Refresh**](swbemrefresher-refresh.md) или метода [**\_ свбемобжектекс. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="7c0ea-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="7c0ea-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="7c0ea-113">Members</span></span>

<span data-ttu-id="7c0ea-114">Объект **свбемрефрешер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7c0ea-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="7c0ea-115">Методы</span><span class="sxs-lookup"><span data-stu-id="7c0ea-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c0ea-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c0ea-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c0ea-117">Методы</span><span class="sxs-lookup"><span data-stu-id="7c0ea-117">Methods</span></span>

<span data-ttu-id="7c0ea-118">Объект **свбемрефрешер** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="7c0ea-119">Метод</span><span class="sxs-lookup"><span data-stu-id="7c0ea-119">Method</span></span>                                        | <span data-ttu-id="7c0ea-120">Описание</span><span class="sxs-lookup"><span data-stu-id="7c0ea-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c0ea-121">**Включить**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="7c0ea-122">Добавляет новый обновляемый объект в коллекцию в объекте обновления.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="7c0ea-123">**адденум**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="7c0ea-124">Добавляет новый перечислитель в объект обновления.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="7c0ea-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="7c0ea-126">Удаляет все элементы из коллекции в объекте обновления.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="7c0ea-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="7c0ea-128">Возвращает указанный элемент обновления из коллекции.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="7c0ea-129">**Обновить**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="7c0ea-130">Обновляет все элементы, содержащиеся в объекте обновления.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="7c0ea-131">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="7c0ea-132">Удаляет из Обновитель объект элемента обновления или набор объектов с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7c0ea-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c0ea-133">Properties</span></span>

<span data-ttu-id="7c0ea-134">Объект **свбемрефрешер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="7c0ea-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="7c0ea-135">Property</span></span>                                                         | <span data-ttu-id="7c0ea-136">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7c0ea-136">Access type</span></span>          | <span data-ttu-id="7c0ea-137">Описание</span><span class="sxs-lookup"><span data-stu-id="7c0ea-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c0ea-138">**аутореконнект**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="7c0ea-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c0ea-139">Read-only</span></span><br/> | <span data-ttu-id="7c0ea-140">Указывает, будет ли Обновитель автоматически повторно подключаться к удаленному поставщику, если соединение разорвано.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="7c0ea-141">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="7c0ea-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c0ea-142">Read-only</span></span><br/> | <span data-ttu-id="7c0ea-143">Содержит число элементов в объекте обновления.</span><span class="sxs-lookup"><span data-stu-id="7c0ea-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="7c0ea-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="7c0ea-144">Examples</span></span>

<span data-ttu-id="7c0ea-145">В следующем примере показано создание объекта **свбемрефрешер** с помощью методов [**Add**](swbemrefresher-add.md) и [**адденум**](swbemrefresher-addenum.md) для хранения одного экземпляра и экземпляра перечисления, обновления данных и использования свойства Item для получения объектов [**свбемрефрешаблеитем**](swbemrefreshableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7c0ea-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="7c0ea-146">Требования</span><span class="sxs-lookup"><span data-stu-id="7c0ea-146">Requirements</span></span>



| <span data-ttu-id="7c0ea-147">Требование</span><span class="sxs-lookup"><span data-stu-id="7c0ea-147">Requirement</span></span> | <span data-ttu-id="7c0ea-148">Значение</span><span class="sxs-lookup"><span data-stu-id="7c0ea-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0ea-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c0ea-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0ea-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c0ea-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c0ea-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c0ea-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0ea-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c0ea-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c0ea-153">Header</span><span class="sxs-lookup"><span data-stu-id="7c0ea-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c0ea-154"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ea-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c0ea-155">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7c0ea-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c0ea-156"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ea-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c0ea-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7c0ea-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c0ea-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c0ea-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c0ea-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="7c0ea-159">CLSID</span></span><br/>                    | <span data-ttu-id="7c0ea-160">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="7c0ea-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="7c0ea-161">IID</span><span class="sxs-lookup"><span data-stu-id="7c0ea-161">IID</span></span><br/>                      | <span data-ttu-id="7c0ea-162">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="7c0ea-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="7c0ea-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c0ea-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0ea-164">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="7c0ea-165">**свбемобжектекс**</span><span class="sxs-lookup"><span data-stu-id="7c0ea-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="7c0ea-166">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="7c0ea-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




