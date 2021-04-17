---
description: Квалификатор CounterType содержит целочисленное значение для типа счетчика свойств в \_ классах Win32 перфравдата. Кукингтипе содержит константы для типов формул свойств в \_ классах Win32 перфформаттеддата.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Квалификатор CounterType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673533"
---
# <a name="countertype-qualifier"></a><span data-ttu-id="3c695-104">Квалификатор CounterType</span><span class="sxs-lookup"><span data-stu-id="3c695-104">CounterType Qualifier</span></span>

<span data-ttu-id="3c695-105">Квалификатор **CounterType** содержит целочисленное значение для типа счетчика свойств в классах [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="3c695-105">The **CounterType** qualifier contains the integer value for the property counter type for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span> <span data-ttu-id="3c695-106">**Кукингтипе** содержит константы для типов формул свойств в классах [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="3c695-106">The **CookingType** contains the constants for property formula types in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="3c695-107">Дополнительные сведения и подразделение типов счетчиков по функциям см. в разделе [типы счетчиков](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="3c695-107">For more information and a breakdown of counter types by function, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>



| <span data-ttu-id="3c695-108">CounterType</span><span class="sxs-lookup"><span data-stu-id="3c695-108">CounterType</span></span> | <span data-ttu-id="3c695-109">кукингтипе</span><span class="sxs-lookup"><span data-stu-id="3c695-109">CookingType</span></span>                              |
|-------------|------------------------------------------|
| <span data-ttu-id="3c695-110">0</span><span class="sxs-lookup"><span data-stu-id="3c695-110">0</span></span>           | <span data-ttu-id="3c695-111">\_равкаунт счетчика производительности " \_ \_ Шестнадцатеричный"</span><span class="sxs-lookup"><span data-stu-id="3c695-111">PERF\_COUNTER\_RAWCOUNT\_HEX</span></span>             |
| <span data-ttu-id="3c695-112">256</span><span class="sxs-lookup"><span data-stu-id="3c695-112">256</span></span>         | <span data-ttu-id="3c695-113">Счетчик производительности " \_ \_ крупный \_ равкаунт \_ Hex"</span><span class="sxs-lookup"><span data-stu-id="3c695-113">PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX</span></span>      |
| <span data-ttu-id="3c695-114">2816</span><span class="sxs-lookup"><span data-stu-id="3c695-114">2816</span></span>        | <span data-ttu-id="3c695-115">\_текст счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-115">PERF\_COUNTER\_TEXT</span></span>                      |
| <span data-ttu-id="3c695-116">65536</span><span class="sxs-lookup"><span data-stu-id="3c695-116">65536</span></span>       | <span data-ttu-id="3c695-117">\_равкаунт счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-117">PERF\_COUNTER\_RAWCOUNT</span></span>                  |
| <span data-ttu-id="3c695-118">65792</span><span class="sxs-lookup"><span data-stu-id="3c695-118">65792</span></span>       | <span data-ttu-id="3c695-119">Счетчик производительности " \_ \_ крупный \_ равкаунт"</span><span class="sxs-lookup"><span data-stu-id="3c695-119">PERF\_COUNTER\_LARGE\_RAWCOUNT</span></span>           |
| <span data-ttu-id="3c695-120">73728</span><span class="sxs-lookup"><span data-stu-id="3c695-120">73728</span></span>       | <span data-ttu-id="3c695-121">Счетчик производительности \_ Double \_ RAW</span><span class="sxs-lookup"><span data-stu-id="3c695-121">PERF\_DOUBLE\_RAW</span></span>                        |
| <span data-ttu-id="3c695-122">4195328</span><span class="sxs-lookup"><span data-stu-id="3c695-122">4195328</span></span>     | <span data-ttu-id="3c695-123">\_Дельта счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-123">PERF\_COUNTER\_DELTA</span></span>                     |
| <span data-ttu-id="3c695-124">4195584</span><span class="sxs-lookup"><span data-stu-id="3c695-124">4195584</span></span>     | <span data-ttu-id="3c695-125">\_ \_ большой Дельта СЧЕТЧИКа производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-125">PERF\_COUNTER\_LARGE\_DELTA</span></span>              |
| <span data-ttu-id="3c695-126">4260864</span><span class="sxs-lookup"><span data-stu-id="3c695-126">4260864</span></span>     | <span data-ttu-id="3c695-127">\_Счетчик выборки производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-127">PERF\_SAMPLE\_COUNTER</span></span>                    |
| <span data-ttu-id="3c695-128">4523008</span><span class="sxs-lookup"><span data-stu-id="3c695-128">4523008</span></span>     | <span data-ttu-id="3c695-129">\_тип куеуелен счетчика производительности \_ \_</span><span class="sxs-lookup"><span data-stu-id="3c695-129">PERF\_COUNTER\_QUEUELEN\_TYPE</span></span>            |
| <span data-ttu-id="3c695-130">4523264</span><span class="sxs-lookup"><span data-stu-id="3c695-130">4523264</span></span>     | <span data-ttu-id="3c695-131">\_ \_ большой \_ тип КУЕУЕЛЕН счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-131">PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="3c695-132">5571840</span><span class="sxs-lookup"><span data-stu-id="3c695-132">5571840</span></span>     | <span data-ttu-id="3c695-133">\_ \_ \_ Тип куеуелен 100 для счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-133">PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="3c695-134">6620416</span><span class="sxs-lookup"><span data-stu-id="3c695-134">6620416</span></span>     | <span data-ttu-id="3c695-135">\_ \_ \_ \_ тип куеуелен времени obj для счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-135">PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE</span></span> |
| <span data-ttu-id="3c695-136">272696320</span><span class="sxs-lookup"><span data-stu-id="3c695-136">272696320</span></span>   | <span data-ttu-id="3c695-137">\_Счетчик счетчиков производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-137">PERF\_COUNTER\_COUNTER</span></span>                   |
| <span data-ttu-id="3c695-138">272696576</span><span class="sxs-lookup"><span data-stu-id="3c695-138">272696576</span></span>   | <span data-ttu-id="3c695-139">Счетчик производительности " \_ \_ небольшого \_ числа"</span><span class="sxs-lookup"><span data-stu-id="3c695-139">PERF\_COUNTER\_BULK\_COUNT</span></span>               |
| <span data-ttu-id="3c695-140">537003008</span><span class="sxs-lookup"><span data-stu-id="3c695-140">537003008</span></span>   | <span data-ttu-id="3c695-141">\_необработанная \_ дробь производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-141">PERF\_RAW\_FRACTION</span></span>                      |
| <span data-ttu-id="3c695-142">541132032</span><span class="sxs-lookup"><span data-stu-id="3c695-142">541132032</span></span>   | <span data-ttu-id="3c695-143">\_таймер счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-143">PERF\_COUNTER\_TIMER</span></span>                     |
| <span data-ttu-id="3c695-144">541525248</span><span class="sxs-lookup"><span data-stu-id="3c695-144">541525248</span></span>   | <span data-ttu-id="3c695-145">\_ \_ системный таймер точности \_ производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-145">PERF\_PRECISION\_SYSTEM\_TIMER</span></span>           |
| <span data-ttu-id="3c695-146">542180608</span><span class="sxs-lookup"><span data-stu-id="3c695-146">542180608</span></span>   | <span data-ttu-id="3c695-147">\_Таймер 100NSEC \_ производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-147">PERF\_100NSEC\_TIMER</span></span>                     |
| <span data-ttu-id="3c695-148">542573824</span><span class="sxs-lookup"><span data-stu-id="3c695-148">542573824</span></span>   | <span data-ttu-id="3c695-149">\_ \_ Таймер 100 для точности производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-149">PERF\_PRECISION\_100NS\_TIMER</span></span>            |
| <span data-ttu-id="3c695-150">543229184</span><span class="sxs-lookup"><span data-stu-id="3c695-150">543229184</span></span>   | <span data-ttu-id="3c695-151">\_таймер времени на obj- \_ время \_</span><span class="sxs-lookup"><span data-stu-id="3c695-151">PERF\_OBJ\_TIME\_TIMER</span></span>                   |
| <span data-ttu-id="3c695-152">543622400</span><span class="sxs-lookup"><span data-stu-id="3c695-152">543622400</span></span>   | <span data-ttu-id="3c695-153">\_ \_ таймер объекта точности \_ производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-153">PERF\_PRECISION\_OBJECT\_TIMER</span></span>           |
| <span data-ttu-id="3c695-154">549585920</span><span class="sxs-lookup"><span data-stu-id="3c695-154">549585920</span></span>   | <span data-ttu-id="3c695-155">\_Простая дробь для образца производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-155">PERF\_SAMPLE\_FRACTION</span></span>                   |
| <span data-ttu-id="3c695-156">557909248</span><span class="sxs-lookup"><span data-stu-id="3c695-156">557909248</span></span>   | <span data-ttu-id="3c695-157">\_таймер счетчика производительности " \_ \_ Инв"</span><span class="sxs-lookup"><span data-stu-id="3c695-157">PERF\_COUNTER\_TIMER\_INV</span></span>                |
| <span data-ttu-id="3c695-158">558957824</span><span class="sxs-lookup"><span data-stu-id="3c695-158">558957824</span></span>   | <span data-ttu-id="3c695-159">\_Таймер 100NSEC \_ производительности \_ Инв</span><span class="sxs-lookup"><span data-stu-id="3c695-159">PERF\_100NSEC\_TIMER\_INV</span></span>                |
| <span data-ttu-id="3c695-160">574686464</span><span class="sxs-lookup"><span data-stu-id="3c695-160">574686464</span></span>   | <span data-ttu-id="3c695-161">Счетчик производительности " \_ \_ несколько \_ таймеров"</span><span class="sxs-lookup"><span data-stu-id="3c695-161">PERF\_COUNTER\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="3c695-162">575735040</span><span class="sxs-lookup"><span data-stu-id="3c695-162">575735040</span></span>   | <span data-ttu-id="3c695-163">100NSEC производительности с \_ \_ несколькими \_ таймерами</span><span class="sxs-lookup"><span data-stu-id="3c695-163">PERF\_100NSEC\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="3c695-164">591463680</span><span class="sxs-lookup"><span data-stu-id="3c695-164">591463680</span></span>   | <span data-ttu-id="3c695-165">Счетчик производительности " \_ \_ Multi \_ Timer \_ Инв"</span><span class="sxs-lookup"><span data-stu-id="3c695-165">PERF\_COUNTER\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="3c695-166">592512256</span><span class="sxs-lookup"><span data-stu-id="3c695-166">592512256</span></span>   | <span data-ttu-id="3c695-167">PERF \_ 100NSEC \_ Multi \_ Timer \_ Инв</span><span class="sxs-lookup"><span data-stu-id="3c695-167">PERF\_100NSEC\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="3c695-168">805438464</span><span class="sxs-lookup"><span data-stu-id="3c695-168">805438464</span></span>   | <span data-ttu-id="3c695-169">\_таймер среднего значения производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-169">PERF\_AVERAGE\_TIMER</span></span>                     |
| <span data-ttu-id="3c695-170">807666944</span><span class="sxs-lookup"><span data-stu-id="3c695-170">807666944</span></span>   | <span data-ttu-id="3c695-171">\_затраченное \_ время производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-171">PERF\_ELAPSED\_TIME</span></span>                      |
| <span data-ttu-id="3c695-172">1073742336</span><span class="sxs-lookup"><span data-stu-id="3c695-172">1073742336</span></span>  | <span data-ttu-id="3c695-173">Cчетчик \_ счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-173">PERF\_COUNTER\_NODATA</span></span>                    |
| <span data-ttu-id="3c695-174">1073874176</span><span class="sxs-lookup"><span data-stu-id="3c695-174">1073874176</span></span>  | <span data-ttu-id="3c695-175">Средний показатель производительности \_ \_</span><span class="sxs-lookup"><span data-stu-id="3c695-175">PERF\_AVERAGE\_BULK</span></span>                      |
| <span data-ttu-id="3c695-176">1073939457</span><span class="sxs-lookup"><span data-stu-id="3c695-176">1073939457</span></span>  | <span data-ttu-id="3c695-177">\_Базовый образец \_ производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-177">PERF\_SAMPLE\_BASE</span></span>                       |
| <span data-ttu-id="3c695-178">1073939458</span><span class="sxs-lookup"><span data-stu-id="3c695-178">1073939458</span></span>  | <span data-ttu-id="3c695-179">\_Базовое среднее значение производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-179">PERF\_AVERAGE\_BASE</span></span>                      |
| <span data-ttu-id="3c695-180">1073939459</span><span class="sxs-lookup"><span data-stu-id="3c695-180">1073939459</span></span>  | <span data-ttu-id="3c695-181">\_необработанная \_ база производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-181">PERF\_RAW\_BASE</span></span>                          |
| <span data-ttu-id="3c695-182">1073939712</span><span class="sxs-lookup"><span data-stu-id="3c695-182">1073939712</span></span>  | <span data-ttu-id="3c695-183">\_ \_ Метка времени точности производительности</span><span class="sxs-lookup"><span data-stu-id="3c695-183">PERF\_PRECISION\_TIMESTAMP</span></span>               |
| <span data-ttu-id="3c695-184">1073939715</span><span class="sxs-lookup"><span data-stu-id="3c695-184">1073939715</span></span>  | <span data-ttu-id="3c695-185">\_необработанная база производительности больших объемов \_ \_</span><span class="sxs-lookup"><span data-stu-id="3c695-185">PERF\_LARGE\_RAW\_BASE</span></span>                   |
| <span data-ttu-id="3c695-186">1107494144</span><span class="sxs-lookup"><span data-stu-id="3c695-186">1107494144</span></span>  | <span data-ttu-id="3c695-187">\_ \_ множественная база СЧЕТЧИКа производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-187">PERF\_COUNTER\_MULTI\_BASE</span></span>               |
| <span data-ttu-id="3c695-188">2147483648</span><span class="sxs-lookup"><span data-stu-id="3c695-188">2147483648</span></span>  | <span data-ttu-id="3c695-189">\_ \_ Тип гистограммы СЧЕТЧИКа производительности \_</span><span class="sxs-lookup"><span data-stu-id="3c695-189">PERF\_COUNTER\_HISTOGRAM\_TYPE</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="3c695-190">Требования</span><span class="sxs-lookup"><span data-stu-id="3c695-190">Requirements</span></span>



| <span data-ttu-id="3c695-191">Требование</span><span class="sxs-lookup"><span data-stu-id="3c695-191">Requirement</span></span> | <span data-ttu-id="3c695-192">Значение</span><span class="sxs-lookup"><span data-stu-id="3c695-192">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3c695-193">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c695-193">Minimum supported client</span></span><br/> | <span data-ttu-id="3c695-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c695-194">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3c695-195">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c695-195">Minimum supported server</span></span><br/> | <span data-ttu-id="3c695-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c695-196">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c695-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c695-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c695-198">Квалификаторы, относящиеся к классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="3c695-198">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

