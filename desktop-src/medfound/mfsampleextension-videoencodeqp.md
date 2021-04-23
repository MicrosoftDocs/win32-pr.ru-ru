---
description: Указывает параметр дискретизация (QP), который использовался для кодирования примера видео.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Атрибут MFSampleExtension_VideoEncodeQP (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711701"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="8a859-103">Мфсампликстенсион \_ видеоенкодекп, атрибут</span><span class="sxs-lookup"><span data-stu-id="8a859-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="8a859-104">Указывает параметр дискретизация (QP), который использовался для кодирования примера видео.</span><span class="sxs-lookup"><span data-stu-id="8a859-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a859-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8a859-105">Data type</span></span>

<span data-ttu-id="8a859-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="8a859-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="8a859-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="8a859-107">Get/set</span></span>

<span data-ttu-id="8a859-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="8a859-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="8a859-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="8a859-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8a859-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="8a859-110">Applies to</span></span>

[<span data-ttu-id="8a859-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="8a859-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="8a859-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a859-112">Remarks</span></span>

<span data-ttu-id="8a859-113">[**Кодировщик видео H. 264**](h-264-video-encoder.md) устанавливает этот атрибут для создаваемых результирующих примеров.</span><span class="sxs-lookup"><span data-stu-id="8a859-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a859-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8a859-114">Requirements</span></span>



| <span data-ttu-id="8a859-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8a859-115">Requirement</span></span> | <span data-ttu-id="8a859-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8a859-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a859-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a859-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8a859-118">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="8a859-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8a859-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a859-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8a859-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a859-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8a859-121">Header</span><span class="sxs-lookup"><span data-stu-id="8a859-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a859-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a859-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a859-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a859-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a859-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a859-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a859-125">**Кодировщик видео H. 264**</span><span class="sxs-lookup"><span data-stu-id="8a859-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="8a859-126">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="8a859-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a859-127">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="8a859-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




