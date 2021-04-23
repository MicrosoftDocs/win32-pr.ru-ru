---
description: Указывает тип изображения, выводимого кодировщиком видео.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Атрибут MFSampleExtension_VideoEncodePictureType (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683080"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="01238-103">Мфсампликстенсион \_ видеоенкодепиктуретипе, атрибут</span><span class="sxs-lookup"><span data-stu-id="01238-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="01238-104">Указывает тип изображения, выводимого кодировщиком видео.</span><span class="sxs-lookup"><span data-stu-id="01238-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="01238-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="01238-105">Data type</span></span>

<span data-ttu-id="01238-106">**eAVEncH264PictureType \_ Б** хранится как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="01238-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="01238-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="01238-107">Get/set</span></span>

<span data-ttu-id="01238-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="01238-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="01238-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="01238-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="01238-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="01238-110">Applies to</span></span>

[<span data-ttu-id="01238-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="01238-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="01238-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01238-112">Remarks</span></span>

<span data-ttu-id="01238-113">[**Кодировщик видео H. 264**](h-264-video-encoder.md) устанавливает этот атрибут для создаваемых результирующих примеров.</span><span class="sxs-lookup"><span data-stu-id="01238-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="01238-114">Значение атрибута является членом перечисления [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .</span><span class="sxs-lookup"><span data-stu-id="01238-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="01238-115">Требования</span><span class="sxs-lookup"><span data-stu-id="01238-115">Requirements</span></span>



| <span data-ttu-id="01238-116">Требование</span><span class="sxs-lookup"><span data-stu-id="01238-116">Requirement</span></span> | <span data-ttu-id="01238-117">Значение</span><span class="sxs-lookup"><span data-stu-id="01238-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01238-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01238-118">Minimum supported client</span></span><br/> | <span data-ttu-id="01238-119">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="01238-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="01238-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01238-120">Minimum supported server</span></span><br/> | <span data-ttu-id="01238-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="01238-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="01238-122">Header</span><span class="sxs-lookup"><span data-stu-id="01238-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="01238-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="01238-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01238-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01238-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01238-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01238-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01238-126">**Кодировщик видео H. 264**</span><span class="sxs-lookup"><span data-stu-id="01238-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="01238-127">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="01238-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="01238-128">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="01238-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




