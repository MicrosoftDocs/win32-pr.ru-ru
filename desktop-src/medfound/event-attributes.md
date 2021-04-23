---
description: Атрибуты событий
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Атрибуты событий (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539551"
---
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="63374-103">Атрибуты событий (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="63374-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="63374-104">Следующие атрибуты применяются к событиям.</span><span class="sxs-lookup"><span data-stu-id="63374-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="63374-105">attribute</span><span class="sxs-lookup"><span data-stu-id="63374-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="63374-106">Описание</span><span class="sxs-lookup"><span data-stu-id="63374-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63374-107">**\_событие MF \_ — \_ сужение**</span><span class="sxs-lookup"><span data-stu-id="63374-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="63374-108">Когда источник мультимедиа запрашивает новый уровень воспроизведения, указывает, запрашивается ли нетонкое воспроизведение источника.</span><span class="sxs-lookup"><span data-stu-id="63374-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="63374-109">**\_ \_ узел вывода событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="63374-110">Определяет узел топологии для приемника потока.</span><span class="sxs-lookup"><span data-stu-id="63374-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="63374-111">**\_ \_ \_ смещение времени презентации событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="63374-112">Смещение между временем презентации и штампами времени источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="63374-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="63374-113">**\_ \_ время СКРУБСАМПЛЕ события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="63374-114">Время презентации для примера, отображаемого во время очистки.</span><span class="sxs-lookup"><span data-stu-id="63374-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="63374-115">**\_сессионкапс событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="63374-116">Содержит флаги, определяющие возможности сеанса мультимедиа на основе текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="63374-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="63374-117">**\_Дельта событий MF \_ сессионкапс \_**</span><span class="sxs-lookup"><span data-stu-id="63374-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="63374-118">Содержит флаги, указывающие, какие возможности были изменены в сеансе мультимедиа на основе текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="63374-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="63374-119">**\_ \_ \_ Фактическое начало источника события MF \_**</span><span class="sxs-lookup"><span data-stu-id="63374-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="63374-120">Содержит время начала, когда источник мультимедиа перезапускается с текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="63374-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="63374-121">**\_ \_ характеристики источника события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="63374-122">Задает текущие характеристики источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="63374-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="63374-123">**\_ \_ \_ старые характеристики источника события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="63374-124">Задает предыдущие характеристики источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="63374-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="63374-125">**\_ \_ \_ поддельный \_ Запуск источника события MF**</span><span class="sxs-lookup"><span data-stu-id="63374-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="63374-126">Указывает, пуста ли текущая топология сегмента.</span><span class="sxs-lookup"><span data-stu-id="63374-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="63374-127">**\_ \_ прожектстарт источник события \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="63374-128">Указывает время начала для топологии сегмента.</span><span class="sxs-lookup"><span data-stu-id="63374-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="63374-129">**\_ \_ топология источника событий MF \_ \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="63374-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="63374-130">Указывает, отменила ли источник Sequencer топологию.</span><span class="sxs-lookup"><span data-stu-id="63374-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="63374-131">**\_ \_ \_ время начала презентации \_ для события MF**</span><span class="sxs-lookup"><span data-stu-id="63374-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="63374-132">Время начала презентации в единицах измерения 100-наносекундных, измеряемое часами представления.</span><span class="sxs-lookup"><span data-stu-id="63374-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="63374-133">**\_событие MF \_ Запуск \_ \_ во время презентации \_ на \_ выходе**</span><span class="sxs-lookup"><span data-stu-id="63374-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="63374-134">Время презентации, с которой приемники мультимедиа выводит первый образец новой топологии.</span><span class="sxs-lookup"><span data-stu-id="63374-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="63374-135">**\_ \_ состояние ТОПОЛОГИИ событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="63374-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="63374-136">Указывает состояние топологии во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="63374-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="63374-137">**\_время сеанса MF, \_ около \_ \_ времени возникновения события \_**</span><span class="sxs-lookup"><span data-stu-id="63374-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="63374-138">Приблизительное время, когда сеанс мультимедиа вызвал событие.</span><span class="sxs-lookup"><span data-stu-id="63374-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="63374-139">См. также</span><span class="sxs-lookup"><span data-stu-id="63374-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63374-140">**имфмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="63374-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="63374-141">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63374-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="63374-142">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63374-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



