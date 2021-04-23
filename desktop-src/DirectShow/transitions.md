---
description: Transitions
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912880"
---
# <a name="transitions"></a><span data-ttu-id="fcb55-103">Transitions</span><span class="sxs-lookup"><span data-stu-id="fcb55-103">Transitions</span></span>

<span data-ttu-id="fcb55-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="fcb55-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="fcb55-105">Переход — это способ перехода от одной видеодорожки к другой с помощью визуального эффекта, такого как выцветание или стирание.</span><span class="sxs-lookup"><span data-stu-id="fcb55-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="fcb55-106">На следующем рисунке показана временная шкала с переходом:</span><span class="sxs-lookup"><span data-stu-id="fcb55-106">The following illustration shows a timeline with a transition:</span></span>

![Временная шкала с переходом](images/timeline3.png)

<span data-ttu-id="fcb55-108">Объект перехода находится на дорожке 1 и представляет переход от Track 0 к отслеживанию 1.</span><span class="sxs-lookup"><span data-stu-id="fcb55-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="fcb55-109">В начале перехода визуализированное видео полностью отводится из дорожки 0 (источник а).</span><span class="sxs-lookup"><span data-stu-id="fcb55-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="fcb55-110">В итоге видео полностью отходит от дорожки 1 (источник C).</span><span class="sxs-lookup"><span data-stu-id="fcb55-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="fcb55-111">В между выходные данные переводятся из источника а в источник C. Например, при переходе на выцветание один источник постепенно переключается на другой.</span><span class="sxs-lookup"><span data-stu-id="fcb55-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="fcb55-112">Окончательный результат — схематизированных вдоль нижней части иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="fcb55-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="fcb55-113">Переходы не могут перекрываться по времени в одной дорожке, но перекрывающиеся переходы можно создавать с помощью объекта композиции, как описано в разделе [композиция и разложение](composition-and-layering.md).</span><span class="sxs-lookup"><span data-stu-id="fcb55-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="fcb55-114">Переход имеет направление.</span><span class="sxs-lookup"><span data-stu-id="fcb55-114">A transition has a direction.</span></span> <span data-ttu-id="fcb55-115">По умолчанию он начинается с более низкого приоритета (источник а в предыдущем примере) и заканчивается на дорожке с более высоким приоритетом (источник C).</span><span class="sxs-lookup"><span data-stu-id="fcb55-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="fcb55-116">В между, видео — это смесь двух источников.</span><span class="sxs-lookup"><span data-stu-id="fcb55-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="fcb55-117">Однако можно указать противоположное поведение, как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="fcb55-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![нтракк с двумя переходами](images/fade.png)

<span data-ttu-id="fcb55-119">В этом случае первый переход постепенно исчезает из Track 0, что является поведением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fcb55-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="fcb55-120">Второй переход постепенно уменьшается с 1 до контрольной записи 0.</span><span class="sxs-lookup"><span data-stu-id="fcb55-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="fcb55-121">Обратите внимание, что оба перехода расположены на дорожке 1.</span><span class="sxs-lookup"><span data-stu-id="fcb55-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcb55-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fcb55-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb55-123">начало работы с помощью служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="fcb55-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="fcb55-124">Переходы и эффекты</span><span class="sxs-lookup"><span data-stu-id="fcb55-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="fcb55-125">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="fcb55-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



