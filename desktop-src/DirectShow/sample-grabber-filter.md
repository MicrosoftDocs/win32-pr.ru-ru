---
description: Образец фильтра захвата позволяет извлекать образцы по мере их прохождения через граф фильтра.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Образец фильтра захвата (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909672"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="67d46-103">Образец фильтра захвата</span><span class="sxs-lookup"><span data-stu-id="67d46-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="67d46-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="67d46-104">\[Deprecated.</span></span> <span data-ttu-id="67d46-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67d46-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67d46-106">Образец фильтра захвата позволяет извлекать образцы по мере их прохождения через граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="67d46-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="67d46-107">Это фильтр преобразования с одним входным закреплением и одним выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="67d46-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="67d46-108">Он передает все образцы в неизменном виде, поэтому его можно вставить в граф фильтра, не изменяя поток данных.</span><span class="sxs-lookup"><span data-stu-id="67d46-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="67d46-109">Приложение может получить отдельные образцы из фильтра, вызвав методы в интерфейсе [**исамплеграббер**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="67d46-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="67d46-110">Если вы хотите получить образцы без подготовки данных к просмотру, подключите образец фильтра захвата к фильтру модуля [**подготовки отчетов со значением NULL**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="67d46-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="67d46-111">Метка</span><span class="sxs-lookup"><span data-stu-id="67d46-111">Label</span></span> | <span data-ttu-id="67d46-112">Значение</span><span class="sxs-lookup"><span data-stu-id="67d46-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67d46-113">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="67d46-113">Filter interfaces</span></span>                        | <span data-ttu-id="67d46-114">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **исамплеграббер**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="67d46-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="67d46-115">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="67d46-115">Input pin media types</span></span>                    | <span data-ttu-id="67d46-116">Любой тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="67d46-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="67d46-117">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="67d46-117">Input pin interfaces</span></span>                     | <span data-ttu-id="67d46-118">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="67d46-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="67d46-119">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="67d46-119">Output pin media types</span></span>                   | <span data-ttu-id="67d46-120">Любой тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="67d46-120">Any media type.</span></span> <span data-ttu-id="67d46-121">Соответствует входному типу носителя.</span><span class="sxs-lookup"><span data-stu-id="67d46-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="67d46-122">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="67d46-122">Output pin interfaces</span></span>                    | <span data-ttu-id="67d46-123">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="67d46-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="67d46-124">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="67d46-124">Filter CLSID</span></span>                             | <span data-ttu-id="67d46-125">\_САМПЛЕГРАББЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="67d46-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="67d46-126">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="67d46-126">Property Page CLSID</span></span>                      | <span data-ttu-id="67d46-127">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="67d46-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="67d46-128">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="67d46-128">Executable</span></span>                               | <span data-ttu-id="67d46-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="67d46-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="67d46-130">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="67d46-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="67d46-131">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="67d46-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="67d46-132">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="67d46-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="67d46-133">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="67d46-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="67d46-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67d46-134">Remarks</span></span>

<span data-ttu-id="67d46-135">Чтобы использовать этот фильтр, добавьте его в граф фильтра и вызовите [**исамплеграббер:: сетмедиатипе**](isamplegrabber-setmediatype.md) с нужным типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="67d46-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="67d46-136">Этот метод указывает тип носителя для соединений входного и выходного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="67d46-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="67d46-137">Затем подключите фильтр к другим фильтрам в графе.</span><span class="sxs-lookup"><span data-stu-id="67d46-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="67d46-138">При вызове [**исамплеграббер:: сетбуфферсамплес**](isamplegrabber-setbuffersamples.md) со значением **true** фильтр помещает каждый пример, который он получает, перед передачей его нисходящим.</span><span class="sxs-lookup"><span data-stu-id="67d46-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="67d46-139">Вызовите метод [**исамплеграббер:: жеткуррентбуффер**](isamplegrabber-getcurrentbuffer.md) , чтобы получить текущее содержимое буфера.</span><span class="sxs-lookup"><span data-stu-id="67d46-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="67d46-140">Кроме того, можно вызвать [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md) , чтобы фильтр вызывал функцию обратного вызова при получении примера.</span><span class="sxs-lookup"><span data-stu-id="67d46-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="67d46-141">Фильтр имеет следующие ограничения для форматов видео:</span><span class="sxs-lookup"><span data-stu-id="67d46-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="67d46-142">Он не поддерживает типы видео с ориентацией сверху вниз (отрицательное **бихеигхт**).</span><span class="sxs-lookup"><span data-stu-id="67d46-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="67d46-143">Он не поддерживает структуру формата [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (тип формата, равный **Format \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="67d46-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="67d46-144">Он отклоняет любой тип видео, где шаг поверхности не соответствует ширине видео.</span><span class="sxs-lookup"><span data-stu-id="67d46-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="67d46-145">В результате этот образец захвата не будет подключаться к модулю прорисовки видео (VMR) для некоторых типов видео.</span><span class="sxs-lookup"><span data-stu-id="67d46-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d46-146">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="67d46-146">Requirements</span></span>



| <span data-ttu-id="67d46-147">Требование</span><span class="sxs-lookup"><span data-stu-id="67d46-147">Requirement</span></span> | <span data-ttu-id="67d46-148">Значение</span><span class="sxs-lookup"><span data-stu-id="67d46-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67d46-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="67d46-149">Header</span></span><br/> | <dl> <span data-ttu-id="67d46-150"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d46-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d46-151">См. также</span><span class="sxs-lookup"><span data-stu-id="67d46-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d46-152">Объекты служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="67d46-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="67d46-153">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="67d46-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




