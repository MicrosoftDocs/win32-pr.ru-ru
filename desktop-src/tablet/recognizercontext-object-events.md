---
description: В следующей таблице описаны потоки, на которых могут срабатывать события объекта Рекогнизерконтекст. Евентсреадсрекогнитионфирес в потоке распознавания фона или в потоке, который вызывает метод распознавания объекта Рекогнизерконтекст. Рекогнитионвисалтернатесфирес в потоке распознавания фона.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: События объекта Рекогнизерконтекст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999044"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="f3194-103">События объекта Рекогнизерконтекст</span><span class="sxs-lookup"><span data-stu-id="f3194-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="f3194-104">В следующей таблице описаны потоки, на которых могут срабатывать события объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f3194-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="f3194-105">Событие</span><span class="sxs-lookup"><span data-stu-id="f3194-105">Event</span></span>                                                                               | <span data-ttu-id="f3194-106">Потоки</span><span class="sxs-lookup"><span data-stu-id="f3194-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3194-107">**Распознавание**</span><span class="sxs-lookup"><span data-stu-id="f3194-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="f3194-108">Срабатывает в потоке распознавания фона или в потоке, который вызывает метод [**распознавания**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f3194-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="f3194-109">**рекогнитионвисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="f3194-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="f3194-110">Активируется в фоновом потоке распознавания.</span><span class="sxs-lookup"><span data-stu-id="f3194-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




