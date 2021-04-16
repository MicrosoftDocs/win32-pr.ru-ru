---
description: Указывает длительность презентации в единицах 100-наносекундных.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Атрибут MF_PD_DURATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712324"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="b4b83-103">\_ \_ Атрибут DURATION для MF PD</span><span class="sxs-lookup"><span data-stu-id="b4b83-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="b4b83-104">Указывает длительность презентации в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="b4b83-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="b4b83-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b4b83-105">Data type</span></span>

<span data-ttu-id="b4b83-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b4b83-106">**UINT64**</span></span>

<span data-ttu-id="b4b83-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="b4b83-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b83-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4b83-108">Remarks</span></span>

<span data-ttu-id="b4b83-109">Источники мультимедиа могут установить этот атрибут для дескриптора презентации, чтобы указать длительность презентации.</span><span class="sxs-lookup"><span data-stu-id="b4b83-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="b4b83-110">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="b4b83-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="b4b83-111">Однако атрибут не должен содержать отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="b4b83-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="b4b83-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b4b83-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="b4b83-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="b4b83-113">Examples</span></span>

<span data-ttu-id="b4b83-114">В следующем примере показано, как получить длительность презентации из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b4b83-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b4b83-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b4b83-115">Requirements</span></span>



| <span data-ttu-id="b4b83-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b4b83-116">Requirement</span></span> | <span data-ttu-id="b4b83-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b4b83-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b83-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4b83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b83-119">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="b4b83-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b4b83-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4b83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b83-121">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="b4b83-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b4b83-122">Header</span><span class="sxs-lookup"><span data-stu-id="b4b83-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b83-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b83-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b83-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4b83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b83-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4b83-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b4b83-126">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="b4b83-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="b4b83-127">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="b4b83-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="b4b83-128">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="b4b83-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b4b83-129">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="b4b83-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b4b83-130">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="b4b83-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




