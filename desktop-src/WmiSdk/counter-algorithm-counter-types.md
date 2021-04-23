---
description: Типы счетчиков алгоритмов счетчиков могут вычислять ставки или средние значения байтов для выборки или за определенный период времени для определенной операции.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Типы счетчиков алгоритмов счетчиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346745"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="8a0b2-103">Типы счетчиков алгоритмов счетчиков</span><span class="sxs-lookup"><span data-stu-id="8a0b2-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="8a0b2-104">Типы счетчиков алгоритмов счетчиков могут вычислять ставки или средние значения байтов для выборки или за определенный период времени для определенной операции.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="8a0b2-105">Свойство **авгдискбитеспертрансфер** в классе [**\_ Перфравдата \_ перфдиск \_ физического диска Win32**](/previous-versions//aa394308(v=vs.85)) использует среднее значение производительности \_ " \_ массовый CounterType".</span><span class="sxs-lookup"><span data-stu-id="8a0b2-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="8a0b2-106">В этом случае передача выполняется операцией, а количество отправленных байтов — данные счетчика.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="8a0b2-107">Для любого из двух примеров деление разности накопленных байтов на разницу в накопленных передачах приведет к среднему числу байтов на передачу в течение периода между образцами.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="8a0b2-108">Предоставляются следующие алгоритмы счетчиков:</span><span class="sxs-lookup"><span data-stu-id="8a0b2-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="8a0b2-109">CounterType</span><span class="sxs-lookup"><span data-stu-id="8a0b2-109">CounterType</span></span>                                                                                              | <span data-ttu-id="8a0b2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8a0b2-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0b2-111">[Производительность \_ Среднее \_ неполное](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))десятичное число 1073874176</span><span class="sxs-lookup"><span data-stu-id="8a0b2-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="8a0b2-112">Число обработанных элементов в среднем во время операции.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="8a0b2-113">Этот тип счетчика отображает отношение обработанных элементов (например, отправленных байтов) к количеству выполненных операций, а для \_ типа счетчика требуется базовое свойство с базой среднего показателя производительности \_ .</span><span class="sxs-lookup"><span data-stu-id="8a0b2-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="8a0b2-114">[Производительность \_ \_Счетчик счетчиков](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))— десятичное 272696320</span><span class="sxs-lookup"><span data-stu-id="8a0b2-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="8a0b2-115">Среднее количество операций, выполненных в течение каждой секунды интервала выборки.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="8a0b2-116">.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="8a0b2-117">[Производительность \_ Пример десятичного \_ счетчика](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4260864</span><span class="sxs-lookup"><span data-stu-id="8a0b2-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="8a0b2-118">Среднее число операций, выполненных за одну секунду.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="8a0b2-119">Для этого типа счетчика требуется базовое свойство с типом счетчика " \_ \_ базовая база знаний".</span><span class="sxs-lookup"><span data-stu-id="8a0b2-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="8a0b2-120">[Производительность \_ Счетчик \_ числа \_ больших](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))чисел 272696576</span><span class="sxs-lookup"><span data-stu-id="8a0b2-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="8a0b2-121">Среднее количество операций, выполненных в течение каждой секунды интервала выборки.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="8a0b2-122">Этот тип счетчика совпадает с \_ \_ типом счетчика счетчика производительности, но использует большие поля для размещения больших значений.</span><span class="sxs-lookup"><span data-stu-id="8a0b2-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="8a0b2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8a0b2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a0b2-124">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="8a0b2-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

