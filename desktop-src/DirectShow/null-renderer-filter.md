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
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908812"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="67a01-103">Фильтр визуализации null</span><span class="sxs-lookup"><span data-stu-id="67a01-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="67a01-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="67a01-104">\[Deprecated.</span></span> <span data-ttu-id="67a01-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67a01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67a01-106">Фильтр визуализации со значением NULL — это модуль подготовки отчетов, который удаляет каждый полученный пример, без отображения или отрисовки демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="67a01-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



| <span data-ttu-id="67a01-107">Метка</span><span class="sxs-lookup"><span data-stu-id="67a01-107">Label</span></span> | <span data-ttu-id="67a01-108">Значение</span><span class="sxs-lookup"><span data-stu-id="67a01-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a01-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="67a01-109">Filter interfaces</span></span>                        | <span data-ttu-id="67a01-110">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="67a01-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="67a01-111">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="67a01-111">Input pin media types</span></span>                    | <span data-ttu-id="67a01-112">Любой тип мультимедиа</span><span class="sxs-lookup"><span data-stu-id="67a01-112">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="67a01-113">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="67a01-113">Input pin interfaces</span></span>                     | <span data-ttu-id="67a01-114">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="67a01-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="67a01-115">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="67a01-115">Output pin media types</span></span>                   | <span data-ttu-id="67a01-116">Не применяется</span><span class="sxs-lookup"><span data-stu-id="67a01-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="67a01-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="67a01-117">Output pin interfaces</span></span>                    | <span data-ttu-id="67a01-118">Не применяется</span><span class="sxs-lookup"><span data-stu-id="67a01-118">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="67a01-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="67a01-119">Filter CLSID</span></span>                             | <span data-ttu-id="67a01-120">\_НУЛЛРЕНДЕРЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="67a01-120">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="67a01-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="67a01-121">Property Page CLSID</span></span>                      | <span data-ttu-id="67a01-122">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="67a01-122">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="67a01-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="67a01-123">Executable</span></span>                               | <span data-ttu-id="67a01-124">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="67a01-124">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="67a01-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="67a01-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="67a01-126">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="67a01-126">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="67a01-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="67a01-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="67a01-128">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="67a01-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="67a01-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67a01-129">Remarks</span></span>

<span data-ttu-id="67a01-130">Используйте этот фильтр, если для выходного контакта на графе требуется подчиненное соединение, но не требуется отображать данные из этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="67a01-130">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="67a01-131">Подключив выходной закрепление к модулю подготовки отчетов со значением NULL, вы завершите соединение без отображения данных.</span><span class="sxs-lookup"><span data-stu-id="67a01-131">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="67a01-132">Несмотря на то, что этот фильтр не отображает какие бы то ни было образцы, он ждет времени показа каждого примера перед отменой выборки.</span><span class="sxs-lookup"><span data-stu-id="67a01-132">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="67a01-133">Поэтому граф будет выполняться по нормальной ставке.</span><span class="sxs-lookup"><span data-stu-id="67a01-133">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="67a01-134">Если вы хотите, чтобы граф выполнялся как можно быстрее, установите для ссылочного времени **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="67a01-134">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="67a01-135">Дополнительные сведения см. [в разделе Установка часов графа](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="67a01-135">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67a01-136">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="67a01-136">Requirements</span></span>



| <span data-ttu-id="67a01-137">Требование</span><span class="sxs-lookup"><span data-stu-id="67a01-137">Requirement</span></span> | <span data-ttu-id="67a01-138">Значение</span><span class="sxs-lookup"><span data-stu-id="67a01-138">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67a01-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="67a01-139">Header</span></span><br/> | <dl> <span data-ttu-id="67a01-140"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="67a01-140"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a01-141">См. также</span><span class="sxs-lookup"><span data-stu-id="67a01-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a01-142">Объекты служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="67a01-142">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




