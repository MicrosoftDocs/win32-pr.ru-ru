---
description: Интеллектуальный фильтр Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Интеллектуальный фильтр Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909302"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="2d19d-103">Интеллектуальный фильтр Tee</span><span class="sxs-lookup"><span data-stu-id="2d19d-103">Smart Tee Filter</span></span>

<span data-ttu-id="2d19d-104">Фильтр Smart tee используется в графах видеозаписи для разбиения видеопотока в поток предварительного просмотра и поток записи.</span><span class="sxs-lookup"><span data-stu-id="2d19d-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="2d19d-105">Это выполняется без дополнительных копирований данных.</span><span class="sxs-lookup"><span data-stu-id="2d19d-105">This is done without any additional data copying.</span></span> <span data-ttu-id="2d19d-106">Выходные контакты поддерживают любые типы мультимедиа, поддерживаемые в нисходящем соединении.</span><span class="sxs-lookup"><span data-stu-id="2d19d-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="2d19d-107">Фильтр Smart tee полезен, если фильтр видеозаписи не предоставляет отдельные ПИН-коды для записи и предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="2d19d-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="2d19d-108">Фильтр Smart tee доставляет данные предварительного просмотра только в том случае, если это не повредит производительность.</span><span class="sxs-lookup"><span data-stu-id="2d19d-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="2d19d-109">Он также удаляет метки времени из предварительной версии потока.</span><span class="sxs-lookup"><span data-stu-id="2d19d-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="2d19d-110">При необходимости построитель диаграмм для записи автоматически вставляет фильтр Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="2d19d-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="2d19d-111">Дополнительные сведения см. в разделе [объединение видеозаписей и предварительной версии](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="2d19d-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="2d19d-112">На следующем рисунке показан типичный граф записи, использующий фильтр Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="2d19d-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![Использование фильтра Smart Tee](images/smarttee.png)



| <span data-ttu-id="2d19d-114">Метка</span><span class="sxs-lookup"><span data-stu-id="2d19d-114">Label</span></span> | <span data-ttu-id="2d19d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2d19d-115">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d19d-116">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="2d19d-116">Filter Interfaces</span></span>                        | [<span data-ttu-id="2d19d-117">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="2d19d-117">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="2d19d-118">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="2d19d-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="2d19d-119">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="2d19d-119">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="2d19d-120">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="2d19d-120">Input Pin Interfaces</span></span>                     | <span data-ttu-id="2d19d-121">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2d19d-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="2d19d-122">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="2d19d-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="2d19d-123">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="2d19d-123">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="2d19d-124">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="2d19d-124">Output Pin Interfaces</span></span>                    | <span data-ttu-id="2d19d-125">[**Иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2d19d-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="2d19d-126">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="2d19d-126">Filter CLSID</span></span>                             | <span data-ttu-id="2d19d-127">\_СМАРТТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="2d19d-127">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="2d19d-128">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="2d19d-128">Property Page CLSID</span></span>                      | <span data-ttu-id="2d19d-129">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="2d19d-129">No property page.</span></span>                                                                                              |
| <span data-ttu-id="2d19d-130">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="2d19d-130">Executable</span></span>                               | <span data-ttu-id="2d19d-131">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="2d19d-131">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="2d19d-132">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="2d19d-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="2d19d-133">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="2d19d-133">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="2d19d-134">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="2d19d-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2d19d-135">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="2d19d-135">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="2d19d-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d19d-136">Remarks</span></span>

<span data-ttu-id="2d19d-137">ПИН-код записи является выходным закреплением 0, а предварительный ПИН-код — выходным закреплением 1.</span><span class="sxs-lookup"><span data-stu-id="2d19d-137">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d19d-138">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2d19d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d19d-139">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d19d-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



