---
description: Интеллектуальный фильтр Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Интеллектуальный фильтр Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495477"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="091b4-103">Интеллектуальный фильтр Tee</span><span class="sxs-lookup"><span data-stu-id="091b4-103">Smart Tee Filter</span></span>

<span data-ttu-id="091b4-104">Фильтр Smart tee используется в графах видеозаписи для разбиения видеопотока в поток предварительного просмотра и поток записи.</span><span class="sxs-lookup"><span data-stu-id="091b4-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="091b4-105">Это выполняется без дополнительных копирований данных.</span><span class="sxs-lookup"><span data-stu-id="091b4-105">This is done without any additional data copying.</span></span> <span data-ttu-id="091b4-106">Выходные контакты поддерживают любые типы мультимедиа, поддерживаемые в нисходящем соединении.</span><span class="sxs-lookup"><span data-stu-id="091b4-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="091b4-107">Фильтр Smart tee полезен, если фильтр видеозаписи не предоставляет отдельные ПИН-коды для записи и предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="091b4-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="091b4-108">Фильтр Smart tee доставляет данные предварительного просмотра только в том случае, если это не повредит производительность.</span><span class="sxs-lookup"><span data-stu-id="091b4-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="091b4-109">Он также удаляет метки времени из предварительной версии потока.</span><span class="sxs-lookup"><span data-stu-id="091b4-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="091b4-110">При необходимости построитель диаграмм для записи автоматически вставляет фильтр Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="091b4-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="091b4-111">Дополнительные сведения см. в разделе [объединение видеозаписей и предварительной версии](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="091b4-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="091b4-112">На следующем рисунке показан типичный граф записи, использующий фильтр Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="091b4-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![Использование фильтра Smart Tee](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="091b4-114">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="091b4-114">Filter Interfaces</span></span>                        | [<span data-ttu-id="091b4-115">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="091b4-115">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="091b4-116">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="091b4-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="091b4-117">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="091b4-117">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="091b4-118">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="091b4-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="091b4-119">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="091b4-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="091b4-120">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="091b4-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="091b4-121">\_Устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="091b4-121">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="091b4-122">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="091b4-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="091b4-123">[**Иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="091b4-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="091b4-124">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="091b4-124">Filter CLSID</span></span>                             | <span data-ttu-id="091b4-125">\_СМАРТТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="091b4-125">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="091b4-126">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="091b4-126">Property Page CLSID</span></span>                      | <span data-ttu-id="091b4-127">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="091b4-127">No property page.</span></span>                                                                                              |
| <span data-ttu-id="091b4-128">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="091b4-128">Executable</span></span>                               | <span data-ttu-id="091b4-129">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="091b4-129">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="091b4-130">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="091b4-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="091b4-131">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="091b4-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="091b4-132">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="091b4-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="091b4-133">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="091b4-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="091b4-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="091b4-134">Remarks</span></span>

<span data-ttu-id="091b4-135">ПИН-код записи является выходным закреплением 0, а предварительный ПИН-код — выходным закреплением 1.</span><span class="sxs-lookup"><span data-stu-id="091b4-135">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="091b4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="091b4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="091b4-137">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="091b4-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



