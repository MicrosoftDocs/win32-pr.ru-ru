---
description: Используйте методы и свойства объекта Свбемобжектпас для создания и проверки пути к объекту. Этот объект может быть создан вызовом метода CreateObject VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Объект Свбемобжектпас (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701951"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="41adc-104">Объект Свбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="41adc-104">SWbemObjectPath object</span></span>

<span data-ttu-id="41adc-105">Используйте методы и свойства объекта **свбемобжектпас** для создания и проверки пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="41adc-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="41adc-106">Этот объект может быть создан вызовом метода **CreateObject** VBScript.</span><span class="sxs-lookup"><span data-stu-id="41adc-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="41adc-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="41adc-107">Members</span></span>

<span data-ttu-id="41adc-108">Объект **свбемобжектпас** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="41adc-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="41adc-109">Методы</span><span class="sxs-lookup"><span data-stu-id="41adc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="41adc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="41adc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41adc-111">Методы</span><span class="sxs-lookup"><span data-stu-id="41adc-111">Methods</span></span>

<span data-ttu-id="41adc-112">Объект **свбемобжектпас** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="41adc-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="41adc-113">Метод</span><span class="sxs-lookup"><span data-stu-id="41adc-113">Method</span></span>                                                   | <span data-ttu-id="41adc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="41adc-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="41adc-115">**сетаскласс**</span><span class="sxs-lookup"><span data-stu-id="41adc-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="41adc-116">Заставляет путь обращаться к классу WMI.</span><span class="sxs-lookup"><span data-stu-id="41adc-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="41adc-117">**сетассинглетон**</span><span class="sxs-lookup"><span data-stu-id="41adc-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="41adc-118">Заставляет путь обращаться к экземпляру WMI Singleton.</span><span class="sxs-lookup"><span data-stu-id="41adc-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41adc-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="41adc-119">Properties</span></span>

<span data-ttu-id="41adc-120">Объект **свбемобжектпас** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="41adc-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="41adc-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="41adc-121">Property</span></span>                                                              | <span data-ttu-id="41adc-122">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="41adc-122">Access type</span></span>           | <span data-ttu-id="41adc-123">Описание</span><span class="sxs-lookup"><span data-stu-id="41adc-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41adc-124">**Authority**</span><span class="sxs-lookup"><span data-stu-id="41adc-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="41adc-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-125">Read/write</span></span><br/> | <span data-ttu-id="41adc-126">Строка, определяющая компонент центра пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="41adc-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="41adc-127">**Класс**</span><span class="sxs-lookup"><span data-stu-id="41adc-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="41adc-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-128">Read/write</span></span><br/> | <span data-ttu-id="41adc-129">Имя класса, который является частью пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="41adc-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="41adc-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="41adc-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="41adc-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-131">Read/write</span></span><br/> | <span data-ttu-id="41adc-132">Строка, содержащая путь в форме, которую можно использовать в качестве отображаемого имени моникера.</span><span class="sxs-lookup"><span data-stu-id="41adc-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="41adc-133">См. раздел [Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="41adc-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="41adc-134">**Класс класса**</span><span class="sxs-lookup"><span data-stu-id="41adc-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="41adc-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="41adc-135">Read-only</span></span><br/>  | <span data-ttu-id="41adc-136">Логическое значение, указывающее, представляет ли этот путь класс.</span><span class="sxs-lookup"><span data-stu-id="41adc-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="41adc-137">Это аналогично свойству [ \_ \_ женус](wmi-system-properties.md) в COM API.</span><span class="sxs-lookup"><span data-stu-id="41adc-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="41adc-138">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="41adc-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="41adc-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="41adc-139">Read-only</span></span><br/>  | <span data-ttu-id="41adc-140">Логическое значение, указывающее, представляет ли этот путь одноэлементный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="41adc-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="41adc-141">**Ключи**</span><span class="sxs-lookup"><span data-stu-id="41adc-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="41adc-142">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="41adc-142">Read-only</span></span><br/>  | <span data-ttu-id="41adc-143">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , содержащий привязки значений ключа.</span><span class="sxs-lookup"><span data-stu-id="41adc-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="41adc-144">**Языкового стандарта**</span><span class="sxs-lookup"><span data-stu-id="41adc-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="41adc-145">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-145">Read/write</span></span><br/> | <span data-ttu-id="41adc-146">Строка, содержащая языковой стандарт для этого пути объекта.</span><span class="sxs-lookup"><span data-stu-id="41adc-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="41adc-147">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="41adc-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="41adc-148">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-148">Read/write</span></span><br/> | <span data-ttu-id="41adc-149">Имя пространства имен, которое является частью пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="41adc-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="41adc-150">Это то же самое, что и свойство [ \_ \_ Namespace](wmi-system-properties.md) в COM API.</span><span class="sxs-lookup"><span data-stu-id="41adc-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="41adc-151">**парентнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="41adc-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="41adc-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="41adc-152">Read-only</span></span><br/>  | <span data-ttu-id="41adc-153">Имя родителя пространства имен, которое является частью пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="41adc-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="41adc-154">**Путь**</span><span class="sxs-lookup"><span data-stu-id="41adc-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="41adc-155">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-155">Read/write</span></span><br/> | <span data-ttu-id="41adc-156">Содержит абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="41adc-156">Contains the absolute path.</span></span> <span data-ttu-id="41adc-157">Это то же самое, что и системное свойство [ \_ \_ path](wmi-system-properties.md) в COM API.</span><span class="sxs-lookup"><span data-stu-id="41adc-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="41adc-158">Это свойство данного объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41adc-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="41adc-159">**релпас**</span><span class="sxs-lookup"><span data-stu-id="41adc-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="41adc-160">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-160">Read/write</span></span><br/> | <span data-ttu-id="41adc-161">Содержит относительный путь.</span><span class="sxs-lookup"><span data-stu-id="41adc-161">Contains the relative path.</span></span> <span data-ttu-id="41adc-162">Это то же самое, что и системное свойство [ \_ \_ релпас](wmi-system-properties.md) в COM API.</span><span class="sxs-lookup"><span data-stu-id="41adc-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="41adc-163">**Безопасность\_**</span><span class="sxs-lookup"><span data-stu-id="41adc-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="41adc-164">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="41adc-164">Read-only</span></span><br/>  | <span data-ttu-id="41adc-165">Используется для чтения или изменения параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="41adc-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="41adc-166">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="41adc-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="41adc-167">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41adc-167">Read/write</span></span><br/> | <span data-ttu-id="41adc-168">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="41adc-168">Name of the server.</span></span> <span data-ttu-id="41adc-169">Это то же самое, что и свойство System [ \_ \_ Server](wmi-system-properties.md) в интерфейсе API COM.</span><span class="sxs-lookup"><span data-stu-id="41adc-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="41adc-170">Примеры</span><span class="sxs-lookup"><span data-stu-id="41adc-170">Examples</span></span>

<span data-ttu-id="41adc-171">В следующем примере кода VBScript показано, как создавать пути к объектам.</span><span class="sxs-lookup"><span data-stu-id="41adc-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="41adc-172">В следующем образце кода Perl показано, как создавать пути к объектам.</span><span class="sxs-lookup"><span data-stu-id="41adc-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="41adc-173">Требования</span><span class="sxs-lookup"><span data-stu-id="41adc-173">Requirements</span></span>



| <span data-ttu-id="41adc-174">Требование</span><span class="sxs-lookup"><span data-stu-id="41adc-174">Requirement</span></span> | <span data-ttu-id="41adc-175">Значение</span><span class="sxs-lookup"><span data-stu-id="41adc-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41adc-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41adc-176">Minimum supported client</span></span><br/> | <span data-ttu-id="41adc-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41adc-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41adc-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41adc-178">Minimum supported server</span></span><br/> | <span data-ttu-id="41adc-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41adc-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41adc-180">Header</span><span class="sxs-lookup"><span data-stu-id="41adc-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="41adc-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41adc-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="41adc-182">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="41adc-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="41adc-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41adc-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41adc-184">DLL</span><span class="sxs-lookup"><span data-stu-id="41adc-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41adc-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41adc-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="41adc-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="41adc-186">CLSID</span></span><br/>                    | <span data-ttu-id="41adc-187">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="41adc-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="41adc-188">IID</span><span class="sxs-lookup"><span data-stu-id="41adc-188">IID</span></span><br/>                      | <span data-ttu-id="41adc-189">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="41adc-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="41adc-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41adc-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41adc-191">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="41adc-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




