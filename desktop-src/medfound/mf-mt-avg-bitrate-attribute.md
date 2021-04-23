---
description: Приблизительная скорость передачи данных в потоке видео (в битах в секунду) для типа видео.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: Атрибут MF_MT_AVG_BITRATE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424017"
---
# <a name="mf_mt_avg_bitrate-attribute"></a><span data-ttu-id="e68d7-103">\_Атрибут с \_ средним скоростью MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e68d7-103">MF\_MT\_AVG\_BITRATE attribute</span></span>

<span data-ttu-id="e68d7-104">Приблизительная скорость передачи данных в потоке видео (в битах в секунду) для типа видео.</span><span class="sxs-lookup"><span data-stu-id="e68d7-104">Approximate data rate of the video stream, in bits per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e68d7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e68d7-105">Data type</span></span>

<span data-ttu-id="e68d7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e68d7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e68d7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e68d7-107">Remarks</span></span>

<span data-ttu-id="e68d7-108">Этот атрибут соответствует элементу **двбитрате** в структурах [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) и [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="e68d7-108">This attribute corresponds to the **dwBitRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="e68d7-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="e68d7-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68d7-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e68d7-110">Requirements</span></span>



| <span data-ttu-id="e68d7-111">Требование</span><span class="sxs-lookup"><span data-stu-id="e68d7-111">Requirement</span></span> | <span data-ttu-id="e68d7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e68d7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e68d7-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e68d7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e68d7-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="e68d7-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e68d7-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e68d7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e68d7-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="e68d7-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e68d7-117">Header</span><span class="sxs-lookup"><span data-stu-id="e68d7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e68d7-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e68d7-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68d7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e68d7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68d7-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e68d7-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e68d7-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="e68d7-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e68d7-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e68d7-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e68d7-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="e68d7-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e68d7-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e68d7-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
