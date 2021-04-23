---
description: Временная шкала
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Временная шкала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684645"
---
# <a name="the-timeline"></a><span data-ttu-id="0a513-103">Временная шкала</span><span class="sxs-lookup"><span data-stu-id="0a513-103">The Timeline</span></span>

<span data-ttu-id="0a513-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="0a513-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0a513-105">Временная шкала предоставляет интерфейс [**иамтимелине**](iamtimeline.md) .</span><span class="sxs-lookup"><span data-stu-id="0a513-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="0a513-106">Этот интерфейс содержит методы для задания свойств на временной шкале. для добавления групп на временную шкалу; и для создания объектов временной шкалы, таких как группы, дорожки и источники.</span><span class="sxs-lookup"><span data-stu-id="0a513-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="0a513-107">Чтобы создать новую временную шкалу, вызовите стандартную функцию **CoCreateInstance** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a513-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="0a513-108">Новая временная шкала пуста.</span><span class="sxs-lookup"><span data-stu-id="0a513-108">The new timeline is empty.</span></span> <span data-ttu-id="0a513-109">На этом этапе можно загрузить существующий файл проекта (см. статью [Загрузка и просмотр проекта](loading-and-previewing-a-project.md)) или создать временную шкалу путем создания и вставки новых объектов (см. раздел [Создание временной шкалы](constructing-a-timeline.md)).</span><span class="sxs-lookup"><span data-stu-id="0a513-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a513-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0a513-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a513-111">Общие сведения о компонентах временной шкалы</span><span class="sxs-lookup"><span data-stu-id="0a513-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



