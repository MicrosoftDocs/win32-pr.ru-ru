---
description: Задает окончательное разрешение вывода декодированного изображения после обработки видео.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Атрибут MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263515"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="02b8b-103">\_Атрибут указания \_ конечного \_ \_ разрешения \_ экрана декодера MFT</span><span class="sxs-lookup"><span data-stu-id="02b8b-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="02b8b-104">Задает окончательное разрешение вывода декодированного изображения после обработки видео.</span><span class="sxs-lookup"><span data-stu-id="02b8b-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="02b8b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="02b8b-105">Data type</span></span>

<span data-ttu-id="02b8b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="02b8b-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="02b8b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02b8b-107">Remarks</span></span>

<span data-ttu-id="02b8b-108">Этот атрибут поддерживается некоторыми декодерами видео.</span><span class="sxs-lookup"><span data-stu-id="02b8b-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="02b8b-109">Приложение может установить этот атрибут, чтобы указать ширину и высоту изображения после обработки видео.</span><span class="sxs-lookup"><span data-stu-id="02b8b-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="02b8b-110">Декодер может использовать эти сведения для оптимизации процесса декодирования, особенно в том случае, если окончательный размер изображения намного меньше, чем размер образа в машинном коде.</span><span class="sxs-lookup"><span data-stu-id="02b8b-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="02b8b-111">Например, декодер может пропустить фильтр по внешнему циклу.</span><span class="sxs-lookup"><span data-stu-id="02b8b-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="02b8b-112">Верхние 32 разрядов содержат ширину, а более низкие биты 32 содержат высоту.</span><span class="sxs-lookup"><span data-stu-id="02b8b-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="02b8b-113">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="02b8b-113">To set this attribute:</span></span>

1.  <span data-ttu-id="02b8b-114">Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="02b8b-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="02b8b-115">Вызовите [**мфсетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) , чтобы добавить атрибут.</span><span class="sxs-lookup"><span data-stu-id="02b8b-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b8b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="02b8b-116">Requirements</span></span>



| <span data-ttu-id="02b8b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="02b8b-117">Requirement</span></span> | <span data-ttu-id="02b8b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="02b8b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b8b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02b8b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="02b8b-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="02b8b-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="02b8b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02b8b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="02b8b-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="02b8b-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="02b8b-123">Header</span><span class="sxs-lookup"><span data-stu-id="02b8b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b8b-124"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="02b8b-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b8b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02b8b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b8b-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02b8b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02b8b-127">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="02b8b-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




