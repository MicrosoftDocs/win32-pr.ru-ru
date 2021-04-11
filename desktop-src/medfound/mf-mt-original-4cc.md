---
description: Содержит исходный кодек FOURCC для видеопотока.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Атрибут MF_MT_ORIGINAL_4CC (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999172"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="221d4-103">\_ \_ Исходный \_ атрибут 4CC MF</span><span class="sxs-lookup"><span data-stu-id="221d4-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="221d4-104">Содержит исходный кодек FOURCC для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="221d4-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="221d4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="221d4-105">Data type</span></span>

<span data-ttu-id="221d4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="221d4-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="221d4-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="221d4-107">Get/set</span></span>

<span data-ttu-id="221d4-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="221d4-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="221d4-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="221d4-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="221d4-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="221d4-110">Applies to</span></span>

[<span data-ttu-id="221d4-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="221d4-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="221d4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="221d4-112">Remarks</span></span>

<span data-ttu-id="221d4-113">В зависимости от исходного файла источник AVI Media может установить этот атрибут для типов мультимедиа, которые он предлагает.</span><span class="sxs-lookup"><span data-stu-id="221d4-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="221d4-114">Файл AVI содержит заголовок потока для каждого потока в файле.</span><span class="sxs-lookup"><span data-stu-id="221d4-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="221d4-115">Источник AVI Media преобразует заголовок потока в тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="221d4-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="221d4-116">Для сжатых видеопотоков в заголовке потока содержится объект FOURCC, идентифицирующий видеокодек.</span><span class="sxs-lookup"><span data-stu-id="221d4-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="221d4-117">В большинстве случаев источник AVI Media преобразует это значение непосредственно в GUID подтипа, как описано в разделе [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="221d4-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="221d4-118">В некоторых случаях, однако, он сопоставляет исходное значение FOURCC с другим параметром FOURCC, эквивалентным.</span><span class="sxs-lookup"><span data-stu-id="221d4-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="221d4-119">Если это так, источник мультимедиа сохраняет исходное значение FOURCC в типе носителя, используя \_ \_ Исходный атрибут 4CC MF MT \_ .</span><span class="sxs-lookup"><span data-stu-id="221d4-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="221d4-120">Сопоставления FOURCC хранятся в реестре в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="221d4-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="221d4-121">**HKey \_ \_Корневой** \\ **медиафаундатион** классов \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="221d4-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="221d4-122">Каждая запись имеет значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="221d4-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="221d4-123">Имя записи является шестнадцатеричным представлением FOURCC без префикса "0x" и первым символом, показываемым первым в строке.</span><span class="sxs-lookup"><span data-stu-id="221d4-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="221d4-124">Например, код FOURCC "abcd" будет выглядеть как "61626364".</span><span class="sxs-lookup"><span data-stu-id="221d4-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="221d4-125">Значение записи является эквивалентным кодом FOURCC.</span><span class="sxs-lookup"><span data-stu-id="221d4-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="221d4-126">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="221d4-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="221d4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="221d4-127">Requirements</span></span>



| <span data-ttu-id="221d4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="221d4-128">Requirement</span></span> | <span data-ttu-id="221d4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="221d4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="221d4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="221d4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="221d4-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="221d4-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="221d4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="221d4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="221d4-133">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="221d4-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="221d4-134">Header</span><span class="sxs-lookup"><span data-stu-id="221d4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="221d4-135"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="221d4-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="221d4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="221d4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221d4-137">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="221d4-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="221d4-138">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="221d4-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




