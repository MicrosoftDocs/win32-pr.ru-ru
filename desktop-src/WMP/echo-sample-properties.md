---
title: Свойства образца Echo
description: Свойства образца Echo
ms.assetid: 16f6f963-d746-42dc-872f-6f4db296cab9
keywords:
- Подключаемые модули проигрывателя Windows Media, пример свойств Echo
- подключаемые модули, свойства образца Echo
- подключаемые модули обработки цифровых сигналов, свойства образца эха
- Подключаемые модули DSP, свойства образца Echo
- Пример подключаемого модуля "Echo DSP", свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ae368a75817320e346dab7e3061fb6b3d7d490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411139"
---
# <a name="echo-sample-properties"></a><span data-ttu-id="93fb9-108">Свойства образца Echo</span><span class="sxs-lookup"><span data-stu-id="93fb9-108">Echo Sample Properties</span></span>

<span data-ttu-id="93fb9-109">Образец Echo предоставляет два свойства: время задержки и уровень влияния (сочетание задержек).</span><span class="sxs-lookup"><span data-stu-id="93fb9-109">The Echo sample exposes two properties: the delay time and the effect level (wet mix).</span></span> <span data-ttu-id="93fb9-110">Значение для уровня сигнала сухой (сухой Mix) всегда берется из значения Mix.</span><span class="sxs-lookup"><span data-stu-id="93fb9-110">The value for the dry signal level (dry mix) is always derived from the wet mix value.</span></span> <span data-ttu-id="93fb9-111">Необходимо изменить существующий код и добавить новый код, чтобы сделать эти свойства доступными.</span><span class="sxs-lookup"><span data-stu-id="93fb9-111">You need to modify existing code and add some new code to make these properties accessible.</span></span>

<span data-ttu-id="93fb9-112">В следующих разделах объясняется, как изменить код свойств.</span><span class="sxs-lookup"><span data-stu-id="93fb9-112">The following sections explain how to modify the properties code:</span></span>

-   [<span data-ttu-id="93fb9-113">Как работают свойства</span><span class="sxs-lookup"><span data-stu-id="93fb9-113">How Properties Work</span></span>](how-properties-work.md)
-   [<span data-ttu-id="93fb9-114">Переменные для хранения свойств</span><span class="sxs-lookup"><span data-stu-id="93fb9-114">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="93fb9-115">Изменение свойства Scale</span><span class="sxs-lookup"><span data-stu-id="93fb9-115">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="93fb9-116">Добавление свойства "Mix!"</span><span class="sxs-lookup"><span data-stu-id="93fb9-116">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="93fb9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="93fb9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93fb9-118">**Пример эха**</span><span class="sxs-lookup"><span data-stu-id="93fb9-118">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




