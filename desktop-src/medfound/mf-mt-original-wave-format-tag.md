---
description: Содержит тег исходного формата WAVE для аудиопотока.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Атрибут MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674409"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="dff05-103">\_ \_ \_ \_ \_ Атрибут пометки исходного формата MF MT</span><span class="sxs-lookup"><span data-stu-id="dff05-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="dff05-104">Содержит тег исходного формата WAVE для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="dff05-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="dff05-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dff05-105">Data type</span></span>

<span data-ttu-id="dff05-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dff05-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="dff05-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="dff05-107">Get/set</span></span>

<span data-ttu-id="dff05-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="dff05-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="dff05-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="dff05-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="dff05-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="dff05-110">Applies to</span></span>

[<span data-ttu-id="dff05-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="dff05-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="dff05-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dff05-112">Remarks</span></span>

<span data-ttu-id="dff05-113">В зависимости от исходного файла источник AVI Media может установить этот атрибут для типов мультимедиа, которые он предлагает.</span><span class="sxs-lookup"><span data-stu-id="dff05-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="dff05-114">Файл AVI содержит заголовок потока для каждого потока в файле.</span><span class="sxs-lookup"><span data-stu-id="dff05-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="dff05-115">Источник AVI Media преобразует заголовок потока в тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dff05-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="dff05-116">Для звуковых потоков в заголовке потока содержится тег Format, определяющий формат аудио.</span><span class="sxs-lookup"><span data-stu-id="dff05-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="dff05-117">(Тег Format содержится в элементе **вформаттаг** структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .) В большинстве случаев источник AVI Media преобразует тег формата непосредственно в GUID подтипа, как описано в разделе [**идентификаторы GUID подтипа Audio**](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="dff05-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="dff05-118">В некоторых случаях, однако, он сопоставляет исходный тег формата с другим эквивалентным тегом формата.</span><span class="sxs-lookup"><span data-stu-id="dff05-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="dff05-119">Если это так, источник мультимедиа сохраняет исходный тег формата в типе носителя, используя \_ \_ \_ \_ атрибут пометки ИСХОДНОГО волнового формата MF MT \_ .</span><span class="sxs-lookup"><span data-stu-id="dff05-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="dff05-120">Сопоставления форматов хранятся в реестре в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="dff05-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="dff05-121">**HKey \_ \_Корневой** \\ **медиафаундатион** классов \\ **мапаудиоформаттаг**</span><span class="sxs-lookup"><span data-stu-id="dff05-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="dff05-122">Каждая запись имеет значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="dff05-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="dff05-123">Имя записи представляет собой десятичное представление тега Format.</span><span class="sxs-lookup"><span data-stu-id="dff05-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="dff05-124">Значением записи является эквивалентный тег Format.</span><span class="sxs-lookup"><span data-stu-id="dff05-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="dff05-125">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="dff05-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff05-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dff05-126">Requirements</span></span>



| <span data-ttu-id="dff05-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dff05-127">Requirement</span></span> | <span data-ttu-id="dff05-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dff05-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dff05-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dff05-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dff05-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dff05-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dff05-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dff05-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dff05-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dff05-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="dff05-133">Header</span><span class="sxs-lookup"><span data-stu-id="dff05-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff05-134"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff05-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff05-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dff05-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff05-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dff05-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dff05-137">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dff05-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
