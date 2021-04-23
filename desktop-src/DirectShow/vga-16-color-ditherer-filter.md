---
description: Фильтр VGA 16 с оттенокм
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Фильтр VGA 16 с оттенокм
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908682"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="f82b5-103">Фильтр VGA 16 с оттенокм</span><span class="sxs-lookup"><span data-stu-id="f82b5-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="f82b5-104">Фильтр VGA 16, отменяющий цвет, выполняет преобразование из типа цвета RGB в 4-разрядный цвет, чтобы видеопотоки AVI и MPEG могли отображаться на старых 16 цветных мониторах.</span><span class="sxs-lookup"><span data-stu-id="f82b5-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="f82b5-105">Этот фильтр вставляется в граф между фильтром декомпрессора и фильтром модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="f82b5-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="f82b5-106">Метка</span><span class="sxs-lookup"><span data-stu-id="f82b5-106">Label</span></span> | <span data-ttu-id="f82b5-107">Значение</span><span class="sxs-lookup"><span data-stu-id="f82b5-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f82b5-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="f82b5-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="f82b5-109">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="f82b5-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="f82b5-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="f82b5-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="f82b5-111">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="f82b5-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="f82b5-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="f82b5-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f82b5-113">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f82b5-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="f82b5-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="f82b5-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="f82b5-115">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="f82b5-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="f82b5-116">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="f82b5-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f82b5-117">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f82b5-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="f82b5-118">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="f82b5-118">Filter CLSID</span></span>                             | <span data-ttu-id="f82b5-119">\_ДИЗЕРИНГ CLSID</span><span class="sxs-lookup"><span data-stu-id="f82b5-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="f82b5-120">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="f82b5-120">Property Page CLSID</span></span>                      | <span data-ttu-id="f82b5-121">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f82b5-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="f82b5-122">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="f82b5-122">Executable</span></span>                               | <span data-ttu-id="f82b5-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f82b5-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="f82b5-124">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="f82b5-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="f82b5-125">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="f82b5-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="f82b5-126">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="f82b5-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f82b5-127">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="f82b5-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="f82b5-128">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f82b5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f82b5-129">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="f82b5-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



