---
description: Указывает, предоставляет ли декодер выходные типы ИЙУВ/I420 (подходящие для перекодирования) перед другими форматами.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Атрибут MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812610"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="ab3d1-103">\_Декодер MFT \_ предоставляют \_ выходные \_ типы \_ в \_ \_ атрибуте собственного порядка</span><span class="sxs-lookup"><span data-stu-id="ab3d1-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="ab3d1-104">Указывает, предоставляет ли декодер выходные типы ИЙУВ/I420 (подходящие для перекодирования) перед другими форматами.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="ab3d1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ab3d1-105">Data type</span></span>

<span data-ttu-id="ab3d1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ab3d1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ab3d1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab3d1-107">Remarks</span></span>

<span data-ttu-id="ab3d1-108">Этот атрибут является указанием для декодера, чтобы упорядочить список типов вывода в определенном порядке, в зависимости от предполагаемого использования: воспроизведение или перекодировать.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="ab3d1-109">Для большинства форматов кодирования (H. 264, MPEG-2, WMV) видеодекодеры в Microsoft Media Foundation поддерживают несколько распространенных выходных данных YUV, включая NV12, YV12, YUY2, ИЙУВ и I420.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="ab3d1-110">Декодер предлагает упорядоченный список типов выходных данных с помощью метода [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .</span><span class="sxs-lookup"><span data-stu-id="ab3d1-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="ab3d1-111">Для воспроизведения NV12 является наиболее эффективным и широко поддерживаемым форматом.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="ab3d1-112">Таким образом, по умолчанию декодеры обычно предлагают NV12 в качестве первого выходного типа в списке.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="ab3d1-113">Это уменьшает время, необходимое для разрешения типа носителя при создании топологии воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="ab3d1-114">Однако для перекодировки ИЙУВ или I420 более эффективны для ЦП и обычно предпочтительны кодировщиками.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="ab3d1-115">Если декодер поддерживает этот атрибут, то атрибут имеет следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="ab3d1-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="ab3d1-116">Если атрибут имеет ненулевое значение, ИЙУВ и I420 отображаются первым в списке типов выходных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="ab3d1-117">Этот параметр наиболее эффективен для перекодирования.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="ab3d1-118">Если атрибут равен нулю, NV12 отображается первым в списке типов выходных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="ab3d1-119">Этот параметр наиболее эффективен для воспроизведения и является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="ab3d1-120">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ab3d1-120">To set this attribute:</span></span>

1.  <span data-ttu-id="ab3d1-121">Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ab3d1-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="ab3d1-122">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) , чтобы добавить атрибут.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab3d1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ab3d1-123">Requirements</span></span>



| <span data-ttu-id="ab3d1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ab3d1-124">Requirement</span></span> | <span data-ttu-id="ab3d1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ab3d1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3d1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab3d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ab3d1-127">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="ab3d1-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ab3d1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab3d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ab3d1-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ab3d1-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ab3d1-130">Header</span><span class="sxs-lookup"><span data-stu-id="ab3d1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab3d1-131"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d1-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab3d1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab3d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab3d1-133">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab3d1-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




