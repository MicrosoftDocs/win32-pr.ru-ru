---
description: Фильтр визуализации со значением NULL — это модуль подготовки отчетов, который удаляет каждый полученный пример, без отображения или отрисовки демонстрационных данных.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Фильтр визуализации null (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689031"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="ef4fd-103">Фильтр визуализации null</span><span class="sxs-lookup"><span data-stu-id="ef4fd-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="ef4fd-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-104">\[Deprecated.</span></span> <span data-ttu-id="ef4fd-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef4fd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef4fd-106">Фильтр визуализации со значением NULL — это модуль подготовки отчетов, который удаляет каждый полученный пример, без отображения или отрисовки демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4fd-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="ef4fd-107">Filter interfaces</span></span>                        | <span data-ttu-id="ef4fd-108">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="ef4fd-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="ef4fd-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="ef4fd-109">Input pin media types</span></span>                    | <span data-ttu-id="ef4fd-110">Любой тип мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ef4fd-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="ef4fd-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="ef4fd-111">Input pin interfaces</span></span>                     | <span data-ttu-id="ef4fd-112">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ef4fd-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="ef4fd-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="ef4fd-113">Output pin media types</span></span>                   | <span data-ttu-id="ef4fd-114">Не применяется</span><span class="sxs-lookup"><span data-stu-id="ef4fd-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="ef4fd-115">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="ef4fd-115">Output pin interfaces</span></span>                    | <span data-ttu-id="ef4fd-116">Не применяется</span><span class="sxs-lookup"><span data-stu-id="ef4fd-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="ef4fd-117">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="ef4fd-117">Filter CLSID</span></span>                             | <span data-ttu-id="ef4fd-118">\_НУЛЛРЕНДЕРЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="ef4fd-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="ef4fd-119">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="ef4fd-119">Property Page CLSID</span></span>                      | <span data-ttu-id="ef4fd-120">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="ef4fd-121">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="ef4fd-121">Executable</span></span>                               | <span data-ttu-id="ef4fd-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="ef4fd-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="ef4fd-123">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="ef4fd-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="ef4fd-124">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="ef4fd-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="ef4fd-125">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="ef4fd-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ef4fd-126">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="ef4fd-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="ef4fd-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef4fd-127">Remarks</span></span>

<span data-ttu-id="ef4fd-128">Используйте этот фильтр, если для выходного контакта на графе требуется подчиненное соединение, но не требуется отображать данные из этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="ef4fd-129">Подключив выходной закрепление к модулю подготовки отчетов со значением NULL, вы завершите соединение без отображения данных.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="ef4fd-130">Несмотря на то, что этот фильтр не отображает какие бы то ни было образцы, он ждет времени показа каждого примера перед отменой выборки.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="ef4fd-131">Поэтому граф будет выполняться по нормальной ставке.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="ef4fd-132">Если вы хотите, чтобы граф выполнялся как можно быстрее, установите для ссылочного времени **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ef4fd-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="ef4fd-133">Дополнительные сведения см. [в разделе Установка часов графа](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="ef4fd-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4fd-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ef4fd-134">Requirements</span></span>



| <span data-ttu-id="ef4fd-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ef4fd-135">Requirement</span></span> | <span data-ttu-id="ef4fd-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ef4fd-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4fd-137">Header</span><span class="sxs-lookup"><span data-stu-id="ef4fd-137">Header</span></span><br/> | <dl> <span data-ttu-id="ef4fd-138"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4fd-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef4fd-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef4fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4fd-140">Объекты служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="ef4fd-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




