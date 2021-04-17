---
description: Ширина и высота видеокадра в пикселях.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: Атрибут MF_MT_FRAME_SIZE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656705"
---
# <a name="mf_mt_frame_size-attribute"></a><span data-ttu-id="286b6-103">\_ \_ Атрибут размера пакета MF MT \_</span><span class="sxs-lookup"><span data-stu-id="286b6-103">MF\_MT\_FRAME\_SIZE attribute</span></span>

<span data-ttu-id="286b6-104">Ширина и высота видеокадра в пикселях.</span><span class="sxs-lookup"><span data-stu-id="286b6-104">Width and height of a video frame, in pixels.</span></span>

## <a name="data-type"></a><span data-ttu-id="286b6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="286b6-105">Data type</span></span>

<span data-ttu-id="286b6-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="286b6-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="286b6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="286b6-107">Remarks</span></span>

<span data-ttu-id="286b6-108">Верхние 32 разрядов содержат ширину, а более низкие биты 32 содержат высоту.</span><span class="sxs-lookup"><span data-stu-id="286b6-108">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="286b6-109">Чтобы задать этот атрибут, используйте функцию [**мфсетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="286b6-109">To set this attribute, use the [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) function.</span></span> <span data-ttu-id="286b6-110">Чтобы получить этот атрибут, используйте функцию [**мфжетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="286b6-110">To get this attribute, use the [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) function.</span></span>

<span data-ttu-id="286b6-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="286b6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="286b6-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="286b6-112">Examples</span></span>


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a><span data-ttu-id="286b6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="286b6-113">Requirements</span></span>



| <span data-ttu-id="286b6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="286b6-114">Requirement</span></span> | <span data-ttu-id="286b6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="286b6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="286b6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="286b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="286b6-117">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="286b6-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="286b6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="286b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="286b6-119">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="286b6-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="286b6-120">Header</span><span class="sxs-lookup"><span data-stu-id="286b6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="286b6-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="286b6-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="286b6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="286b6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="286b6-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="286b6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="286b6-124">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="286b6-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="286b6-125">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="286b6-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




