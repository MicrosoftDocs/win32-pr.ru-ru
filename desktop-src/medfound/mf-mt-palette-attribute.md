---
description: Содержит записи палитры для типа видеоматериала. Используйте этот атрибут для форматов видео палеттизед, например RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: Атрибут MF_MT_PALETTE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647297"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="c876c-104">\_ \_ Атрибут палитры MF MT</span><span class="sxs-lookup"><span data-stu-id="c876c-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="c876c-105">Содержит записи палитры для типа видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="c876c-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="c876c-106">Используйте этот атрибут для форматов видео палеттизед, например RGB 8.</span><span class="sxs-lookup"><span data-stu-id="c876c-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="c876c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c876c-107">Data type</span></span>

<span data-ttu-id="c876c-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="c876c-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c876c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c876c-109">Remarks</span></span>

<span data-ttu-id="c876c-110">Данные атрибута являются массивом объединений [**мфпалеттинтри**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .</span><span class="sxs-lookup"><span data-stu-id="c876c-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="c876c-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="c876c-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c876c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c876c-112">Requirements</span></span>



| <span data-ttu-id="c876c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c876c-113">Requirement</span></span> | <span data-ttu-id="c876c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c876c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c876c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c876c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c876c-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c876c-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c876c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c876c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c876c-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c876c-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c876c-119">Header</span><span class="sxs-lookup"><span data-stu-id="c876c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c876c-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c876c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c876c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c876c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c876c-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c876c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c876c-123">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="c876c-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c876c-124">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="c876c-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="c876c-125">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c876c-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c876c-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c876c-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




