---
description: Частота кадров типа видеоклипа в кадрах в секунду.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Атрибут MF_MT_FRAME_RATE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423990"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="07c9f-103">\_ \_ Атрибут частоты кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="07c9f-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="07c9f-104">Частота кадров типа видеоклипа в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="07c9f-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="07c9f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="07c9f-105">Data type</span></span>

<span data-ttu-id="07c9f-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="07c9f-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="07c9f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07c9f-107">Remarks</span></span>

<span data-ttu-id="07c9f-108">Частота кадров выражается в виде коэффициента.</span><span class="sxs-lookup"><span data-stu-id="07c9f-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="07c9f-109">Верхний 32 бит значения атрибута содержит числитель, а младшие 32 бита содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="07c9f-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="07c9f-110">Например, если частота кадров составляет 30 кадров в секунду (кадров/с), то соотношение составляет 30/1.</span><span class="sxs-lookup"><span data-stu-id="07c9f-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="07c9f-111">Если частота кадров составляет 29,97 кадров/с, то коэффициент равен 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="07c9f-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="07c9f-112">Чтобы задать значение, используйте функцию [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="07c9f-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="07c9f-113">Чтобы получить значение, используйте функцию [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="07c9f-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="07c9f-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="07c9f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="07c9f-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="07c9f-115">Examples</span></span>

<span data-ttu-id="07c9f-116">В следующем примере задается частота кадров для типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="07c9f-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="07c9f-117">В следующем примере показано получение частоты кадров из типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="07c9f-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="07c9f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="07c9f-118">Requirements</span></span>



| <span data-ttu-id="07c9f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="07c9f-119">Requirement</span></span> | <span data-ttu-id="07c9f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="07c9f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07c9f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07c9f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07c9f-122">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="07c9f-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="07c9f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07c9f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07c9f-124">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="07c9f-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="07c9f-125">Header</span><span class="sxs-lookup"><span data-stu-id="07c9f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c9f-126"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c9f-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c9f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07c9f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c9f-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07c9f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="07c9f-129">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="07c9f-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="07c9f-130">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="07c9f-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="07c9f-131">**мфаверажетимеперфраметофрамерате**</span><span class="sxs-lookup"><span data-stu-id="07c9f-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="07c9f-132">**мффрамератетоаверажетимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="07c9f-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




