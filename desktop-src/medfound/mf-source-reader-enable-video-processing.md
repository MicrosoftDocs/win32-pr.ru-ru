---
description: Включает обработку видео модулем чтения исходного кода.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Атрибут MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497358"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="e5d10-103">MF \_ source \_ Reader \_ Включение \_ \_ атрибута обработки видео</span><span class="sxs-lookup"><span data-stu-id="e5d10-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="e5d10-104">Включает обработку видео [модулем чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="e5d10-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="e5d10-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e5d10-105">Data type</span></span>

<span data-ttu-id="e5d10-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e5d10-106">**UINT32**</span></span>



| <span data-ttu-id="e5d10-107">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d10-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="e5d10-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d10-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="e5d10-109"><dt>**Отличные**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d10-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="e5d10-110">Включить обработку видео.</span><span class="sxs-lookup"><span data-stu-id="e5d10-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="e5d10-111"><dt>**Ноль**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d10-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="e5d10-112">Отключить обработку видео.</span><span class="sxs-lookup"><span data-stu-id="e5d10-112">Disable video processing.</span></span> <span data-ttu-id="e5d10-113">(по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5d10-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="e5d10-114">Get/Set</span><span class="sxs-lookup"><span data-stu-id="e5d10-114">Get/set</span></span>

<span data-ttu-id="e5d10-115">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e5d10-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e5d10-116">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e5d10-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5d10-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5d10-117">Remarks</span></span>

<span data-ttu-id="e5d10-118">Если этот атрибут имеет **значение true** (отличное от нуля), модуль чтения исходного кода может выполнять следующую ограниченную обработку видео для несжатых видеокадров:</span><span class="sxs-lookup"><span data-stu-id="e5d10-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="e5d10-119">Преобразование из YUV в RGB-32.</span><span class="sxs-lookup"><span data-stu-id="e5d10-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="e5d10-120">Деинтерлейсинга.</span><span class="sxs-lookup"><span data-stu-id="e5d10-120">Deinterlacing.</span></span>

<span data-ttu-id="e5d10-121">Эти операции выполняются в программном обеспечении и не оптимизируются для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e5d10-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="e5d10-122">Эта функция предназначена для приложений, которые обрабатывают небольшое количество кадров, например для создания эскиза видео, или для приложений, которые не декодируются кадры в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="e5d10-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="e5d10-123">Операция чередования выполняет интерполяцию данных из одного поля, поэтому они теряются.</span><span class="sxs-lookup"><span data-stu-id="e5d10-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="e5d10-124">Избегайте этого параметра, если вы используете Direct3D для показа видеокадров, так как GPU обычно предоставляет лучшие возможности обработки видео.</span><span class="sxs-lookup"><span data-stu-id="e5d10-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="e5d10-125">Если этот атрибут имеет **значение true**, следующие атрибуты должны иметь **значение false**:</span><span class="sxs-lookup"><span data-stu-id="e5d10-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="e5d10-126">\_ \_ \_ Диспетчер D3D чтения источника \_ MF</span><span class="sxs-lookup"><span data-stu-id="e5d10-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="e5d10-127">\_ \_ запретить \_ конвертеры MF ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e5d10-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="e5d10-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e5d10-128">Requirements</span></span>



| <span data-ttu-id="e5d10-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e5d10-129">Requirement</span></span> | <span data-ttu-id="e5d10-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d10-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d10-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5d10-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d10-132">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="e5d10-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e5d10-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5d10-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d10-134">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e5d10-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e5d10-135">Header</span><span class="sxs-lookup"><span data-stu-id="e5d10-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d10-136"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d10-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d10-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5d10-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d10-138">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5d10-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e5d10-139">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="e5d10-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="e5d10-140">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="e5d10-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




