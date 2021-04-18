---
description: Содержит Имфмедиатипе, описывающий тип формата изображения, который содержится в \_ атрибуте Мфсампликстенсион thumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Атрибут MFSampleExtension_PhotoThumbnailMediaType (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720037"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="af960-103">Мфсампликстенсион \_ фотосумбнаилмедиатипе, атрибут</span><span class="sxs-lookup"><span data-stu-id="af960-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="af960-104">Содержит [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , описывающий тип формата изображения, который содержится в атрибуте [мфсампликстенсион \_ thumbnail](mfsampleextension-photothumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="af960-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="af960-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="af960-105">Data type</span></span>

<span data-ttu-id="af960-106">**IUnknown** , хранимый как **имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="af960-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="af960-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af960-107">Remarks</span></span>

<span data-ttu-id="af960-108">Если атрибут [мфсампликстенсион \_ фотоэскизов](mfsampleextension-photothumbnail.md) имеется в образце Photo, то мфсампликстенсион \_ фотосумбнаилмедиатипе является обязательным и должен содержать, по крайней мере, [ \_ \_ основной \_ тип MF MT, номер](mf-mt-major-type-attribute.md)MF- [ \_ \_ MT](mf-mt-subtype-attribute.md) и [ \_ \_ \_ Размер кадра MF MT](mf-mt-frame-size-attribute.md) , описывающие эскиз.</span><span class="sxs-lookup"><span data-stu-id="af960-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="af960-109">Требования</span><span class="sxs-lookup"><span data-stu-id="af960-109">Requirements</span></span>



| <span data-ttu-id="af960-110">Требование</span><span class="sxs-lookup"><span data-stu-id="af960-110">Requirement</span></span> | <span data-ttu-id="af960-111">Значение</span><span class="sxs-lookup"><span data-stu-id="af960-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af960-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af960-112">Minimum supported client</span></span><br/> | <span data-ttu-id="af960-113">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="af960-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="af960-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af960-114">Minimum supported server</span></span><br/> | <span data-ttu-id="af960-115">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="af960-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="af960-116">Header</span><span class="sxs-lookup"><span data-stu-id="af960-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="af960-117"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="af960-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af960-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af960-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af960-119">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af960-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="af960-120">Мфсампликстенсион \_ ФотоЭскизы</span><span class="sxs-lookup"><span data-stu-id="af960-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




