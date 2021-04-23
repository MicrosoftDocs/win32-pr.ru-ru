---
description: Наложение фильтра микшера 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Наложение фильтра микшера 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682275"
---
# <a name="overlay-mixer-2-filter"></a><span data-ttu-id="9de08-103">Наложение фильтра микшера 2</span><span class="sxs-lookup"><span data-stu-id="9de08-103">Overlay Mixer 2 Filter</span></span>

<span data-ttu-id="9de08-104">Фильтр оверлея 2 идентичен фильтру [микшера](overlay-mixer-filter.md) наложения, за исключением:</span><span class="sxs-lookup"><span data-stu-id="9de08-104">The Overlay Mixer 2 filter is identical to the [Overlay Mixer](overlay-mixer-filter.md) filter, except:</span></span>

-   <span data-ttu-id="9de08-105">Он поддерживает только типы мультимедиа с форматами [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="9de08-105">It supports only media types with [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats.</span></span>
-   <span data-ttu-id="9de08-106">Он имеет более высокий уровень, что позволяет автоматически добавлять его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="9de08-106">It has a higher merit, which enables it to be added to a filter graph automatically.</span></span>

<span data-ttu-id="9de08-107">Микшер наложения 2 обеспечивает, что диспетчер графов фильтров добавляет его к графу при подготовке к просмотру видео в формате MPEG-2, отличном от DVD.</span><span class="sxs-lookup"><span data-stu-id="9de08-107">The Overlay Mixer 2 is provided so that the Filter Graph Manager will add it to the graph when it renders non-DVD MPEG-2 video.</span></span> <span data-ttu-id="9de08-108">Возможность использования микшера наложения или наложения 2 обрабатывается компонентом, который создает граф, диспетчер графов фильтров, Построитель графов записи или построитель DVD Graph.</span><span class="sxs-lookup"><span data-stu-id="9de08-108">The choice of whether to use the Overlay Mixer or the Overlay Mixer 2 is handled by the component that builds the graph, either the Filter Graph Manager, the Capture Graph Builder, or the DVD Graph Builder.</span></span> <span data-ttu-id="9de08-109">С точки зрения приложения они представляют собой один и тот же фильтр с одинаковыми интерфейсами и функциональными возможностями.</span><span class="sxs-lookup"><span data-stu-id="9de08-109">From an application perspective, they are the same filter, with the same interfaces and functionality.</span></span>

<span data-ttu-id="9de08-110">Следующая таблица содержит сведения, относящиеся к микшеру наложения 2.</span><span class="sxs-lookup"><span data-stu-id="9de08-110">The following table contains information specific to the Overlay Mixer 2.</span></span> <span data-ttu-id="9de08-111">Сведения о всех других данных фильтра см. в документации по микшеру наложения.</span><span class="sxs-lookup"><span data-stu-id="9de08-111">For all other filter data, refer to the documentation for the Overlay Mixer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9de08-112">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="9de08-112">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="9de08-113">Тип формата: Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="9de08-113">Format Type: Format_VIDEOINFO2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9de08-114">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="9de08-114">Filter CLSID</span></span></td>
<td><span data-ttu-id="9de08-115">CLSID_OverlayMixer2</span><span class="sxs-lookup"><span data-stu-id="9de08-115">CLSID_OverlayMixer2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9de08-116"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="9de08-116"><a href="merit.md">Merit</a></span></span></td>
<td><ul>
<li><span data-ttu-id="9de08-117">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="9de08-117">MERIT_UNLIKELY</span></span></li>
<li><span data-ttu-id="9de08-118">Windows Vista или более поздней версии: MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="9de08-118">Windows Vista or later: MERIT_DO_NOT_USE</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9de08-119">В Windows Vista или более поздней версии фильтр оверлея 2 не \_ \_ \_ используется, так как новые модули подготовки видео (VMR-7, VMR-9 и Евр) поддерживают форматы **VIDEOINFOHEADER2** , поэтому нет необходимости использовать микшер наложения.</span><span class="sxs-lookup"><span data-stu-id="9de08-119">In Windows Vista or later, the merit of the Overlay Mixer 2 filter is MERIT\_DO\_NOT\_USE, because the newer video renderers (VMR-7, VMR-9, and EVR) all support **VIDEOINFOHEADER2** formats, and therefore it is not necessary to use the Overlay Mixer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9de08-120">См. также</span><span class="sxs-lookup"><span data-stu-id="9de08-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9de08-121">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="9de08-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



