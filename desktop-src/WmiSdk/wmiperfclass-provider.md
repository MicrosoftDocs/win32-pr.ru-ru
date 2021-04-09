---
description: Начиная с Windows Vista, этот поставщик создает классы счетчиков производительности WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Поставщик Вмиперфкласс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080890"
---
# <a name="wmiperfclass-provider"></a><span data-ttu-id="07556-103">Поставщик Вмиперфкласс</span><span class="sxs-lookup"><span data-stu-id="07556-103">WmiPerfClass Provider</span></span>

<span data-ttu-id="07556-104">Начиная с Windows Vista, этот поставщик создает [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="07556-104">Starting with Windows Vista, this provider creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="07556-105">Данные динамически передаются этим классам производительности WMI поставщиком [вмиперфинст](wmiperfinst-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="07556-105">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst](wmiperfinst-provider.md) provider.</span></span> <span data-ttu-id="07556-106">Процесс автоопределения и автоочистки (ADAP) больше не передает объекты счетчиков производительности в классы производительности WMI в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="07556-106">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="07556-107">Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="07556-107">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="07556-108">Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="07556-108">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="07556-109">Хотя не рекомендуется разрабатывать новые объекты производительности, создавая высокопроизводительный поставщик WMI и зависящий от процесса [*обратных адаптеров ADAP*](gloss-r.md) для перемещения данных в библиотеки производительности, исключением является разработка WDM драйвера, предоставляющего данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="07556-109">While it is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries, the exception is development of a Windows Driver Model driver that supplies performance data.</span></span> <span data-ttu-id="07556-110">Несмотря на то, что процесс обратного адаптера продолжит работать в целях обратной совместимости, рекомендуется использовать [счетчики производительности версии 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="07556-110">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="07556-111">Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) этого поставщика — "вмиперфкласс".</span><span class="sxs-lookup"><span data-stu-id="07556-111">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfClass".</span></span>

## <a name="related-topics"></a><span data-ttu-id="07556-112">См. также</span><span class="sxs-lookup"><span data-stu-id="07556-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07556-113">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="07556-113">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="07556-114">Библиотеки производительности и инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="07556-114">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="07556-115">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="07556-115">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
