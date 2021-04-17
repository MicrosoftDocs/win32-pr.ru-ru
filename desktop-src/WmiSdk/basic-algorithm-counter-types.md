---
description: Представляют различия между образцами со временем и часто используют базовое значение для вычисления.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Типы счетчиков базового алгоритма
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702840"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="4af7a-103">Типы счетчиков базового алгоритма</span><span class="sxs-lookup"><span data-stu-id="4af7a-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="4af7a-104">Типы счетчиков базовых алгоритмов обычно представляют различия между образцами во времени и часто используют базовое значение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="4af7a-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="4af7a-105">Например, свойство **перцентфриспаце** класса [**Win32 \_ перфформаттеддата \_ перфдиск \_ физический**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) диск представляет отношение свободного места, доступного на физическом диске, к общему объему свободного места, предоставленному выбранному физическому диску.</span><span class="sxs-lookup"><span data-stu-id="4af7a-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="4af7a-106">Этот класс также содержит базовое значение **перцентфриспаце \_ base**.</span><span class="sxs-lookup"><span data-stu-id="4af7a-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="4af7a-107">Процент свободного места на диске достигается путем деления **перцентфриспаце** на **перцентфриспаце \_ base** и умножения на 100%.</span><span class="sxs-lookup"><span data-stu-id="4af7a-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="4af7a-108">Ниже приведены основные алгоритмы, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4af7a-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="4af7a-109">Константа CounterType</span><span class="sxs-lookup"><span data-stu-id="4af7a-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="4af7a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4af7a-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af7a-111">[Производительность \_ Необработанное десятичное \_ дробное](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))число 537003008</span><span class="sxs-lookup"><span data-stu-id="4af7a-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="4af7a-112">Отношение подмножества к его набору в процентах.</span><span class="sxs-lookup"><span data-stu-id="4af7a-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="4af7a-113">Этот тип счетчика отображает только текущий процент, а не среднее значение со временем.</span><span class="sxs-lookup"><span data-stu-id="4af7a-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="4af7a-114">[Производительность \_ Пример десятичного \_ дробного](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))числа 549585920</span><span class="sxs-lookup"><span data-stu-id="4af7a-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="4af7a-115">Среднее соотношение попаданий ко всем операциям за последние два интервала выборки.</span><span class="sxs-lookup"><span data-stu-id="4af7a-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="4af7a-116">Для этого типа счетчика требуется базовое свойство с \_ \_ типом базового счетчика "пример производительности".</span><span class="sxs-lookup"><span data-stu-id="4af7a-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="4af7a-117">[Производительность \_ \_Разность значений счетчика](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span><span class="sxs-lookup"><span data-stu-id="4af7a-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="4af7a-118">Счетчик этого типа показывает изменение в измеряемом атрибуте между двумя последними интервалами измерения.</span><span class="sxs-lookup"><span data-stu-id="4af7a-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="4af7a-119">[Производительность \_ Счетчик \_ больших \_ дельта](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))чисел 4195584</span><span class="sxs-lookup"><span data-stu-id="4af7a-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="4af7a-120">То же, что и \_ Дельта счетчика производительности, \_ но 64-разрядное представление для больших значений.</span><span class="sxs-lookup"><span data-stu-id="4af7a-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="4af7a-121">[Производительность \_ Прошедшее \_ время](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)), десятичное 807666944</span><span class="sxs-lookup"><span data-stu-id="4af7a-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="4af7a-122">Общее время между началом процесса и временем вычисления этого значения.</span><span class="sxs-lookup"><span data-stu-id="4af7a-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="4af7a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4af7a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4af7a-124">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="4af7a-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

