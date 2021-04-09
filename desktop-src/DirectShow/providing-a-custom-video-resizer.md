---
description: Предоставление пользовательского изменения размера видео
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Предоставление пользовательского изменения размера видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139723"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="54e20-103">Предоставление пользовательского изменения размера видео</span><span class="sxs-lookup"><span data-stu-id="54e20-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="54e20-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="54e20-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="54e20-105">Для этого компонента требуется DirectX 9,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="54e20-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="54e20-106">Когда [службы редактирования DirectShow](directshow-editing-services.md) (DES) изменяют размер исходного фрагмента видео, поведением по умолчанию является *стретчблт*, которое выполняется быстро, но не сглажено.</span><span class="sxs-lookup"><span data-stu-id="54e20-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="54e20-107">Поведение изменения размера можно изменить, реализовав пользовательский размер в качестве фильтра преобразования DirectShow.</span><span class="sxs-lookup"><span data-stu-id="54e20-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="54e20-108">Фильтр должен предоставлять интерфейс [**иресизе**](iresize.md) , который позволяет des указывать размер входного и выходного видео.</span><span class="sxs-lookup"><span data-stu-id="54e20-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="54e20-109">Дополнительные сведения о написании фильтра преобразования см. в разделе [написание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="54e20-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="54e20-110">В качестве отправной точки рекомендуется использовать базовый класс **ктрансформфилтер** .</span><span class="sxs-lookup"><span data-stu-id="54e20-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="54e20-111">При реализации фильтра Обратите внимание на следующее.</span><span class="sxs-lookup"><span data-stu-id="54e20-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="54e20-112">Поддержка интерфейса **иресизе** в фильтре (не на контактах).</span><span class="sxs-lookup"><span data-stu-id="54e20-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="54e20-113">Фильтр должен принимать только форматы [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ видеоинфо).</span><span class="sxs-lookup"><span data-stu-id="54e20-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="54e20-114">Отклоните другие типы форматов.</span><span class="sxs-lookup"><span data-stu-id="54e20-114">Reject other format types.</span></span>
-   <span data-ttu-id="54e20-115">Формат видео из DES может быть любым несжатым типом RGB, включая 32-разрядный RGB с альфа (МЕДИАСУБТИПЕ \_ ARGB32).</span><span class="sxs-lookup"><span data-stu-id="54e20-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="54e20-116">Фильтр может безопасно отклонять форматы с помощью **бихеигхт** < 0.</span><span class="sxs-lookup"><span data-stu-id="54e20-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="54e20-117">Перед тем как подсистема визуализации подключится к выходному закрепления фильтра, он вызывает [**иресизе::p UT \_ mediaType**](iresize-put-mediatype.md) для задания типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="54e20-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="54e20-118">Он также может вызывать [**иресизе::p UT \_ size**](iresize-put-size.md) для настройки размера выходных данных.</span><span class="sxs-lookup"><span data-stu-id="54e20-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="54e20-119">Он может вызывать эти два метода в любом порядке (любое количество раз) перед подключением выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="54e20-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="54e20-120">После того как подсистема визуализации подключится к выходному закреплениям, она может снова вызвать метод **вернуть \_ Размер** .</span><span class="sxs-lookup"><span data-stu-id="54e20-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="54e20-121">Фильтр изменения размера должен повторно подключить свой выходной ПИН-код с новым размером.</span><span class="sxs-lookup"><span data-stu-id="54e20-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="54e20-122">В методе [**ктрансформфилтер:: Transform**](ctransformfilter-transform.md) фильтра растяните входное видео на размер выходных данных.</span><span class="sxs-lookup"><span data-stu-id="54e20-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="54e20-123">Фильтр не должен задавать флаг небесперебойной работы в образце выходных данных или присоединять тип мультимедиа к образцу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="54e20-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="54e20-124">Чтобы сохранить состояние фильтра в файле Графедит (. ГРФ), реализуйте интерфейс **IPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="54e20-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="54e20-125">(Это необязательно, но полезно для тестирования.)</span><span class="sxs-lookup"><span data-stu-id="54e20-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="54e20-126">Чтобы использовать фильтр изменения, фильтр должен быть зарегистрирован в системе пользователя как COM-объект.</span><span class="sxs-lookup"><span data-stu-id="54e20-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="54e20-127">Прежде чем приложение отрисовывает видеопроект, запросите подсистему визуализации для интерфейса [**IRenderEngine2**](irenderengine2.md) и вызовите [**IRenderEngine2:: сетресизергуид**](irenderengine2-setresizerguid.md) с идентификатором CLSID фильтра изменения размера.</span><span class="sxs-lookup"><span data-stu-id="54e20-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54e20-128">См. также</span><span class="sxs-lookup"><span data-stu-id="54e20-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e20-129">Подготовка проекта</span><span class="sxs-lookup"><span data-stu-id="54e20-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



