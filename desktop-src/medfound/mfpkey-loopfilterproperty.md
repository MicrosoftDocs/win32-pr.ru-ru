---
description: Указывает, должен ли кодек использовать фильтр для деблокировки в процессе кодирования.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Свойство MFPKEY_LOOPFILTER (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692848"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="5e6a8-103">МФПКЭЙ \_ лупфилтер, свойство</span><span class="sxs-lookup"><span data-stu-id="5e6a8-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="5e6a8-104">Указывает, должен ли кодек использовать фильтр для деблокировки в процессе кодирования.</span><span class="sxs-lookup"><span data-stu-id="5e6a8-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5e6a8-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="5e6a8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5e6a8-106">g \_ всзвмвклупфилтер</span><span class="sxs-lookup"><span data-stu-id="5e6a8-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="5e6a8-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5e6a8-107">Data Type</span></span>

<span data-ttu-id="5e6a8-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="5e6a8-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6a8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e6a8-109">Remarks</span></span>

<span data-ttu-id="5e6a8-110">Фильтр в цикле является разблокирующим методом, который применяется во время кодирования и декодирования, чтобы сократить количество блокирующих артефактов во время кодирования ("в цикле"), чтобы будущие кадры P-и B-Frame не перенаправлялись.</span><span class="sxs-lookup"><span data-stu-id="5e6a8-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="5e6a8-111">Результатом применения фильтра в цикле является то, что края блоков макросов в выходных видеокадрах менее заметны.</span><span class="sxs-lookup"><span data-stu-id="5e6a8-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="5e6a8-112">В то же время изображение может стать более мягким в внешнем виде.</span><span class="sxs-lookup"><span data-stu-id="5e6a8-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="5e6a8-113">Хотя фильтр в цикле может привести к уменьшению детализации изображения в некоторых кадрах, общее качество видео будет существенно выгодно.</span><span class="sxs-lookup"><span data-stu-id="5e6a8-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="5e6a8-114">Самым большим недостатком использования фильтрации в цикле являются дополнительные затраты на производительность декодирования.</span><span class="sxs-lookup"><span data-stu-id="5e6a8-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e6a8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5e6a8-115">Requirements</span></span>



| <span data-ttu-id="5e6a8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5e6a8-116">Requirement</span></span> | <span data-ttu-id="5e6a8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5e6a8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6a8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e6a8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5e6a8-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5e6a8-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5e6a8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e6a8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5e6a8-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e6a8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e6a8-122">Header</span><span class="sxs-lookup"><span data-stu-id="5e6a8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e6a8-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e6a8-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e6a8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e6a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6a8-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e6a8-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




