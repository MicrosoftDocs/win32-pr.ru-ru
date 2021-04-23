---
description: Включает расширенную обработку видео модулем чтения исходного кода, включая преобразование цветового пространства, дечередование, изменение размера видео и преобразование кадрового потока.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Атрибут MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541354"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="13a1d-103">MF \_ исходный \_ считыватель \_ включить \_ Расширенный \_ \_ атрибут обработки видео</span><span class="sxs-lookup"><span data-stu-id="13a1d-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="13a1d-104">Включает расширенную обработку видео [модулем чтения исходного кода](source-reader.md), включая преобразование цветового пространства, дечередование, изменение размера видео и преобразование кадрового потока.</span><span class="sxs-lookup"><span data-stu-id="13a1d-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="13a1d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="13a1d-105">Data type</span></span>

<span data-ttu-id="13a1d-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="13a1d-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="13a1d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13a1d-107">Remarks</span></span>

<span data-ttu-id="13a1d-108">Если этот атрибут имеет **значение true**, модуль чтения исходного кода может вставлять обработчик видео в конвейер обработки, что позволяет выполнять следующие типы преобразования форматов:</span><span class="sxs-lookup"><span data-stu-id="13a1d-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="13a1d-109">Преобразование цветового пространства (YUV в RGB-32)</span><span class="sxs-lookup"><span data-stu-id="13a1d-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="13a1d-110">Деинтерлейсинга</span><span class="sxs-lookup"><span data-stu-id="13a1d-110">Deinterlacing</span></span>
-   <span data-ttu-id="13a1d-111">Изменение размера видео</span><span class="sxs-lookup"><span data-stu-id="13a1d-111">Video resizing</span></span>
-   <span data-ttu-id="13a1d-112">Преобразование частоты кадров</span><span class="sxs-lookup"><span data-stu-id="13a1d-112">Frame-rate conversion</span></span>

<span data-ttu-id="13a1d-113">Если этот атрибут имеет **значение true**, [то \_ \_ Отключить \_ преобразователи](mf-readwrite-disable-converters.md) с помощью атрибута "Disable ReadWrite" должно быть **значение false**.</span><span class="sxs-lookup"><span data-stu-id="13a1d-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="13a1d-114">Модуль чтения исходного кода ищет видеопроцессоры, зарегистрированные в **категории \_ основной \_ \_ видеопроцессор категории MFT** , включая МФТС, зарегистрированные для локального процесса.</span><span class="sxs-lookup"><span data-stu-id="13a1d-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="13a1d-115">(Дополнительные сведения о локальной регистрации МФТС см. в разделе [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) .) Модуль чтения исходного кода использует обработчик видео перекодирования (КСВП), если не найден другой подходящий обработчик видео.</span><span class="sxs-lookup"><span data-stu-id="13a1d-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="13a1d-116">Приложение указывает требуемый тип выходных данных путем вызова [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="13a1d-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="13a1d-117">Когда модуль чтения исходного кода настраивает обработчик видео, он пытается сопоставить следующие атрибуты типа выходных данных:</span><span class="sxs-lookup"><span data-stu-id="13a1d-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="13a1d-118">Частота кадров ([MF \_ - \_ \_ Частота кадров](mf-mt-frame-rate-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="13a1d-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="13a1d-119">Размер кадра ([MF \_ - \_ \_ Формат кадра](mf-mt-frame-size-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="13a1d-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="13a1d-120">Режим с чередованием ([MF \_ MT, \_ \_ режим чередования](mf-mt-interlace-mode-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="13a1d-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="13a1d-121">Пропорция в пикселях (пропорции[MF в \_ \_ пикселях \_ \_ ](mf-mt-pixel-aspect-ratio-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="13a1d-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="13a1d-122">Подтип ([MF \_ MT \_ подтипа](mf-mt-subtype-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="13a1d-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="13a1d-123">Этот атрибут подобен [ \_ модулю считывания исходного кода MF, который \_ \_ включает атрибут \_ \_ обработки видео](mf-source-reader-enable-video-processing.md) , но предоставляет следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="13a1d-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="13a1d-124">Поддерживается больший диапазон преобразований формата.</span><span class="sxs-lookup"><span data-stu-id="13a1d-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="13a1d-125">Приложения могут регистрировать собственные преобразователи.</span><span class="sxs-lookup"><span data-stu-id="13a1d-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="13a1d-126">Некоторые преобразования могут выполняться на оборудовании с помощью GPU.</span><span class="sxs-lookup"><span data-stu-id="13a1d-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a1d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="13a1d-127">Requirements</span></span>



| <span data-ttu-id="13a1d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="13a1d-128">Requirement</span></span> | <span data-ttu-id="13a1d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="13a1d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a1d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13a1d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13a1d-131">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="13a1d-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="13a1d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13a1d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13a1d-133">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="13a1d-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="13a1d-134">Header</span><span class="sxs-lookup"><span data-stu-id="13a1d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a1d-135"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a1d-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a1d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13a1d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a1d-137">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13a1d-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="13a1d-138">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="13a1d-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="13a1d-139">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="13a1d-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




