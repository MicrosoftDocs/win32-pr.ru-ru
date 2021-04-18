---
description: Модель временной шкалы
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Модель временной шкалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559069"
---
# <a name="the-timeline-model"></a><span data-ttu-id="1cd4b-103">Модель временной шкалы</span><span class="sxs-lookup"><span data-stu-id="1cd4b-103">The Timeline Model</span></span>

<span data-ttu-id="1cd4b-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="1cd4b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1cd4b-105">*Временная шкала* — это объект, используемый [службами редактирования DirectShow](directshow-editing-services.md) (DES) для представления проекта редактирования видео.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="1cd4b-106">Проект редактирования запускается как коллекция исходных клипов, взятых из видеофайлов, звуковых файлов или по-прежнему файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="1cd4b-107">Линейная последовательность клипов образуется на *дорожке*. В службах редактирования DirectShow (DES) аудио и видео помещаются в отдельные дорожки.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="1cd4b-108">Дорожки также могут быть слоены.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-108">Tracks can also be layered.</span></span> <span data-ttu-id="1cd4b-109">Несколько звуковых дорожек смешиваются вместе и могут включать звуковые эффекты, такие как исчезновение или переглаголы.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="1cd4b-110">Для создания переходов используется несколько видеодорожек.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="1cd4b-111">Например, можно создать очистку от одного клипа к другому.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="1cd4b-112">Еще один пример — ключ чрома, в котором фон одного клипа отключается и заменяется другой записью. (Например, прогноз погоды перед изображением Сателите — это пример ключа чрома.)</span><span class="sxs-lookup"><span data-stu-id="1cd4b-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="1cd4b-113">Для представления редактирования DES использует древовидную структуру:</span><span class="sxs-lookup"><span data-stu-id="1cd4b-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="1cd4b-114">Аудиоклипы и видеоклипы формируют конечные узлы или *исходные* объекты.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="1cd4b-115">Набор источников с равномерным типом мультимедиа (аудио или видео) — это *дорожка*.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="1cd4b-116">Коллекция дорожек является *композицией*.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="1cd4b-117">Композиция визуализируется как составная часть всех содержащихся в ней дорожек.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="1cd4b-118">Композиции могут содержать другие композиции, что позволяет выполнять сложное упорядочение дорожек.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="1cd4b-119">Набор композиций и дорожек верхнего уровня (все, представляющие один и тот же тип носителя) является *группой*.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="1cd4b-120">Набор из одной или нескольких групп образует *временную шкалу*.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="1cd4b-121">Временная шкала — это корневой узел дерева.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="1cd4b-122">Временная шкала должна содержать по крайней мере одну группу.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="1cd4b-123">Каждая группа представляет один поток в окончательной рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="1cd4b-124">Типичный проект включает одну группу видео и одну звуковую группу.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="1cd4b-125">Композиции необязательны; они существуют, чтобы обеспечить дополнительную структуру при необходимости.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="1cd4b-126">На следующем рисунке показаны отношения дочерних и родительских элементов, которые составляют временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![структура узла](images/timeline1.png)

<span data-ttu-id="1cd4b-128">Ниже показана временная шкала в виде временной последовательности:</span><span class="sxs-lookup"><span data-stu-id="1cd4b-128">The following shows a timeline as a temporal sequence:</span></span>

![Иллюстрация временной шкалы](images/timeline2.png)

<span data-ttu-id="1cd4b-130">Стрелка в верхней части представляет направление временной шкалы, начиная с нулевого времени.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="1cd4b-131">В группе видео дорожка 1 имеет более высокий приоритет, чем дорожка 0.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="1cd4b-132">Исходные объекты в дорожке 1 скрывают их в дорожке 0.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="1cd4b-133">Если значение Track 1 пустое, отследите за отображением 0 ".</span><span class="sxs-lookup"><span data-stu-id="1cd4b-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="1cd4b-134">Как упоминалось ранее, звуковые дорожки просто смешиваются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cd4b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1cd4b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cd4b-136">начало работы с помощью служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="1cd4b-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="1cd4b-137">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="1cd4b-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



