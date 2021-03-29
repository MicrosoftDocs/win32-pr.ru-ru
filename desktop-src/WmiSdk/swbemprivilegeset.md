---
description: Объект Свбемпривилежесет — это коллекция объектов Свбемпривилеже в объекте Свбемсекурити, которая запрашивает определенные привилегии для объекта инструментарий управления Windows (WMI) (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Объект Свбемпривилежесет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344722"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="6fd24-103">Объект Свбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="6fd24-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="6fd24-104">Объект **свбемпривилежесет** — это коллекция объектов [**Свбемпривилеже**](swbemprivilege.md) в объекте [**свбемсекурити**](swbemsecurity.md) , которая запрашивает определенные привилегии для объекта инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6fd24-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="6fd24-105">Список привилегий см. в разделе [**константы прав доступа**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6fd24-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="6fd24-106">Элементы добавляются в коллекцию с помощью методов [**Add**](swbemprivilegeset-add.md) и [**аддасстринг**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd24-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="6fd24-107">Элементы извлекаются из коллекции с помощью метода [**Item**](swbemprivilegeset-item.md) и удаляются с помощью метода [**Remove**](swbemprivilegeset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd24-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="6fd24-108">Этот объект не может быть создан вызовом метода [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) для VBScript.</span><span class="sxs-lookup"><span data-stu-id="6fd24-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="6fd24-109">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6fd24-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="6fd24-110">Объект **свбемпривилежесет** — это набор запросов переопределения привилегий для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="6fd24-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="6fd24-111">При вызове API с помощью этого объекта предпринимается попытка выполнить запросы на переопределение привилегий.</span><span class="sxs-lookup"><span data-stu-id="6fd24-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="6fd24-112">Объект **свбемпривилежесет** не определяет привилегии, доступные текущему пользователю или процессу.</span><span class="sxs-lookup"><span data-stu-id="6fd24-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="6fd24-113">Другими словами, получение привилегий для любого объекта WMI не определяет параметры привилегий, которые выполняются при подключении к WMI, или привилегии, действующие при доставке объекта в приемник.</span><span class="sxs-lookup"><span data-stu-id="6fd24-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="6fd24-114">Элементы</span><span class="sxs-lookup"><span data-stu-id="6fd24-114">Members</span></span>

<span data-ttu-id="6fd24-115">Объект **свбемпривилежесет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6fd24-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="6fd24-116">Методы</span><span class="sxs-lookup"><span data-stu-id="6fd24-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="6fd24-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fd24-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6fd24-118">Методы</span><span class="sxs-lookup"><span data-stu-id="6fd24-118">Methods</span></span>

<span data-ttu-id="6fd24-119">Объект **свбемпривилежесет** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="6fd24-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="6fd24-120">Метод</span><span class="sxs-lookup"><span data-stu-id="6fd24-120">Method</span></span>                                               | <span data-ttu-id="6fd24-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6fd24-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fd24-122">**Включить**</span><span class="sxs-lookup"><span data-stu-id="6fd24-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="6fd24-123">Добавляет объект [**свбемпривилеже**](swbemprivilege.md) в коллекцию **свбемпривилежесет** с помощью константы [вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="6fd24-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="6fd24-124">**аддасстринг**</span><span class="sxs-lookup"><span data-stu-id="6fd24-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="6fd24-125">Добавляет объект [**свбемпривилеже**](swbemprivilege.md) в коллекцию **свбемпривилежесет** с помощью строки привилегий.</span><span class="sxs-lookup"><span data-stu-id="6fd24-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="6fd24-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="6fd24-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="6fd24-127">Удаляет все привилегии из коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd24-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6fd24-128">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6fd24-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="6fd24-129">Извлекает объект [**свбемпривилеже**](swbemprivilege.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd24-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="6fd24-130">Это метод по умолчанию для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="6fd24-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="6fd24-131">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="6fd24-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="6fd24-132">Удаляет объект [**свбемпривилеже**](swbemprivilege.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd24-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="6fd24-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fd24-133">Properties</span></span>

<span data-ttu-id="6fd24-134">Объект **свбемпривилежесет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6fd24-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="6fd24-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="6fd24-135">Property</span></span>                                            | <span data-ttu-id="6fd24-136">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="6fd24-136">Access type</span></span>          | <span data-ttu-id="6fd24-137">Описание</span><span class="sxs-lookup"><span data-stu-id="6fd24-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="6fd24-138">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="6fd24-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="6fd24-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="6fd24-139">Read-only</span></span><br/> | <span data-ttu-id="6fd24-140">Количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6fd24-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="6fd24-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="6fd24-141">Examples</span></span>

<span data-ttu-id="6fd24-142">Следующий пример кода VBScript получает объект Свбемпривилежес и добавляет все доступные привилегии в коллекцию по значению привилегии, как определено в [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="6fd24-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="6fd24-143">В следующем примере кода VBScript показано, как добавить привилегии с помощью объекта **свбемпривилежесет** .</span><span class="sxs-lookup"><span data-stu-id="6fd24-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="6fd24-144">В следующем примере кода Perl показано, как добавить привилегии с помощью объекта **свбемпривилежесет** .</span><span class="sxs-lookup"><span data-stu-id="6fd24-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="6fd24-145">Требования</span><span class="sxs-lookup"><span data-stu-id="6fd24-145">Requirements</span></span>



| <span data-ttu-id="6fd24-146">Требование</span><span class="sxs-lookup"><span data-stu-id="6fd24-146">Requirement</span></span> | <span data-ttu-id="6fd24-147">Значение</span><span class="sxs-lookup"><span data-stu-id="6fd24-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd24-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fd24-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd24-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fd24-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6fd24-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fd24-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd24-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fd24-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fd24-152">Header</span><span class="sxs-lookup"><span data-stu-id="6fd24-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fd24-153"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fd24-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fd24-154">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6fd24-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="6fd24-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6fd24-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6fd24-156">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd24-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd24-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd24-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fd24-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="6fd24-158">CLSID</span></span><br/>                    | <span data-ttu-id="6fd24-159">\_СВБЕМПРИВИЛЕЖЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="6fd24-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="6fd24-160">IID</span><span class="sxs-lookup"><span data-stu-id="6fd24-160">IID</span></span><br/>                      | <span data-ttu-id="6fd24-161">IID \_ исвбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="6fd24-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="6fd24-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fd24-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd24-163">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="6fd24-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="6fd24-164">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="6fd24-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="6fd24-165">вбемпривилежеенум</span><span class="sxs-lookup"><span data-stu-id="6fd24-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="6fd24-166">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="6fd24-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="6fd24-167">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="6fd24-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

