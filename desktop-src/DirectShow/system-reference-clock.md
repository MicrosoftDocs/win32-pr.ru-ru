---
description: Время системных ссылок
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Время системных ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909492"
---
# <a name="system-reference-clock"></a><span data-ttu-id="dcf05-103">Время системных ссылок</span><span class="sxs-lookup"><span data-stu-id="dcf05-103">System Reference Clock</span></span>

<span data-ttu-id="dcf05-104">Объект часов системных ссылок реализует ссылочный период времени, который возвращает системное время.</span><span class="sxs-lookup"><span data-stu-id="dcf05-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="dcf05-105">Если ни один из фильтров в графе не предоставляет эталонные часы, диспетчер графов фильтров использует этот компонент для синхронизации графа.</span><span class="sxs-lookup"><span data-stu-id="dcf05-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="dcf05-106">Создайте этот объект, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="dcf05-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="dcf05-107">Метка</span><span class="sxs-lookup"><span data-stu-id="dcf05-107">Label</span></span> | <span data-ttu-id="dcf05-108">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf05-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf05-109">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="dcf05-109">Class Identifier</span></span> | <span data-ttu-id="dcf05-110">\_СИСТЕМКЛОКК CLSID</span><span class="sxs-lookup"><span data-stu-id="dcf05-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="dcf05-111">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="dcf05-111">Interfaces</span></span>       | <span data-ttu-id="dcf05-112">[**Иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**иреференцеклокктимерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="dcf05-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dcf05-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dcf05-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcf05-114">Объекты DirectShow</span><span class="sxs-lookup"><span data-stu-id="dcf05-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="dcf05-115">Эталонные часы</span><span class="sxs-lookup"><span data-stu-id="dcf05-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="dcf05-116">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="dcf05-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



