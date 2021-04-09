---
description: Фильтр VGA 16 с оттенокм
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Фильтр VGA 16 с оттенокм
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081083"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="6625a-103">Фильтр VGA 16 с оттенокм</span><span class="sxs-lookup"><span data-stu-id="6625a-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="6625a-104">Фильтр VGA 16, отменяющий цвет, выполняет преобразование из типа цвета RGB в 4-разрядный цвет, чтобы видеопотоки AVI и MPEG могли отображаться на старых 16 цветных мониторах.</span><span class="sxs-lookup"><span data-stu-id="6625a-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="6625a-105">Этот фильтр вставляется в граф между фильтром декомпрессора и фильтром модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="6625a-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6625a-106">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="6625a-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="6625a-107">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="6625a-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="6625a-108">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="6625a-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="6625a-109">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="6625a-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="6625a-110">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="6625a-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="6625a-111">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6625a-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="6625a-112">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="6625a-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="6625a-113">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="6625a-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="6625a-114">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="6625a-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="6625a-115">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6625a-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="6625a-116">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="6625a-116">Filter CLSID</span></span>                             | <span data-ttu-id="6625a-117">\_ДИЗЕРИНГ CLSID</span><span class="sxs-lookup"><span data-stu-id="6625a-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="6625a-118">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="6625a-118">Property Page CLSID</span></span>                      | <span data-ttu-id="6625a-119">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="6625a-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="6625a-120">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="6625a-120">Executable</span></span>                               | <span data-ttu-id="6625a-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6625a-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="6625a-122">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6625a-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="6625a-123">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="6625a-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="6625a-124">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="6625a-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="6625a-125">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="6625a-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6625a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6625a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6625a-127">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="6625a-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



