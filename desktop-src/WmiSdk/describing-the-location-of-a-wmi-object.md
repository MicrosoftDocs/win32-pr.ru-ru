---
description: По сути, аналогично URL-адресу, путь к объекту WMI представляет собой строку, однозначно определяющую пространство имен на сервере, класс в пространстве имен или экземпляры класса.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Описание расположения объекта WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711738"
---
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="2404e-103">Описание расположения объекта WMI</span><span class="sxs-lookup"><span data-stu-id="2404e-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="2404e-104">По сути, аналогично URL-адресу, путь к объекту WMI представляет собой строку, однозначно определяющую пространство имен на сервере, класс в пространстве имен или экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="2404e-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="2404e-105">Путь к объекту является иерархическим и содержит несколько элементов, описывающих расположение рассматриваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="2404e-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="2404e-106">Как и пути к файлам, пути к объектам WMI можно описать в полном или указанном виде относительного пути.</span><span class="sxs-lookup"><span data-stu-id="2404e-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="2404e-107">Пространство имен WMI-объекта указано на справочной странице инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="2404e-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="2404e-108">Например, расположение большинства классов, поддерживаемых [поставщиками WMI CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) , находится в \\ корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="2404e-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="2404e-109">Следующий код PowerShell описывает вызов для получения объекта [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="2404e-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="2404e-110">Кроме того, конкретный экземпляр логического диска [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) может иметь следующий путь из свойства [**SWbemObject. Path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="2404e-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="2404e-111">В следующем примере показан относительный путь к этому экземпляру, как показано при отображении свойства [**релпас**](swbemobjectpath-relpath.md) объекта [**свбемобжектпас**](swbemobjectpath.md) , возвращенного вызовом [**SWbemObject. Path \_**](swbemobject-path-.md).</span><span class="sxs-lookup"><span data-stu-id="2404e-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="2404e-112">Обратите внимание, что **DeviceID** является ключевым свойством класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="2404e-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="2404e-113">C++</span><span class="sxs-lookup"><span data-stu-id="2404e-113">C++</span></span>

<span data-ttu-id="2404e-114">В следующей таблице перечислены типы путей к объектам и связанные с ними методы, требующие путей к объектам.</span><span class="sxs-lookup"><span data-stu-id="2404e-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2404e-115">Тип пути к объекту</span><span class="sxs-lookup"><span data-stu-id="2404e-115">Object path type</span></span></th>
<th><span data-ttu-id="2404e-116">Метод</span><span class="sxs-lookup"><span data-stu-id="2404e-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2404e-117"><a href="describing-a-wmi-namespace-object-path.md">Пространство имен</a></span><span class="sxs-lookup"><span data-stu-id="2404e-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="2404e-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2404e-119"><a href="describing-a-class-object-path.md">Класс</a></span><span class="sxs-lookup"><span data-stu-id="2404e-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="2404e-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="2404e-121">[<strong>IWbemServices:: ексекмесодасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-ексекмесодасинк)</span><span class="sxs-lookup"><span data-stu-id="2404e-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2404e-122"><a href="describing-a-class-object-path.md">Класс</a> или <a href="describing-an-instance-object-path.md">экземпляр</a></span><span class="sxs-lookup"><span data-stu-id="2404e-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="2404e-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="2404e-124">[<strong>IWbemServices:: жетобжектасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-жетобжектасинк)</span><span class="sxs-lookup"><span data-stu-id="2404e-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2404e-125"><a href="describing-an-instance-object-path.md">Экземпляр</a></span><span class="sxs-lookup"><span data-stu-id="2404e-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="2404e-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D Елетеинстанце</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="2404e-127">[<strong>IWbemServices::D елетеинстанцеасинк</strong>] (/Виндовс/десктоп/АПИ/вбемкли/НФ-вбемкли-ивбемсервицес-делетеинстанцеасинк)</span><span class="sxs-lookup"><span data-stu-id="2404e-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="2404e-128">Скрипт</span><span class="sxs-lookup"><span data-stu-id="2404e-128">Script</span></span>

<span data-ttu-id="2404e-129">Пути к объектам могут быть созданы несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="2404e-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="2404e-130">Получите свойство метода, который возвращает объект [**свбемобжектпас**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="2404e-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="2404e-131">Получите свойство [**SWbemObject. Path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="2404e-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="2404e-132">Создайте строковую переменную, содержащую путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="2404e-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="2404e-133">В следующей таблице перечислены объекты скрипта, для которых требуются пути к объектам.</span><span class="sxs-lookup"><span data-stu-id="2404e-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2404e-134">Объект скрипта</span><span class="sxs-lookup"><span data-stu-id="2404e-134">Scripting object</span></span></th>
<th><span data-ttu-id="2404e-135">Метод</span><span class="sxs-lookup"><span data-stu-id="2404e-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2404e-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="2404e-137"><a href="swbemservices-associatorsof.md"><strong>ассоЦиаторсоф</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="2404e-138">[<strong>АссоЦиаторсофасинк</strong>] (swbemservices-associatorsofasync.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="2404e-139">[<strong>Удалить</strong>] (swbemservices-delete.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="2404e-140">[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="2404e-141">[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="2404e-142">[<strong>Ексекмесодасинк</strong>] (swbemservices-execmethodasync.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="2404e-143">[<strong>Get</strong>] (swbemservices-get.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="2404e-144">[<strong>Async</strong>] (swbemservices-getasync.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="2404e-145">[<strong>Референцесто</strong>] (swbemservices-referencesto.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="2404e-146">[<strong>Референцестоасинк</strong>] (swbemservices-referencestoasync.md)</span><span class="sxs-lookup"><span data-stu-id="2404e-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2404e-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="2404e-148"><a href="swbemobjectset-item.md"><strong>Элемент</strong></a></span><span class="sxs-lookup"><span data-stu-id="2404e-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
