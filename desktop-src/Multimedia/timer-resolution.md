---
title: Разрешение таймера
description: Разрешение таймера
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- Таймеры мультимедиа, разрешение
- таймеры, разрешение
- Минимальное разрешение таймера
- Максимальное разрешение таймера
- Таймеры мультимедиа, максимальное разрешение
- таймеры, максимальное разрешение
- Таймеры мультимедиа, минимальное разрешение
- таймеры, минимальное разрешение
- Функция Тимежетдевкапс
- Функция Тимебегинпериод
- Функция Тиминдпериод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "103772527"
---
# <a name="timer-resolution"></a><span data-ttu-id="04f49-114">Разрешение таймера</span><span class="sxs-lookup"><span data-stu-id="04f49-114">Timer Resolution</span></span>

<span data-ttu-id="04f49-115">Чтобы определить минимальное и максимальное разрешения таймера, поддерживаемые службами таймера, используйте функцию [**тимежетдевкапс**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="04f49-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="04f49-116">Эта функция заполняет элементы **впериодмин** и **впериодмакс** структуры [**тимекапс**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) с минимальным и максимальным разрешением.</span><span class="sxs-lookup"><span data-stu-id="04f49-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="04f49-117">Этот диапазон может различаться для разных компьютеров и платформ Windows.</span><span class="sxs-lookup"><span data-stu-id="04f49-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="04f49-118">Определив минимальное и максимальное доступные разрешения таймера, необходимо установить минимальное разрешение, которое должно использоваться приложением.</span><span class="sxs-lookup"><span data-stu-id="04f49-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="04f49-119">Используйте функции [**тимебегинпериод**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) и [**тиминдпериод**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) , чтобы установить и очистить это разрешение.</span><span class="sxs-lookup"><span data-stu-id="04f49-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="04f49-120">Необходимо сопоставить каждый вызов **тимебегинпериод** с вызовом **тиминдпериод**, указав то же минимальное разрешение в обоих вызовах.</span><span class="sxs-lookup"><span data-stu-id="04f49-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="04f49-121">Приложение может выполнять несколько вызовов **тимебегинпериод** , если каждый вызов соответствует вызову **тиминдпериод**.</span><span class="sxs-lookup"><span data-stu-id="04f49-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="04f49-122">В [**тимебегинпериод**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) и [**тиминдпериод**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)параметр *упериод* указывает минимальное разрешение таймера в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="04f49-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="04f49-123">Можно указать любое значение разрешения таймера в диапазоне, поддерживаемом таймером.</span><span class="sxs-lookup"><span data-stu-id="04f49-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04f49-124">См. также</span><span class="sxs-lookup"><span data-stu-id="04f49-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04f49-125">О таймерах мультимедиа</span><span class="sxs-lookup"><span data-stu-id="04f49-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




