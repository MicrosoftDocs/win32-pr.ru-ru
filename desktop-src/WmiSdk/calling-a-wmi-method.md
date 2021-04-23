---
title: Вызов метода WMI
description: Основной целью инструментария WMI является предоставление доступа к классам и экземплярам, представляющим объекты в сети.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546098"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="bb3d9-103">Вызов метода WMI</span><span class="sxs-lookup"><span data-stu-id="bb3d9-103">How to call a WMI method</span></span>

<span data-ttu-id="bb3d9-104">Основной целью инструментария WMI является предоставление доступа к классам и экземплярам, представляющим объекты в сети.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="bb3d9-105">Эти классы и экземпляры поддерживаются поставщиками.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="bb3d9-106">Например, все экземпляры, представляющие стандартные аппаратные устройства на предприятии, такие как [**Win32 \_ фисикалмемори**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) или [**\_ принтер Win32**](/windows/desktop/CIMWin32Prov/win32-printer), поддерживаются поставщиком Win32.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="bb3d9-107">Аналогичным образом, доступ к журналу событий можно получить с помощью регистратора событий и реестра с помощью поставщика реестра.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="bb3d9-108">Методы, реализуемые WMI в интерфейсах, таких как [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) или объекты скриптов, такие как [**SwbemServices**](swbemservices.md), в основном используются для универсального получения данных, предоставляемых любым поставщиком, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="bb3d9-109">Например, используйте [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) для получения всех экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) в подмножестве компьютеров предприятия.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="bb3d9-110">Затем можно вызвать метод поставщика Win32 [**жетовнерсид**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) для каждого объекта **\_ процесса Win32** .</span><span class="sxs-lookup"><span data-stu-id="bb3d9-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="bb3d9-111">В следующем примере метод [**жетовнерсид**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) вызывается как метод автоматизации для объекта Process.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="bb3d9-112">Метод WMI, например метод [**\_ path**](swbemobject-path-.md) , определенный для [**SWbemObject**](swbemobject.md) , также может вызываться для объекта **Process** .</span><span class="sxs-lookup"><span data-stu-id="bb3d9-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="bb3d9-113">Фактический процесс использования методов WMI идентичен использованию любых других интерфейсов COM или интерфейса автоматизации Windows.</span><span class="sxs-lookup"><span data-stu-id="bb3d9-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="bb3d9-114">Дополнительные сведения см. в разделе [com](../cossdk/component-services-portal.md) и [Создание приложения или скрипта WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d9-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="bb3d9-115">Дополнительные сведения о интерфейсах, поддерживаемых WMI, см. в разделе [API COM для WMI](com-api-for-wmi.md) и [API сценариев для WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d9-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="bb3d9-116">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d9-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb3d9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="bb3d9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb3d9-118">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="bb3d9-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
