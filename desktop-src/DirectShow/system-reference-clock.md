---
description: Время системных ссылок
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Время системных ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674093"
---
# <a name="system-reference-clock"></a><span data-ttu-id="65d83-103">Время системных ссылок</span><span class="sxs-lookup"><span data-stu-id="65d83-103">System Reference Clock</span></span>

<span data-ttu-id="65d83-104">Объект часов системных ссылок реализует ссылочный период времени, который возвращает системное время.</span><span class="sxs-lookup"><span data-stu-id="65d83-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="65d83-105">Если ни один из фильтров в графе не предоставляет эталонные часы, диспетчер графов фильтров использует этот компонент для синхронизации графа.</span><span class="sxs-lookup"><span data-stu-id="65d83-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="65d83-106">Создайте этот объект, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="65d83-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d83-107">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="65d83-107">Class Identifier</span></span> | <span data-ttu-id="65d83-108">\_СИСТЕМКЛОКК CLSID</span><span class="sxs-lookup"><span data-stu-id="65d83-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="65d83-109">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="65d83-109">Interfaces</span></span>       | <span data-ttu-id="65d83-110">[**Иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**иреференцеклокктимерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="65d83-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65d83-111">См. также</span><span class="sxs-lookup"><span data-stu-id="65d83-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d83-112">Объекты DirectShow</span><span class="sxs-lookup"><span data-stu-id="65d83-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="65d83-113">Эталонные часы</span><span class="sxs-lookup"><span data-stu-id="65d83-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="65d83-114">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="65d83-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



