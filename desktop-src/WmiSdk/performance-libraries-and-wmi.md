---
description: Поставщик Вмиперфкласс и поставщик Вмиперфинст динамически предоставляют данные счетчиков производительности для классов счетчиков производительности WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Библиотеки производительности и инструментарий WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701787"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="83b61-103">Библиотеки производительности и инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="83b61-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="83b61-104">[Поставщик вмиперфкласс](wmiperfclass-provider.md) и [поставщик вмиперфинст](wmiperfinst-provider.md) динамически предоставляют данные счетчиков производительности для [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="83b61-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="83b61-105">Поставщики Вмиперфкласс и Вмиперфинст</span><span class="sxs-lookup"><span data-stu-id="83b61-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="83b61-106">[Поставщик вмиперфкласс](wmiperfclass-provider.md) создает [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI при инициализации системы.</span><span class="sxs-lookup"><span data-stu-id="83b61-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="83b61-107">[Поставщик вмиперфинст](wmiperfinst-provider.md) динамически предоставляет данные счетчиков производительности для этих классов.</span><span class="sxs-lookup"><span data-stu-id="83b61-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="83b61-108">Поставщик поставщика Вмиперфкласс предоставляет классы для [счетчиков производительности](/windows/desktop/PerfCtrs/performance-counters-portal)версии 1 и версии 2.</span><span class="sxs-lookup"><span data-stu-id="83b61-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="83b61-109">Счетчики версии 1 находятся в реестре в разделе **hKey \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**.</span><span class="sxs-lookup"><span data-stu-id="83b61-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="83b61-110">Службы, предоставляющие данные о производительности, имеют подраздел **производительности** .</span><span class="sxs-lookup"><span data-stu-id="83b61-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="83b61-111">Классы производительности WMI, созданные из счетчиков версии 1, не имеют "счетчиков" в составе имени.</span><span class="sxs-lookup"><span data-stu-id="83b61-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="83b61-112">**Идентификатор GUID**, определяющий поставщик счетчика производительности версии 2, находится в реестре в разделе **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ PerfLib \\ \_ V2Providers**.</span><span class="sxs-lookup"><span data-stu-id="83b61-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="83b61-113">Вмиперфкласс регистрируется как стандартный поставщик классов WMI.</span><span class="sxs-lookup"><span data-stu-id="83b61-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="83b61-114">Вмиперфинст — это поставщик экземпляров WMI, предоставляющий данные из модуля поддержки данных производительности (PDH) для счетчиков версии 1 и версии 2.</span><span class="sxs-lookup"><span data-stu-id="83b61-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="83b61-115">Дополнительные сведения см. в разделе [Использование функций PDH для использования данных счетчика](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="83b61-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83b61-116">См. также</span><span class="sxs-lookup"><span data-stu-id="83b61-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83b61-117">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="83b61-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="83b61-118">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="83b61-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
