---
description: Содержит эскиз фотографии Имфсампле.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Атрибут MFSampleExtension_PhotoThumbnail (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155962"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="66b5d-103">\_Атрибут Фотоэскизов мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="66b5d-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="66b5d-104">Содержит эскиз фотографии [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="66b5d-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="66b5d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="66b5d-105">Data type</span></span>

<span data-ttu-id="66b5d-106">**IUnknown** , хранимый как **имфмедиабуффер**</span><span class="sxs-lookup"><span data-stu-id="66b5d-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="66b5d-107">Эскиз настраивается с помощью **кспропертисетид \_ екстендедкамераконтрол**.</span><span class="sxs-lookup"><span data-stu-id="66b5d-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b5d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66b5d-108">Remarks</span></span>

<span data-ttu-id="66b5d-109">Этот атрибут задается для [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , ПРЕДОСТАВЛЯЕМого MFT0, и является интерфейсом [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , связанным с эскизом фотографии.</span><span class="sxs-lookup"><span data-stu-id="66b5d-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="66b5d-110">Эскиз фотографии может иметь формат JPEG (изображение крупного типа), NV12 или ARGB32.</span><span class="sxs-lookup"><span data-stu-id="66b5d-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="66b5d-111">[Мфсампликстенсион \_ фотосумбнаилмедиатипе](mfsampleextension-photothumbnailmediatype.md) необходим для того, чтобы эскизы описывали тип носителя.</span><span class="sxs-lookup"><span data-stu-id="66b5d-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b5d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="66b5d-112">Requirements</span></span>



| <span data-ttu-id="66b5d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="66b5d-113">Requirement</span></span> | <span data-ttu-id="66b5d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="66b5d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66b5d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66b5d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="66b5d-116">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="66b5d-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="66b5d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66b5d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="66b5d-118">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="66b5d-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="66b5d-119">Header</span><span class="sxs-lookup"><span data-stu-id="66b5d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b5d-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b5d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b5d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66b5d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b5d-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66b5d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66b5d-123">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="66b5d-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
