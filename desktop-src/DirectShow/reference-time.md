---
description: ССЫЛОЧный \_ тип данных определяет единицы времени ссылки в DirectShow. Каждая единица времени ссылки составляет 100 наносекунд.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Стрмиф. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689275"
---
# <a name="reference_time"></a><span data-ttu-id="ae830-104">\_время ссылки</span><span class="sxs-lookup"><span data-stu-id="ae830-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="ae830-105">**Ссылочный \_** тип данных определяет единицы времени ссылки в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae830-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="ae830-106">Каждая единица времени ссылки составляет 100 наносекунд.</span><span class="sxs-lookup"><span data-stu-id="ae830-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="ae830-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae830-107">Remarks</span></span>

<span data-ttu-id="ae830-108">Тип данных **ссылочного \_ времени** — это 64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="ae830-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="ae830-109">Время ссылки обычно измеряется в одном из следующих базовых показателей:</span><span class="sxs-lookup"><span data-stu-id="ae830-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="ae830-110">Абсолютное время.</span><span class="sxs-lookup"><span data-stu-id="ae830-110">An absolute clock time.</span></span> <span data-ttu-id="ae830-111">В этом случае базовый уровень будет зависеть от реализации часов.</span><span class="sxs-lookup"><span data-stu-id="ae830-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="ae830-112">Дополнительные сведения см. в разделе [эталонные часы](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="ae830-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="ae830-113">Относительно начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ae830-113">Relative to the start of playback.</span></span>

<span data-ttu-id="ae830-114">Дополнительные сведения о времени ссылки см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ae830-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae830-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ae830-115">Requirements</span></span>



| <span data-ttu-id="ae830-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ae830-116">Requirement</span></span> | <span data-ttu-id="ae830-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ae830-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae830-118">Header</span><span class="sxs-lookup"><span data-stu-id="ae830-118">Header</span></span><br/> | <dl> <span data-ttu-id="ae830-119"><dt>Стрмиф. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae830-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae830-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae830-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae830-121">Типы данных DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae830-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




