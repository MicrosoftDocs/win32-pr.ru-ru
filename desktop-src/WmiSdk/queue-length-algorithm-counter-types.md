---
description: Типы счетчиков алгоритма длины очереди увеличивают число элементов в очереди на каждый интервал выборки, как указано в соответствующем свойстве Frequency&\# 8212; Frequency \_ перфтиме и т. д.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Типы счетчиков алгоритма длины очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263823"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="e0ae0-103">Типы счетчиков алгоритма длины очереди</span><span class="sxs-lookup"><span data-stu-id="e0ae0-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="e0ae0-104">Типы счетчиков алгоритма длины очереди увеличивают количество элементов в очереди на каждый интервал выборки в соответствии с соответствующей частотой свойства Frequency \_ перфтиме и т. д.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="e0ae0-105">Результат обработанные делится на число выборок, чтобы получить среднюю длину очереди.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="e0ae0-106">Примером является свойство **авгдисккуеуеленгс** в параметре [**Win32 \_ перфравдата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) , который использует \_ \_ \_ тип счетчика производительности 100 НС куеуелен \_ типа.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="e0ae0-107">Константа CounterType</span><span class="sxs-lookup"><span data-stu-id="e0ae0-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="e0ae0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e0ae0-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ae0-109">[Производительность \_ \_ \_ Тип куеуелен счетчика](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span><span class="sxs-lookup"><span data-stu-id="e0ae0-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="e0ae0-110">Средняя длина очереди для ресурса с течением времени.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="e0ae0-111">Он показывает разницу между длинами очередей, наблюдаемых в течение двух последних интервалов измерения, деленную на продолжительность интервала.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="e0ae0-112">[Производительность \_ Счетчик \_ больших \_ куеуелен \_ типа](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span><span class="sxs-lookup"><span data-stu-id="e0ae0-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="e0ae0-113">Средняя длина очереди для ресурса с течением времени.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="e0ae0-114">Счетчики этого типа отображают разницу между длинами очередей, наблюдаемых в течение двух последних интервалов измерения, деленную на продолжительность интервала.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="e0ae0-115">[Производительность \_ Счетчик \_ 100 НС \_ куеуелен \_ тип](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span><span class="sxs-lookup"><span data-stu-id="e0ae0-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="e0ae0-116">Средняя длина очереди для ресурса с течением времени в 100 НС единиц.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="e0ae0-117">[Производительность \_ Счетчик \_ obj- \_ время \_ куеуелен \_ тип](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))десятичный 6620416</span><span class="sxs-lookup"><span data-stu-id="e0ae0-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="e0ae0-118">Время, когда объект находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="e0ae0-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e0ae0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ae0-120">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="e0ae0-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

