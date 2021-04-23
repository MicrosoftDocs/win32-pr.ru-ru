---
description: Содержит дополнительные данные формата для типа мультимедиа.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Атрибут MF_MT_USER_DATA (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712579"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="31496-103">\_ \_ Атрибут данных пользователя MF MT \_</span><span class="sxs-lookup"><span data-stu-id="31496-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="31496-104">Содержит дополнительные данные формата для типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31496-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="31496-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="31496-105">Data type</span></span>

<span data-ttu-id="31496-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="31496-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="31496-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31496-107">Remarks</span></span>

<span data-ttu-id="31496-108">Значение данных в этом атрибуте зависит от формата, который описывается типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31496-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="31496-109">Тип формата</span><span class="sxs-lookup"><span data-stu-id="31496-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="31496-110">Дополнительные данные формата</span><span class="sxs-lookup"><span data-stu-id="31496-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31496-111">Кодек Windows Media.</span><span class="sxs-lookup"><span data-stu-id="31496-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="31496-112">Частные данные кодека.</span><span class="sxs-lookup"><span data-stu-id="31496-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="31496-113">Преобразована структура [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="31496-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="31496-114">Дополнительные данные, которые появляются после структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , не включая таблицу цветов или цветовые маски.</span><span class="sxs-lookup"><span data-stu-id="31496-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="31496-115">Преобразована структура [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) или [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="31496-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="31496-116">Дополнительные данные, которые отображаются после структуры звукового формата.</span><span class="sxs-lookup"><span data-stu-id="31496-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="31496-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="31496-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="31496-118">Требования</span><span class="sxs-lookup"><span data-stu-id="31496-118">Requirements</span></span>



| <span data-ttu-id="31496-119">Требование</span><span class="sxs-lookup"><span data-stu-id="31496-119">Requirement</span></span> | <span data-ttu-id="31496-120">Значение</span><span class="sxs-lookup"><span data-stu-id="31496-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31496-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31496-121">Minimum supported client</span></span><br/> | <span data-ttu-id="31496-122">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="31496-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="31496-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31496-123">Minimum supported server</span></span><br/> | <span data-ttu-id="31496-124">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="31496-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="31496-125">Header</span><span class="sxs-lookup"><span data-stu-id="31496-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="31496-126"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="31496-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31496-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31496-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31496-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31496-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31496-129">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="31496-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="31496-130">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="31496-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="31496-131">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="31496-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="31496-132">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="31496-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
