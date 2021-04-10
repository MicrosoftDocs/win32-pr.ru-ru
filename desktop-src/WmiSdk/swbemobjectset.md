---
description: Объект SWbemObjectSet — это коллекция объектов SWbemObject. Дополнительные сведения см. в разделе доступ к коллекции. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Объект SWbemObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272558"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="b9145-105">Объект SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9145-105">SWbemObjectSet object</span></span>

<span data-ttu-id="b9145-106">Объект **SWbemObjectSet** — это коллекция объектов [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="b9145-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="b9145-107">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="b9145-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="b9145-108">Не удается создать этот объект с **помощью вызова функции** VBScript.</span><span class="sxs-lookup"><span data-stu-id="b9145-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="b9145-109">Объект **SWbemObjectSet** можно получить, вызвав любой из следующих методов или их асинхронных эквивалентов:</span><span class="sxs-lookup"><span data-stu-id="b9145-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="b9145-110">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="b9145-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="b9145-111">**SWbemObject. Instances\_**</span><span class="sxs-lookup"><span data-stu-id="b9145-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="b9145-112">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="b9145-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="b9145-113">**SWbemObject. подклассы\_**</span><span class="sxs-lookup"><span data-stu-id="b9145-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="b9145-114">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="b9145-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="b9145-115">**SWbemServices.ExeКкуери**</span><span class="sxs-lookup"><span data-stu-id="b9145-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="b9145-116">**SWbemServices. Инстанцесоф**</span><span class="sxs-lookup"><span data-stu-id="b9145-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="b9145-117">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="b9145-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="b9145-118">**SWbemServices. Субклассесоф**</span><span class="sxs-lookup"><span data-stu-id="b9145-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="b9145-119">Объект **SWbemObjectSet** не поддерживает необязательные методы **добавления** и **удаления** коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9145-120">Поскольку обратный вызов к приемнику может быть не возвращен на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="b9145-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="b9145-121">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b9145-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="b9145-122">Элементы</span><span class="sxs-lookup"><span data-stu-id="b9145-122">Members</span></span>

<span data-ttu-id="b9145-123">Объект **SWbemObjectSet** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b9145-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="b9145-124">Методы</span><span class="sxs-lookup"><span data-stu-id="b9145-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9145-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9145-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9145-126">Методы</span><span class="sxs-lookup"><span data-stu-id="b9145-126">Methods</span></span>

<span data-ttu-id="b9145-127">Объект **SWbemObjectSet** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="b9145-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="b9145-128">Метод</span><span class="sxs-lookup"><span data-stu-id="b9145-128">Method</span></span>                              | <span data-ttu-id="b9145-129">Описание</span><span class="sxs-lookup"><span data-stu-id="b9145-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9145-130">**Item**</span><span class="sxs-lookup"><span data-stu-id="b9145-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="b9145-131">Извлекает объект [**SWbemObject**](swbemobject.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="b9145-132">Это метод объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9145-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b9145-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9145-133">Properties</span></span>

<span data-ttu-id="b9145-134">Объект **SWbemObjectSet** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b9145-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="b9145-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="b9145-135">Property</span></span>                                                  | <span data-ttu-id="b9145-136">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b9145-136">Access type</span></span>          | <span data-ttu-id="b9145-137">Описание</span><span class="sxs-lookup"><span data-stu-id="b9145-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="b9145-138">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="b9145-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="b9145-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9145-139">Read-only</span></span><br/> | <span data-ttu-id="b9145-140">Количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="b9145-141">**Безопасность\_**</span><span class="sxs-lookup"><span data-stu-id="b9145-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="b9145-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9145-142">Read-only</span></span><br/> | <span data-ttu-id="b9145-143">Используется для чтения или изменения параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="b9145-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9145-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9145-144">Remarks</span></span>

<span data-ttu-id="b9145-145">**SWbemObjectSet** — это коллекция из нуля или более объектов [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="b9145-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="b9145-146">Каждый **SWbemObject** в **SWbemObjectSet** может представлять одно из двух вещей:</span><span class="sxs-lookup"><span data-stu-id="b9145-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="b9145-147">Экземпляр управляемого WMI ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9145-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="b9145-148">Экземпляр определения класса.</span><span class="sxs-lookup"><span data-stu-id="b9145-148">An instance of a class definition.</span></span>

<span data-ttu-id="b9145-149">Чаще всего этот класс используется в WMI как возвращаемое значение для вызова [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) или [**инстанцесоф**](swbemservices-instancesof.md) , как описано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="b9145-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="b9145-150">В большинстве случаев единственное, что вы будете делать с **SWbemObjectSet** , — перечисляет все объекты, содержащиеся в самой коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="b9145-151">Однако **SWbemObjectSet** включает число свойств, которое может быть полезно при создании сценариев системного администрирования.</span><span class="sxs-lookup"><span data-stu-id="b9145-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="b9145-152">Как следует из названия, Count сообщает число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="b9145-153">Например, этот скрипт извлекает коллекцию всех служб, установленных на компьютере, а затем отображает общее число найденных служб:</span><span class="sxs-lookup"><span data-stu-id="b9145-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="b9145-154">Дополнительные сведения об использовании этого класса см. в разделе [перечисление WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b9145-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9145-155">Примеры</span><span class="sxs-lookup"><span data-stu-id="b9145-155">Examples</span></span>

<span data-ttu-id="b9145-156">В следующем примере кода VBScript показано, как обрабатываются **SWbemObjectSet** коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="b9145-157">В следующем образце кода Perl показано, как обрабатываются **SWbemObjectSet** коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9145-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="b9145-158">Требования</span><span class="sxs-lookup"><span data-stu-id="b9145-158">Requirements</span></span>



| <span data-ttu-id="b9145-159">Требование</span><span class="sxs-lookup"><span data-stu-id="b9145-159">Requirement</span></span> | <span data-ttu-id="b9145-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b9145-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9145-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9145-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b9145-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9145-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9145-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9145-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b9145-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9145-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9145-165">Header</span><span class="sxs-lookup"><span data-stu-id="b9145-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9145-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9145-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9145-167">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b9145-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9145-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b9145-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b9145-169">DLL</span><span class="sxs-lookup"><span data-stu-id="b9145-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9145-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9145-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9145-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="b9145-171">CLSID</span></span><br/>                    | <span data-ttu-id="b9145-172">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="b9145-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="b9145-173">IID</span><span class="sxs-lookup"><span data-stu-id="b9145-173">IID</span></span><br/>                      | <span data-ttu-id="b9145-174">IID \_ исвбемобжектсет</span><span class="sxs-lookup"><span data-stu-id="b9145-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="b9145-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9145-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9145-176">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="b9145-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




