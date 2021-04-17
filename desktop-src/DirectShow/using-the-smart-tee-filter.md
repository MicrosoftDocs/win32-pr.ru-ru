---
description: Использование фильтра Smart Tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Использование фильтра Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663755"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="88223-103">Использование фильтра Smart Tee</span><span class="sxs-lookup"><span data-stu-id="88223-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="88223-104">Если фильтр записи имеет отдельные ПИН-коды для записи и предварительной версии, их можно захватить в ходе предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="88223-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="88223-105">Но если у фильтра нет ПИН-кода для предварительного просмотра, то то же самое можно сделать, включив в диаграмму фильтр [Smart tee](smart-tee-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="88223-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="88223-106">Этот фильтр разделяет данные из ПИН-кода захвата на два идентичных потока: один для записи и один для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="88223-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="88223-107">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="88223-107">The following diagram illustrates this process.</span></span>

![записать граф с помощью фильтра Smart Tee](images/vidcap05.png)

<span data-ttu-id="88223-109">Метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) автоматически вставляет фильтр Smart tee, если он необходим.</span><span class="sxs-lookup"><span data-stu-id="88223-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="88223-110">Однако при использовании методов **играфбуилдер** для построения графа, а не **RenderStream**, может потребоваться вставить фильтр Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="88223-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="88223-111">Перед отображением контактов в фильтре записи проверьте, имеет ли фильтр ПИН-код предварительной версии или ПИН-код порта.</span><span class="sxs-lookup"><span data-stu-id="88223-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="88223-112">Если это не так и вы хотите выполнить предварительный просмотр, добавьте фильтр Smart tee к графу и подключите его к закреплениям захвата в фильтре записи.</span><span class="sxs-lookup"><span data-stu-id="88223-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="88223-113">Вы можете рассматривать ПИН-код в качестве ПИН-кода для предварительного просмотра, поэтому фильтр с ПИН-кодом вице-президента не требует интеллектуального фильтра Tee.</span><span class="sxs-lookup"><span data-stu-id="88223-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="88223-114">Однако у них есть и другие особые требования.</span><span class="sxs-lookup"><span data-stu-id="88223-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="88223-115">Дополнительные сведения см. в статье [ПИН-коды портов видео](video-port-pins.md).</span><span class="sxs-lookup"><span data-stu-id="88223-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88223-116">См. также</span><span class="sxs-lookup"><span data-stu-id="88223-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88223-117">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="88223-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="88223-118">Объединение видеозаписей и предварительной версии</span><span class="sxs-lookup"><span data-stu-id="88223-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="88223-119">Работа с категориями ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="88223-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



