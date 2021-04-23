---
description: Источник файлов в формате MP3 анализирует MP3-файлы.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Источник MP3-файла
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155343"
---
# <a name="mp3-file-source"></a><span data-ttu-id="edbf4-103">Источник MP3-файла</span><span class="sxs-lookup"><span data-stu-id="edbf4-103">MP3 File Source</span></span>

<span data-ttu-id="edbf4-104">Источник файлов в формате MP3 анализирует MP3-файлы.</span><span class="sxs-lookup"><span data-stu-id="edbf4-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="edbf4-105">Источник файлов в формате MP3 выводит буферы, содержащие звуковые кадры MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="edbf4-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="edbf4-106">Он не расшифровывает звук.</span><span class="sxs-lookup"><span data-stu-id="edbf4-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="edbf4-107">Расширения файлов и типы MIME</span><span class="sxs-lookup"><span data-stu-id="edbf4-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="edbf4-108">Источник файлов в формате MP3 — это источник мультимедиа по умолчанию для следующего расширения имени файла:</span><span class="sxs-lookup"><span data-stu-id="edbf4-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="edbf4-109">.mp3</span><span class="sxs-lookup"><span data-stu-id="edbf4-109">.mp3</span></span>

<span data-ttu-id="edbf4-110">Он также является источником мультимедиа по умолчанию для следующих типов MIME.</span><span class="sxs-lookup"><span data-stu-id="edbf4-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="edbf4-111">аудио/MPEG</span><span class="sxs-lookup"><span data-stu-id="edbf4-111">audio/mpeg</span></span>
-   <span data-ttu-id="edbf4-112">аудио/x-MP3</span><span class="sxs-lookup"><span data-stu-id="edbf4-112">audio/x-mp3</span></span>
-   <span data-ttu-id="edbf4-113">аудио/x-MPEG</span><span class="sxs-lookup"><span data-stu-id="edbf4-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="edbf4-114">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="edbf4-114">Media Types</span></span>

<span data-ttu-id="edbf4-115">Тип носителя, предлагаемый источником файлов в формате MP3, содержит следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="edbf4-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="edbf4-116">attribute</span><span class="sxs-lookup"><span data-stu-id="edbf4-116">Attribute</span></span>                                                                                    | <span data-ttu-id="edbf4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="edbf4-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edbf4-118">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="edbf4-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="edbf4-119">Равно **мфмедиатипе \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="edbf4-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="edbf4-120">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="edbf4-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="edbf4-121">Равно **мфаудиоформат \_ MP3** или **мфаудиоформат \_ MPEG**.</span><span class="sxs-lookup"><span data-stu-id="edbf4-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="edbf4-122">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="edbf4-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="edbf4-123">Среднее число байтов в секунду.</span><span class="sxs-lookup"><span data-stu-id="edbf4-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="edbf4-124">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="edbf4-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="edbf4-125">Равно 1.</span><span class="sxs-lookup"><span data-stu-id="edbf4-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="edbf4-126">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="edbf4-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="edbf4-127">Число аудиоканалов.</span><span class="sxs-lookup"><span data-stu-id="edbf4-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="edbf4-128">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="edbf4-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="edbf4-129">Количество звуковых выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="edbf4-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="edbf4-130">**\_ \_ данные пользователя MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="edbf4-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="edbf4-131">Содержит часть структуры [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) , которая отображается после элемента **вфкс** структуры.</span><span class="sxs-lookup"><span data-stu-id="edbf4-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="edbf4-132">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="edbf4-132">Interfaces</span></span>

<span data-ttu-id="edbf4-133">Источник файлов в формате MP3 предоставляет следующие интерфейсы через [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="edbf4-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="edbf4-134">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="edbf4-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="edbf4-135">**имфмедиаевентженератор**</span><span class="sxs-lookup"><span data-stu-id="edbf4-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="edbf4-136">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="edbf4-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="edbf4-137">Кроме того, он предоставляет доступ к следующим интерфейсам через [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span><span class="sxs-lookup"><span data-stu-id="edbf4-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edbf4-138">Service GUID</span><span class="sxs-lookup"><span data-stu-id="edbf4-138">Service GUID</span></span></th>
<th><span data-ttu-id="edbf4-139">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="edbf4-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edbf4-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="edbf4-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="edbf4-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>имфметадатапровидер</strong></a></span><span class="sxs-lookup"><span data-stu-id="edbf4-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edbf4-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="edbf4-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="edbf4-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>ипропертисторе</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="edbf4-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="edbf4-144">См. раздел <a href="shell-metadata-providers.md">поставщики метаданных оболочки</a>.</span><span class="sxs-lookup"><span data-stu-id="edbf4-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edbf4-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="edbf4-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="edbf4-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>имфратеконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="edbf4-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edbf4-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="edbf4-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="edbf4-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>имфратесуппорт</strong></a></span><span class="sxs-lookup"><span data-stu-id="edbf4-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="edbf4-149">Требования</span><span class="sxs-lookup"><span data-stu-id="edbf4-149">Requirements</span></span>



| <span data-ttu-id="edbf4-150">Требование</span><span class="sxs-lookup"><span data-stu-id="edbf4-150">Requirement</span></span> | <span data-ttu-id="edbf4-151">Значение</span><span class="sxs-lookup"><span data-stu-id="edbf4-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="edbf4-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edbf4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="edbf4-153">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="edbf4-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edbf4-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edbf4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="edbf4-155">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="edbf4-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="edbf4-156">DLL</span><span class="sxs-lookup"><span data-stu-id="edbf4-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edbf4-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edbf4-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbf4-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edbf4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbf4-159">Источники и приемники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="edbf4-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="edbf4-160">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="edbf4-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="edbf4-161">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="edbf4-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="edbf4-162">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="edbf4-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
