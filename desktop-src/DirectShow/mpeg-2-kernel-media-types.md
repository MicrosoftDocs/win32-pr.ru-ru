---
description: Для нескольких идентификаторов GUID типа носителя MPEG-2 в Windows DDK определены имена, отличные от имен, используемых в DirectShow. В следующей таблице приведены имена DirectShow (определенные в Ксууидс. h) и соответствующие имена в режиме ядра (определенные в Ксмедиа. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Типы носителей ядра MPEG-2 (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689096"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="410cb-104">Типы носителей ядра MPEG-2</span><span class="sxs-lookup"><span data-stu-id="410cb-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="410cb-105">Для нескольких идентификаторов GUID типа носителя MPEG-2 в Windows DDK определены имена, отличные от имен, используемых в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="410cb-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="410cb-106">В следующей таблице приведены имена DirectShow (определенные в Ксууидс. h) и соответствующие имена в режиме ядра (определенные в Ксмедиа. h).</span><span class="sxs-lookup"><span data-stu-id="410cb-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="410cb-107">Имя в Ксууидс. h</span><span class="sxs-lookup"><span data-stu-id="410cb-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="410cb-108">Имя в Ксмедиа. h</span><span class="sxs-lookup"><span data-stu-id="410cb-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="410cb-109">ФОРМАТ \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="410cb-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="410cb-110">\_вавеформатекс ОПИСАТЕЛЬ ксдатаформат \_</span><span class="sxs-lookup"><span data-stu-id="410cb-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="410cb-111">ФОРМАТ \_ MPEG2Video</span><span class="sxs-lookup"><span data-stu-id="410cb-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="410cb-112">\_Видео о спецификаторе ксдатаформат \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="410cb-113">МЕДИАСУБТИПЕ \_ ATSC \_ Si</span><span class="sxs-lookup"><span data-stu-id="410cb-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="410cb-114">\_ПОДТИП ксдатаформат \_ ATSC \_ Si</span><span class="sxs-lookup"><span data-stu-id="410cb-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="410cb-115">МЕДИАСУБТИПЕ \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="410cb-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="410cb-116">КСДАТАФОРМАТ \_ подтип \_ AC3 \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="410cb-117">МЕДИАСУБТИПЕ \_ DVB \_ Si</span><span class="sxs-lookup"><span data-stu-id="410cb-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="410cb-118">\_ПОДТИП ксдатаформат \_ DVB \_ Si</span><span class="sxs-lookup"><span data-stu-id="410cb-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="410cb-119">МЕДИАСУБТИПЕ \_ DVD \_ лпкм \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="410cb-120">КСДАТАФОРМАТ \_ подтип \_ лпкм \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="410cb-121">МЕДИАСУБТИПЕ \_ MPEG2 \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="410cb-122">КСДАТАФОРМАТ \_ подтипа \_ MPEG2 \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="410cb-123">\_Программа медиасубтипе MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="410cb-124">\_Программа статического ксдатаформат \_ типа \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="410cb-125">\_Транспорт медиасубтипе MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="410cb-126">\_Транспорт ксдатаформат типа \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="410cb-127">\_Видео медиасубтипе MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="410cb-128">\_Видео о ПОДТИПЕ ксдатаформат \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="410cb-129">\_Разделы MEDIATYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="410cb-130">\_Разделы ксдатаформат типа \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="410cb-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="410cb-131">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="410cb-132">\_тип ксдатаформат \_ Audio</span><span class="sxs-lookup"><span data-stu-id="410cb-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="410cb-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="410cb-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="410cb-134">КСДАТАФОРМАТ \_ тип \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="410cb-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="410cb-135">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="410cb-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="410cb-136">\_видео типа \_ ксдатаформат</span><span class="sxs-lookup"><span data-stu-id="410cb-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="410cb-137">Требования</span><span class="sxs-lookup"><span data-stu-id="410cb-137">Requirements</span></span>



| <span data-ttu-id="410cb-138">Требование</span><span class="sxs-lookup"><span data-stu-id="410cb-138">Requirement</span></span> | <span data-ttu-id="410cb-139">Значение</span><span class="sxs-lookup"><span data-stu-id="410cb-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="410cb-140">Header</span><span class="sxs-lookup"><span data-stu-id="410cb-140">Header</span></span><br/> | <dl> <span data-ttu-id="410cb-141"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="410cb-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410cb-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="410cb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410cb-143">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="410cb-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




