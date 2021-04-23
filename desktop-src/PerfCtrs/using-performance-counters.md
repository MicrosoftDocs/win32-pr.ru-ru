---
description: Сведения об использовании данных счетчика см. в разделе Использование данных счетчика.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Использование счетчиков производительности
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663144"
---
# <a name="using-performance-counters"></a><span data-ttu-id="cb8ac-103">Использование счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="cb8ac-103">Using Performance Counters</span></span>

<span data-ttu-id="cb8ac-104">**Потребители** счетчиков производительности — это программные компоненты, собирающие и использующие данные счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-104">Performance counter **consumers** are software components that collect and make use of performance counter data.</span></span> <span data-ttu-id="cb8ac-105">Например, потребители, предоставляемые корпорацией Майкрософт, включают системный монитор (perfmon.exe), монитор ресурсов (resmon.exe), Log Manager (logman.exe) и typeperf.exe.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-105">Example consumers provided by Microsoft include Performance Monitor (perfmon.exe), Resource Monitor (resmon.exe), Log Manager (logman.exe) and typeperf.exe.</span></span> <span data-ttu-id="cb8ac-106">Сторонние программные компоненты также могут собирать данные о производительности с помощью API сбора данных о производительности или с помощью классов счетчиков производительности WMI.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-106">Third-party software components may also collect performance data via performance collection APIs or via WMI performance counter classes.</span></span>

<span data-ttu-id="cb8ac-107">**Поставщики** счетчиков производительности — это программные компоненты, которые публикуют данные счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-107">Performance counter **providers** are software components that publish performance counter data.</span></span> <span data-ttu-id="cb8ac-108">Счетчики производительности могут предоставляться компонентами операционной системы, драйверами устройств и службами.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-108">Performance counters can be provided by operating system components, device drivers, and services.</span></span> <span data-ttu-id="cb8ac-109">Многие счетчики производительности предоставляются как часть операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-109">Many performance counters are provided as part of the Windows operating system.</span></span> <span data-ttu-id="cb8ac-110">Программные компоненты сторонних производителей могут предоставлять дополнительные счетчики через API поставщика счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-110">Additional counters may be provided by third-party software components via the performance counter provider APIs.</span></span>

- <span data-ttu-id="cb8ac-111">Используйте [средства счетчиков производительности](performance-counters-tools.md) , если требуется получить или просмотреть данные счетчика из системы.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-111">Use [Performance Counter Tools](performance-counters-tools.md) when you want to collect or view the counter data from a system.</span></span>
- <span data-ttu-id="cb8ac-112">Используйте [API-интерфейсы потребителя счетчика производительности](consuming-counter-data.md) , если требуется написать программу, собирающую данные счетчиков из локальной системы.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-112">Use [Performance Counter Consumer APIs](consuming-counter-data.md) when you want to write a program that collects counter data from the local system.</span></span>
- <span data-ttu-id="cb8ac-113">Используйте [Классы счетчиков производительности WMI](/windows/desktop/WmiSdk/monitoring-performance-data) , если требуется получить данные счетчиков из локальной или удаленной системы с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-113">Use [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) when you want to collect counter data from a local or remote system using WMI.</span></span>
- <span data-ttu-id="cb8ac-114">Используйте [API поставщика счетчиков производительности](providing-counter-data.md) , если требуется опубликовать данные счетчиков производительности из программного компонента.</span><span class="sxs-lookup"><span data-stu-id="cb8ac-114">Use [Performance Counter Provider APIs](providing-counter-data.md) when you want to publish performance counter data from your software component.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb8ac-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb8ac-115">See also</span></span>

[<span data-ttu-id="cb8ac-116">Сведения о счетчиках производительности</span><span class="sxs-lookup"><span data-stu-id="cb8ac-116">About Performance Counters</span></span>](about-performance-counters.md)

[<span data-ttu-id="cb8ac-117">Справочник по счетчикам производительности</span><span class="sxs-lookup"><span data-stu-id="cb8ac-117">Performance Counters Reference</span></span>](performance-counters-reference.md)
