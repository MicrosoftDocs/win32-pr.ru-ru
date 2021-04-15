---
description: Благодаря увеличению количества устройств хранения мультимедиа, требующих сжатия звуковых форматов, приложения должны вычислить, описать и использовать множество новых закодированных звуковых данных для передачи содержимого с компьютеров на устройства, например, с помощью формата HDMI или Дисплайпорт.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Представление форматов для передач IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655925"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a><span data-ttu-id="6d835-103">Представление форматов для передач IEC 61937</span><span class="sxs-lookup"><span data-stu-id="6d835-103">Representing Formats for IEC 61937 Transmissions</span></span>

<span data-ttu-id="6d835-104">Благодаря увеличению количества устройств хранения мультимедиа, требующих сжатия звуковых форматов, приложения должны вычислить, описать и использовать множество новых закодированных звуковых данных для передачи содержимого с компьютеров на устройства, например, с помощью формата HDMI или Дисплайпорт.</span><span class="sxs-lookup"><span data-stu-id="6d835-104">With the increase in media storage devices that require compressed audio formats, applications must identify, describe, and use a variety of new encoded audio content for transmitting content from PCs to devices such as HDMI or DisplayPort receiver.</span></span>

<span data-ttu-id="6d835-105">Для представления закодированного звукового потока, передаваемого через совместимый с IEC 61937 интерфейс, приложение должно предоставить:</span><span class="sxs-lookup"><span data-stu-id="6d835-105">To represent an encoded audio stream to be transmitted over an IEC 61937-compatible interface, an application must provide:</span></span>

-   <span data-ttu-id="6d835-106">Характеристики закодированного звукового потока для передачи.</span><span class="sxs-lookup"><span data-stu-id="6d835-106">The characteristics of an encoded audio stream to be transmitted.</span></span>

-   <span data-ttu-id="6d835-107">Характеристики декодированного звукового потока на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="6d835-107">The characteristics of a decoded audio stream on the target device.</span></span>

<span data-ttu-id="6d835-108">В Windows Vista и более ранних операционных системах Windows приложение может определить уровень качества звукового формата от количества каналов, размера выборки и скорости передачи данных в потоке аудиопотока, использующем этот формат.</span><span class="sxs-lookup"><span data-stu-id="6d835-108">In Windows Vista and earlier Windows operating systems, an application can infer the quality level of an audio format from the number of channels, the sample size, and the data rate of an audio stream that uses the format.</span></span> <span data-ttu-id="6d835-109">Для формата PCM эта информация доступна из элементов **нчаннелс**, **нсамплесперсек** и **навгбитесперсек** структуры **вавеформатекс** , которая определяет формат.</span><span class="sxs-lookup"><span data-stu-id="6d835-109">For a PCM format, this information is available from the **nChannels**, **nSamplesPerSec**, and **nAvgBytesPerSec** members of the **WAVEFORMATEX** structure that specifies the format.</span></span> <span data-ttu-id="6d835-110">Для формата, отличного от PCM, эти три элемента были коммандиред для хранения информации о сжатых данных в потоке аудио.</span><span class="sxs-lookup"><span data-stu-id="6d835-110">For a non-PCM format, these three members have been commandeered to store information about the compressed data in the audio stream.</span></span> <span data-ttu-id="6d835-111">Таким словами, структура **вавеформатекс** не имеет сведений о действительном количестве каналов, объеме выборки и скорости передачи данных из аудиопотока, не использующих PCM, после распаковки и воспроизведения потока.</span><span class="sxs-lookup"><span data-stu-id="6d835-111">Thus, the **WAVEFORMATEX** structure lacks information about the effective number of channels, sample size, and data rate of the non-PCM audio stream after the stream is decompressed and played.</span></span> <span data-ttu-id="6d835-112">На основе информации в этой структуре пользователь или приложение могут испытывать трудности при откладывание уровня качества потока, не являющегося потоком PCM.</span><span class="sxs-lookup"><span data-stu-id="6d835-112">Based on the information in this structure, a user or an application might have difficulty inferring the quality level of the non-PCM stream.</span></span>

<span data-ttu-id="6d835-113">**Вавеформатекс** был расширен до структуры **вавеформатекстенсибле** , чтобы предоставить дополнительные характеристики потока.</span><span class="sxs-lookup"><span data-stu-id="6d835-113">The **WAVEFORMATEX** was extended to the **WAVEFORMATEXTENSIBLE** structure to provide the extra stream characteristics.</span></span> <span data-ttu-id="6d835-114">Однако эта структура также недостаточна для описания потока для передачи данных IEC 61937, так как она предполагалась для представления одного набора характеристик и используется для несжатых, многоканальные данные PCM.</span><span class="sxs-lookup"><span data-stu-id="6d835-114">However, this structure is also not adequate in describing the stream for IEC 61937 transmissions because it was intended to represent a single set of characteristics and used for uncompressed, multi-channel PCM data.</span></span>

<span data-ttu-id="6d835-115">В Windows 7 операционная система решает эту проблему, предоставляя поддержку новой структуры, **вавеформатекстенсибле \_ IEC61937** , которая расширяет структуру **вавеформатекстенсибле** для хранения двух наборов характеристик аудиопотока: закодированный аудио формат перед передачей и характеристиками звукового потока после декодирования.</span><span class="sxs-lookup"><span data-stu-id="6d835-115">In Windows 7, the operating system addresses this problem by providing support for a new structure, **WAVEFORMATEXTENSIBLE\_IEC61937** which extends **WAVEFORMATEXTENSIBLE** structure to store two sets of audio stream characteristics: the encoded audio format before transmission and characteristics of the audio stream after it has been decoded.</span></span> <span data-ttu-id="6d835-116">Новая структура явно указывает фактическое количество каналов, размер выборки и скорость передачи данных в формате, не являющемся форматом PCM.</span><span class="sxs-lookup"><span data-stu-id="6d835-116">The new structure explicitly specifies the effective number of channels, sample size, and data rate of a non-PCM format.</span></span> <span data-ttu-id="6d835-117">С помощью этих сведений приложение может определить уровень качества потока, не являющегося потоком PCM, после его распаковки и воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6d835-117">With this information, an application can infer the quality level of the non-PCM stream after it is decompressed and played.</span></span>

<span data-ttu-id="6d835-118">Структура **\_ IEC61937 вавеформатекстенсибле** объявляется в заголовке ксмедиа. h, ВКЛЮЧЕННОМ в пакет SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d835-118">The **WAVEFORMATEXTENSIBLE\_IEC61937** structure is declared in the KsMedia.h header included with the Windows 7 SDK.</span></span> <span data-ttu-id="6d835-119">Элемент **форматекст** — это структура **вавеформатекстенсибле** , в которой хранятся характеристики передаваемого потока.</span><span class="sxs-lookup"><span data-stu-id="6d835-119">The **FormatExt** member is the **WAVEFORMATEXTENSIBLE** structure that stores the characteristics of the stream to be transmitted.</span></span> <span data-ttu-id="6d835-120">Элемент **Format** структуры **вавеформатекстенсибле** является структурой **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="6d835-120">The **Format** member of the **WAVEFORMATEXTENSIBLE** structure is the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="6d835-121">Содержимое этого **вавеформатекс** и **вавеформатекстенсибле** указывает приложению, может ли структура интерпретироваться как структура **\_ IEC61937 вавеформатекстенсибле** .</span><span class="sxs-lookup"><span data-stu-id="6d835-121">The contents of this **WAVEFORMATEX** and **WAVEFORMATEXTENSIBLE** indicate to an application whether the structure can be interpreted as a **WAVEFORMATEXTENSIBLE\_IEC61937** structure.</span></span> <span data-ttu-id="6d835-122">Для структуры **\_ IEC61937 вавеформатекстенсибле** :</span><span class="sxs-lookup"><span data-stu-id="6d835-122">For a **WAVEFORMATEXTENSIBLE\_IEC61937** structure:</span></span>

-   <span data-ttu-id="6d835-123">Элемент **вформаттаг** объекта **вавеформатекс** должен содержать формат волны \_ \_ EXTENSIBLE ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).</span><span class="sxs-lookup"><span data-stu-id="6d835-123">The **wFormatTag** member of **WAVEFORMATEX** must contain WAVE\_FORMAT\_EXTENSIBLE (`FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE`).</span></span>

-   <span data-ttu-id="6d835-124">Элемент **Подформата** структуры **вавеформатекстенсибле** указывает идентификатор GUID закодированного формата для передачи.</span><span class="sxs-lookup"><span data-stu-id="6d835-124">The **SubFormat** member of the **WAVEFORMATEXTENSIBLE** structure specifies the GUID of the encoded format to be transmitted.</span></span> <span data-ttu-id="6d835-125">Например, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` указывает формат Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="6d835-125">For example, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indicates the Dolby Digital Plus format.</span></span> <span data-ttu-id="6d835-126">Поддерживаемые идентификаторы GUID см. в разделе идентификаторы GUID подформатов.</span><span class="sxs-lookup"><span data-stu-id="6d835-126">For the supported GUIDs, see SubFormat GUIDs.</span></span>

-   <span data-ttu-id="6d835-127">Размер, указанный членом **КБСИЗЕ** вавеформатекс, составляет 34 байт.</span><span class="sxs-lookup"><span data-stu-id="6d835-127">The size indicated by **cbSize** member of the WAVEFORMATEX is 34 bytes.</span></span> <span data-ttu-id="6d835-128">(`FormatExt.Format.cbSize = 34`).</span><span class="sxs-lookup"><span data-stu-id="6d835-128">(`FormatExt.Format.cbSize = 34`).</span></span> <span data-ttu-id="6d835-129">Общий размер **вавеформатекстенсибле \_ IEC61937** составляет 52 байт.</span><span class="sxs-lookup"><span data-stu-id="6d835-129">The total size of **WAVEFORMATEXTENSIBLE\_IEC61937** is 52 bytes.</span></span>

<span data-ttu-id="6d835-130">Члены **двенкодедсамплесперсек**, **Двенкодедчаннелкаунт** и **дваверажебитесперсек** **вавеформатекстенсибле \_ IEC61937** описывают частоту выборки, число каналов и скорость передачи данных в байтах потока аудиопотока после его декодирования.</span><span class="sxs-lookup"><span data-stu-id="6d835-130">The **dwEncodedSamplesPerSec**, **dwEncodedChannelCount**, and **dwAverageBytesPerSec** members of **WAVEFORMATEXTENSIBLE\_IEC61937** describe the sampling rate, number of channels, and bit rate in bytes of the stream of the audio stream after it has been decoded.</span></span>

## <a name="subformat-guids"></a><span data-ttu-id="6d835-131">Идентификаторы GUID подформата</span><span class="sxs-lookup"><span data-stu-id="6d835-131">SubFormat GUIDs</span></span>

<span data-ttu-id="6d835-132">В Windows 7 заголовок Ксмедиа. h содержит определения для идентификаторов GUID подформата для сжатых звуковых форматов, определенных CEA-861-D.</span><span class="sxs-lookup"><span data-stu-id="6d835-132">In Windows 7, the KsMedia.h header contains definitions for the SubFormat GUIDs for the compressed audio formats defined by CEA-861-D.</span></span> <span data-ttu-id="6d835-133">Идентификаторы GUID указываются в элементе подформата **вавеформатекстенсибле**, указанном в элементе **форматекст** структуры **вавеформатекстенсибле \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).</span><span class="sxs-lookup"><span data-stu-id="6d835-133">The GUIDs are specified in the SubFormat member of the **WAVEFORMATEXTENSIBLE**, specified in the **FormatExt** member of the **WAVEFORMATEXTENSIBLE\_IEC61937** structure (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`).</span></span>

<span data-ttu-id="6d835-134">Идентификаторы GUID для сжатых звуковых форматов, доступных в виде стандартных звуковых форматов IEC 61937, перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6d835-134">The GUIDs for the compressed audio formats that are available as standard IEC 61937 encoded audio formats are listed in the following table.</span></span> <span data-ttu-id="6d835-135">Эти форматы схожи с существующими представлениями форматов звука с кодом 3 (AC-3) и Digital театра (DTS) в Windows.</span><span class="sxs-lookup"><span data-stu-id="6d835-135">These formats are similar to the existing Active Coding 3 (AC-3) and Digital Theater Sound (DTS) formats representations in Windows.</span></span>



| <span data-ttu-id="6d835-136">Тип CEA 861</span><span class="sxs-lookup"><span data-stu-id="6d835-136">CEA 861 Type</span></span> | <span data-ttu-id="6d835-137">GUID подформата</span><span class="sxs-lookup"><span data-stu-id="6d835-137">SubFormat GUID</span></span>                                                                                                          | <span data-ttu-id="6d835-138">Описание</span><span class="sxs-lookup"><span data-stu-id="6d835-138">Description</span></span>                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="6d835-139">0x00</span><span class="sxs-lookup"><span data-stu-id="6d835-139">0x00</span></span>         |                                                                                                                         | <span data-ttu-id="6d835-140">См. поток.</span><span class="sxs-lookup"><span data-stu-id="6d835-140">Refer to the stream.</span></span>                         |
| <span data-ttu-id="6d835-141">0x01</span><span class="sxs-lookup"><span data-stu-id="6d835-141">0x01</span></span>         | <span data-ttu-id="6d835-142">00000000-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-142">00000000-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-143">КСДАТАФОРМАТ \_ подтип \_ вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="6d835-143">KSDATAFORMAT\_SUBTYPE\_WAVEFORMATEX</span></span><br/>                          | <span data-ttu-id="6d835-144">IEC 60958 PCM</span><span class="sxs-lookup"><span data-stu-id="6d835-144">IEC 60958 PCM</span></span>                                |
| <span data-ttu-id="6d835-145">0x02</span><span class="sxs-lookup"><span data-stu-id="6d835-145">0x02</span></span>         | <span data-ttu-id="6d835-146">00000092-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-146">00000092-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-147">\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital</span><span class="sxs-lookup"><span data-stu-id="6d835-147">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL</span></span><br/>              | <span data-ttu-id="6d835-148">AC-3</span><span class="sxs-lookup"><span data-stu-id="6d835-148">AC-3</span></span>                                         |
| <span data-ttu-id="6d835-149">0x03</span><span class="sxs-lookup"><span data-stu-id="6d835-149">0x03</span></span>         | <span data-ttu-id="6d835-150">00000003-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-150">00000003-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-151">КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ MPEG1</span><span class="sxs-lookup"><span data-stu-id="6d835-151">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG1</span></span><br/>                       | <span data-ttu-id="6d835-152">MPEG-1 (уровень 1 & 2)</span><span class="sxs-lookup"><span data-stu-id="6d835-152">MPEG-1 (Layer 1 & 2)</span></span>                         |
| <span data-ttu-id="6d835-153">0x04</span><span class="sxs-lookup"><span data-stu-id="6d835-153">0x04</span></span>         | <span data-ttu-id="6d835-154">00000004-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-154">00000004-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-155">КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ MPEG3</span><span class="sxs-lookup"><span data-stu-id="6d835-155">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG3</span></span><br/>                       | <span data-ttu-id="6d835-156">MPEG-3 (уровень 3)</span><span class="sxs-lookup"><span data-stu-id="6d835-156">MPEG-3 (Layer 3)</span></span>                             |
| <span data-ttu-id="6d835-157">0x05</span><span class="sxs-lookup"><span data-stu-id="6d835-157">0x05</span></span>         | <span data-ttu-id="6d835-158">00000005-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-158">00000005-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-159">\_ПОДТИП ксдатаформат \_ IEC61937 \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="6d835-159">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG2</span></span> <br/>                      | <span data-ttu-id="6d835-160">MPEG-2 (многоканальный)</span><span class="sxs-lookup"><span data-stu-id="6d835-160">MPEG-2(multichannel)</span></span>                         |
| <span data-ttu-id="6d835-161">0x06</span><span class="sxs-lookup"><span data-stu-id="6d835-161">0x06</span></span>         | <span data-ttu-id="6d835-162">00000006-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-162">00000006-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-163">КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ AAC</span><span class="sxs-lookup"><span data-stu-id="6d835-163">KSDATAFORMAT\_SUBTYPE\_IEC61937\_AAC</span></span><br/>                         | <span data-ttu-id="6d835-164">Расширенное аудио кодирование (MPEG-2/4 AAC в ADTS)</span><span class="sxs-lookup"><span data-stu-id="6d835-164">Advanced Audio Coding (MPEG-2/4 AAC in ADTS)</span></span> |
| <span data-ttu-id="6d835-165">0x07</span><span class="sxs-lookup"><span data-stu-id="6d835-165">0x07</span></span>         | <span data-ttu-id="6d835-166">00000008-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-166">00000008-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-167">КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ DTS</span><span class="sxs-lookup"><span data-stu-id="6d835-167">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS</span></span><br/>                         | <span data-ttu-id="6d835-168">DTS</span><span class="sxs-lookup"><span data-stu-id="6d835-168">DTS</span></span>                                          |
| <span data-ttu-id="6d835-169">0x0A</span><span class="sxs-lookup"><span data-stu-id="6d835-169">0x0a</span></span>         | <span data-ttu-id="6d835-170">0000000a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-170">0000000a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-171">\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital \_ Plus</span><span class="sxs-lookup"><span data-stu-id="6d835-171">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS</span></span><br/>        | <span data-ttu-id="6d835-172">Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="6d835-172">Dolby Digital Plus</span></span>                           |
| <span data-ttu-id="6d835-173">0x0A</span><span class="sxs-lookup"><span data-stu-id="6d835-173">0x0a</span></span>         | <span data-ttu-id="6d835-174">0000010a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-174">0000010a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-175">\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ Digital \_ Plus \_ атмос</span><span class="sxs-lookup"><span data-stu-id="6d835-175">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS\_ATMOS</span></span><br/> | <span data-ttu-id="6d835-176">Dolby атмос в кодировке Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="6d835-176">Dolby Atmos encoded with Dolby Digital Plus</span></span>  |
| <span data-ttu-id="6d835-177">0x0f</span><span class="sxs-lookup"><span data-stu-id="6d835-177">0x0f</span></span>         |                                                                                                                         | <span data-ttu-id="6d835-178">Неиспользованные зарезервированные</span><span class="sxs-lookup"><span data-stu-id="6d835-178">Unused Reserved</span></span>                              |



 

<span data-ttu-id="6d835-179">В следующей таблице перечислены идентификаторы GUID для сжатых звуковых форматов, которые передаются в звуковых примерах с высоким уровнем скорости.</span><span class="sxs-lookup"><span data-stu-id="6d835-179">The GUIDs for the compressed audio formats that are transmitted in high bit-rate audio sample packets are listed in the following table.</span></span>



| <span data-ttu-id="6d835-180">Тип CEA 861</span><span class="sxs-lookup"><span data-stu-id="6d835-180">CEA 861 Type</span></span> | <span data-ttu-id="6d835-181">GUID подформата</span><span class="sxs-lookup"><span data-stu-id="6d835-181">SubFormat GUID</span></span>                                                                                           | <span data-ttu-id="6d835-182">Описание</span><span class="sxs-lookup"><span data-stu-id="6d835-182">Description</span></span>                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d835-183">0x0B</span><span class="sxs-lookup"><span data-stu-id="6d835-183">0x0b</span></span>         | <span data-ttu-id="6d835-184">0000000b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-184">0000000b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-185">\_ПОДТИП ксдатаформат \_ IEC61937 \_ DTS \_ HD</span><span class="sxs-lookup"><span data-stu-id="6d835-185">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS\_HD</span></span><br/>      | <span data-ttu-id="6d835-186">DTS-HD (24-разрядная, 96Khz)</span><span class="sxs-lookup"><span data-stu-id="6d835-186">DTS-HD (24-bit, 96Khz)</span></span>                                                                                                          |
| <span data-ttu-id="6d835-187">0x0c</span><span class="sxs-lookup"><span data-stu-id="6d835-187">0x0c</span></span>         | <span data-ttu-id="6d835-188">0000000c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-188">0000000c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-189">\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ MLP</span><span class="sxs-lookup"><span data-stu-id="6d835-189">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MLP</span></span><br/>   | <span data-ttu-id="6d835-190">Dolby водо1,0:</span><span class="sxs-lookup"><span data-stu-id="6d835-190">Dolby MAT 1.0:</span></span><br/> <span data-ttu-id="6d835-191">Dolby Труехд (MLP – меридианов без потерь упаковки) — 24-разрядный 192KHz/до 18 Мбит/с, 8 каналов)</span><span class="sxs-lookup"><span data-stu-id="6d835-191">Dolby TrueHD (MLP – Meridian Lossless Packing) – 24-bit 192KHz/up to 18 Mbps, 8 channels)</span></span> <br/> |
| <span data-ttu-id="6d835-192">0x0c</span><span class="sxs-lookup"><span data-stu-id="6d835-192">0x0c</span></span>         | <span data-ttu-id="6d835-193">0000010c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-193">0000010c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-194">\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ MAT20</span><span class="sxs-lookup"><span data-stu-id="6d835-194">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT20</span></span><br/> | <span data-ttu-id="6d835-195">Dolby водо2,0:</span><span class="sxs-lookup"><span data-stu-id="6d835-195">Dolby MAT 2.0:</span></span> <br/> <span data-ttu-id="6d835-196">Dolby Труехд – 24-разрядный 192KHz/до 18 Мбит/с, 8 каналов или ЛПКМ до 24 Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="6d835-196">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="6d835-197">0x0c</span><span class="sxs-lookup"><span data-stu-id="6d835-197">0x0c</span></span>         | <span data-ttu-id="6d835-198">0000030c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-198">0000030c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-199">\_ПОДТИП ксдатаформат \_ IEC61937 \_ Dolby \_ MAT21</span><span class="sxs-lookup"><span data-stu-id="6d835-199">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT21</span></span><br/> | <span data-ttu-id="6d835-200">Dolby водо2,1:</span><span class="sxs-lookup"><span data-stu-id="6d835-200">Dolby MAT 2.1:</span></span> <br/> <span data-ttu-id="6d835-201">Dolby Труехд – 24-разрядный 192KHz/до 18 Мбит/с, 8 каналов или ЛПКМ до 24 Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="6d835-201">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="6d835-202">0x0E</span><span class="sxs-lookup"><span data-stu-id="6d835-202">0x0e</span></span>         | <span data-ttu-id="6d835-203">00000164-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-203">00000164-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-204">\_ПОДТИП ксдатаформат \_ IEC61937 \_ WMA \_ Pro</span><span class="sxs-lookup"><span data-stu-id="6d835-204">KSDATAFORMAT\_SUBTYPE\_IEC61937\_WMA\_PRO</span></span><br/>     | <span data-ttu-id="6d835-205">Windows Media Audio (WMA) Pro</span><span class="sxs-lookup"><span data-stu-id="6d835-205">Windows Media Audio (WMA) Pro</span></span>                                                                                                   |



 

<span data-ttu-id="6d835-206">Драйвер класса HD Audio, предоставляемый корпорацией Майкрософт, поддерживает форматы PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, BI (MLP).</span><span class="sxs-lookup"><span data-stu-id="6d835-206">Microsoft-provided HD Audio class driver supports PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP) formats.</span></span> <span data-ttu-id="6d835-207">Идентификаторы GUID для сжатых звуковых форматов, которые не поддерживаются драйвером класса HD Audio и могут быть реализованы сторонними решениями, перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6d835-207">The GUIDs for the compressed audio formats that are not supported by the HD audio class driver and can be implemented by third-party solutions are listed in the following table.</span></span>



| <span data-ttu-id="6d835-208">Тип CEA 861</span><span class="sxs-lookup"><span data-stu-id="6d835-208">CEA 861 Type</span></span> | <span data-ttu-id="6d835-209">GUID подформата</span><span class="sxs-lookup"><span data-stu-id="6d835-209">SubFormat GUID</span></span>                                                                                              | <span data-ttu-id="6d835-210">Описание</span><span class="sxs-lookup"><span data-stu-id="6d835-210">Description</span></span>                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="6d835-211">0x08</span><span class="sxs-lookup"><span data-stu-id="6d835-211">0x08</span></span>         | <span data-ttu-id="6d835-212">00000008-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-212">00000008-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-213">КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ АТРАК</span><span class="sxs-lookup"><span data-stu-id="6d835-213">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ATRAC</span></span><br/>           | <span data-ttu-id="6d835-214">Акустическое кодирование с адаптивным преобразованием (АТРАК)</span><span class="sxs-lookup"><span data-stu-id="6d835-214">Adaptive Transform Acoustic Coding (ATRAC)</span></span>                                     |
| <span data-ttu-id="6d835-215">0x09</span><span class="sxs-lookup"><span data-stu-id="6d835-215">0x09</span></span>         | <span data-ttu-id="6d835-216">00000009-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-216">00000009-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-217">\_ПОДТИП ксдатаформат \_ IEC61937 \_ один \_ битовый \_ звук</span><span class="sxs-lookup"><span data-stu-id="6d835-217">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ONE\_BIT\_AUDIO</span></span><br/> | <span data-ttu-id="6d835-218">One-Bit звук</span><span class="sxs-lookup"><span data-stu-id="6d835-218">One-Bit Audio</span></span>                                                                  |
| <span data-ttu-id="6d835-219">0x0D</span><span class="sxs-lookup"><span data-stu-id="6d835-219">0x0d</span></span>         | <span data-ttu-id="6d835-220">0000000d-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="6d835-220">0000000d-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="6d835-221">КСДАТАФОРМАТ \_ подтип \_ IEC61937 \_ DST</span><span class="sxs-lookup"><span data-stu-id="6d835-221">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DST</span></span><br/>             | <span data-ttu-id="6d835-222">Прямой потоковый транспорт (DST) — сжатый DSD без потерь (прямая Streaming Digital).</span><span class="sxs-lookup"><span data-stu-id="6d835-222">Direct Stream Transport (DST)—lossless compressed DSD (Direct Stream Digital).</span></span> |



 

## <a name="dolby-digital-plus-format"></a><span data-ttu-id="6d835-223">Формат Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="6d835-223">Dolby Digital Plus Format</span></span>

<span data-ttu-id="6d835-224">Когда содержимое Dolby Digital Plus передается через IEC 60958, скорость выборки ссылок должна быть в четыре раза больше частоты выборки содержимого.</span><span class="sxs-lookup"><span data-stu-id="6d835-224">When Dolby Digital Plus content is transmitted over IEC 60958, the link-sampling rate must be four times the sampling rate of the content.</span></span> <span data-ttu-id="6d835-225">Dolby Digital Plus поддерживает частоту примеров содержимого 32 кГц, 44,1 кГц и 48 кГц.</span><span class="sxs-lookup"><span data-stu-id="6d835-225">Dolby Digital Plus supports content sample rates of 32 KHz, 44.1 KHz, and 48 KHz.</span></span> <span data-ttu-id="6d835-226">Такие интерфейсы, как HDMI, не поддерживают 128 кГц (32 кГц x 4), поэтому поддерживаются только тарифы на выборку содержимого (44,1 и 48 кГц).</span><span class="sxs-lookup"><span data-stu-id="6d835-226">Interfaces such as HDMI do not support 128 KHz (32 KHz x 4), so only 44.1 and 48 KHz content sample rates can be supported.</span></span>

<span data-ttu-id="6d835-227">Значения, заданные приложением в \_ структуре вавеформатекстенсибле IEC61937 для представления формата Dolby Digital Plus с частотой дискретизации 48 кГц, показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6d835-227">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby Digital Plus format at a content sample rate of 48 KHz are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a><span data-ttu-id="6d835-228">Dolby Труехд (с)</span><span class="sxs-lookup"><span data-stu-id="6d835-228">Dolby TrueHD (MAT)</span></span>

<span data-ttu-id="6d835-229">Содержимое Dolby Труехд передается через IEC 60958 в каналах 176,4 кГц/8 (требует частоту кадров IEC 60958, равном 705,6 кГц) для частотных выборок содержимого в 44,1, 88,2 и 176,4 кГц и 192 кГц/8 (требует частоту кадров IEC 60958 в 768 КГц) для частоты дискретизации для примеров содержимого 48, 96 и 192 кГц.</span><span class="sxs-lookup"><span data-stu-id="6d835-229">Dolby TrueHD content is transmitted over IEC 60958 at 176.4 kHz / 8 channels (requiring an IEC 60958 frame rate of 705.6 kHz) for content sample rates of 44.1, 88.2 and 176.4 kHz, and 192 kHz / 8 channels (requiring an IEC 60958 frame rate of 768 kHz) for content sample rates of 48, 96 and 192 kHz.</span></span>

<span data-ttu-id="6d835-230">Значения, заданные приложением в \_ структуре вавеформатекстенсибле IEC61937, чтобы представить Труехд Dolby с частотой дискретизации 96 кГц, показаны в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="6d835-230">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby TrueHD at a content sample rate of 96 KHz are shown in the following examples.</span></span>

<span data-ttu-id="6d835-231">Dolby водо1,0</span><span class="sxs-lookup"><span data-stu-id="6d835-231">Dolby MAT 1.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="6d835-232">Dolby водо2,0</span><span class="sxs-lookup"><span data-stu-id="6d835-232">Dolby MAT 2.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="6d835-233">Dolby водо2,1</span><span class="sxs-lookup"><span data-stu-id="6d835-233">Dolby MAT 2.1</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> <span data-ttu-id="6d835-234">Поддержка одной версии Dolby, не подразумевает поддержки Dolby для управления версиями с более низким номером версии.</span><span class="sxs-lookup"><span data-stu-id="6d835-234">Support for one version of Dolby MAT does not imply support for Dolby MAT with a lower version number.</span></span> <span data-ttu-id="6d835-235">Так как Dolby водо2,1 имеет обратную совместимость с предыдущими версиями функции Dolby, драйвер класса, который указывает на поддержку Dolby водо2,1, обычно также указывает на поддержку Dolby водо2,0 и Dolby водо1,0, используя отдельную \_ структуру вавеформатекстенсибле IEC61937 для каждой версии.</span><span class="sxs-lookup"><span data-stu-id="6d835-235">Since Dolby MAT 2.1 is backwards compatible with previous versions of Dolby MAT, a class driver that indicates support for Dolby MAT 2.1 will typically also indicate support for Dolby MAT 2.0 and Dolby MAT 1.0, using a separate WAVEFORMATEXTENSIBLE\_IEC61937 structure for each version.</span></span>

 

## <a name="wma-pro"></a><span data-ttu-id="6d835-236">WMA Pro</span><span class="sxs-lookup"><span data-stu-id="6d835-236">WMA Pro</span></span>

<span data-ttu-id="6d835-237">Аудио содержимое WMA Pro может быть закодировано в одном из четырех профилей, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6d835-237">WMA Pro audio content can be encoded in one of the four profiles listed in the following table.</span></span>



| <span data-ttu-id="6d835-238">Профиль</span><span class="sxs-lookup"><span data-stu-id="6d835-238">Profile</span></span> | <span data-ttu-id="6d835-239">Свойство-значение</span><span class="sxs-lookup"><span data-stu-id="6d835-239">Property - Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="6d835-240">Описание</span><span class="sxs-lookup"><span data-stu-id="6d835-240">Description</span></span>                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d835-241">Степпинг</span><span class="sxs-lookup"><span data-stu-id="6d835-241">M0</span></span>      | <span data-ttu-id="6d835-242">Максимальная скорость передачи — 192000 бит/с</span><span class="sxs-lookup"><span data-stu-id="6d835-242">Maximum bit rate – 192000 bps</span></span> <br/> <span data-ttu-id="6d835-243">Максимальная частота выборки — 48 кГц</span><span class="sxs-lookup"><span data-stu-id="6d835-243">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="6d835-244">Максимальное число каналов — 2</span><span class="sxs-lookup"><span data-stu-id="6d835-244">Maximum channel count – 2</span></span> <br/> <span data-ttu-id="6d835-245">Максимальный размер буфера — 600 \* 1024 бит</span><span class="sxs-lookup"><span data-stu-id="6d835-245">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="6d835-246">Максимальное число выборок на кадр — 2048</span><span class="sxs-lookup"><span data-stu-id="6d835-246">Maximum samples per frame – 2048</span></span> <br/> <span data-ttu-id="6d835-247">Максимальное число бит на кадр — 655536</span><span class="sxs-lookup"><span data-stu-id="6d835-247">Maximum bits per frame - 655536</span></span><br/>   | <span data-ttu-id="6d835-248">Рекомендуется для воспроизведения музыки и потоковой передачи в эфире.</span><span class="sxs-lookup"><span data-stu-id="6d835-248">Recommended for over-the-air music and streaming.</span></span><br/> <span data-ttu-id="6d835-249">Максимальная скорость потока в звуковой рамке — 1536000 бит/с.</span><span class="sxs-lookup"><span data-stu-id="6d835-249">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/>          |
| <span data-ttu-id="6d835-250">M1</span><span class="sxs-lookup"><span data-stu-id="6d835-250">M1</span></span>      | <span data-ttu-id="6d835-251">Максимальная скорость передачи — 385000 бит/с</span><span class="sxs-lookup"><span data-stu-id="6d835-251">Maximum bit rate – 385000 bps</span></span> <br/> <span data-ttu-id="6d835-252">Максимальная частота выборки — 48 кГц</span><span class="sxs-lookup"><span data-stu-id="6d835-252">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="6d835-253">Максимальное число каналов — 6</span><span class="sxs-lookup"><span data-stu-id="6d835-253">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="6d835-254">Максимальный размер буфера — 600 \* 1024 бит</span><span class="sxs-lookup"><span data-stu-id="6d835-254">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="6d835-255">Максимальное число выборок на кадр — 4096</span><span class="sxs-lookup"><span data-stu-id="6d835-255">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="6d835-256">Максимальное число бит на кадр — 131072</span><span class="sxs-lookup"><span data-stu-id="6d835-256">Maximum bits per frame - 131072</span></span><br/>   | <span data-ttu-id="6d835-257">Рекомендуется для фильмов с определением стандартных звуковых эффектов.</span><span class="sxs-lookup"><span data-stu-id="6d835-257">Recommended for surround-sound standard definition movies.</span></span><br/> <span data-ttu-id="6d835-258">Максимальная скорость потока в звуковой рамке — 1536000 бит/с.</span><span class="sxs-lookup"><span data-stu-id="6d835-258">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/> |
| <span data-ttu-id="6d835-259">M2</span><span class="sxs-lookup"><span data-stu-id="6d835-259">M2</span></span>      | <span data-ttu-id="6d835-260">Максимальная скорость передачи — 769000 бит/с</span><span class="sxs-lookup"><span data-stu-id="6d835-260">Maximum bit rate – 769000 bps</span></span> <br/> <span data-ttu-id="6d835-261">Максимальная частота выборки — 96 кГц</span><span class="sxs-lookup"><span data-stu-id="6d835-261">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="6d835-262">Максимальное число каналов — 6</span><span class="sxs-lookup"><span data-stu-id="6d835-262">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="6d835-263">Максимальный размер буфера — 1200 \* 1024 бит</span><span class="sxs-lookup"><span data-stu-id="6d835-263">Maximum buffer size – 1200\*1024 bits</span></span> <br/> <span data-ttu-id="6d835-264">Максимальное число выборок на кадр — 4096</span><span class="sxs-lookup"><span data-stu-id="6d835-264">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="6d835-265">Максимальное число бит на кадр — 131072</span><span class="sxs-lookup"><span data-stu-id="6d835-265">Maximum bits per frame - 131072</span></span><br/>  | <span data-ttu-id="6d835-266">Рекомендуется для фильмов с высокой степенью четкости.</span><span class="sxs-lookup"><span data-stu-id="6d835-266">Recommended for surround-sound high definition movies.</span></span><br/> <span data-ttu-id="6d835-267">Максимальная скорость в звуковой рамке — 3072000 бит/с.</span><span class="sxs-lookup"><span data-stu-id="6d835-267">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>         |
| <span data-ttu-id="6d835-268">M3</span><span class="sxs-lookup"><span data-stu-id="6d835-268">M3</span></span>      | <span data-ttu-id="6d835-269">Максимальная скорость передачи — 3000000 бит/с</span><span class="sxs-lookup"><span data-stu-id="6d835-269">Maximum bit rate – 3000000 bps</span></span> <br/> <span data-ttu-id="6d835-270">Максимальная частота выборки — 96 кГц</span><span class="sxs-lookup"><span data-stu-id="6d835-270">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="6d835-271">Максимальное число каналов — 8</span><span class="sxs-lookup"><span data-stu-id="6d835-271">Maximum channel count – 8</span></span> <br/> <span data-ttu-id="6d835-272">Максимальный размер буфера — 2400 \* 1024 бит</span><span class="sxs-lookup"><span data-stu-id="6d835-272">Maximum buffer size – 2400\*1024 bits</span></span> <br/> <span data-ttu-id="6d835-273">Максимальное число выборок на кадр — 4096</span><span class="sxs-lookup"><span data-stu-id="6d835-273">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="6d835-274">Максимальное число бит на кадр — 131072</span><span class="sxs-lookup"><span data-stu-id="6d835-274">Maximum bits per frame - 131072</span></span><br/> | <span data-ttu-id="6d835-275">Рекомендуется для цифрового кинотеатра.</span><span class="sxs-lookup"><span data-stu-id="6d835-275">Recommended for digital theater.</span></span><br/> <span data-ttu-id="6d835-276">Максимальная скорость в звуковой рамке — 3072000 бит/с.</span><span class="sxs-lookup"><span data-stu-id="6d835-276">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>                               |



 

<span data-ttu-id="6d835-277">Профили M0 и M1 соответствуют потоку 48 кГц/16 бит/стерео (1536000 бит/с) IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="6d835-277">The M0 and M1 profiles fit into a 48 KHz/16 bit/Stereo (1536000 bps) IEC 60958 stream.</span></span> <span data-ttu-id="6d835-278">Профили m2 и M3 соответствуют потоку 96 кГц/16 бит/стерео (3072000 бит/с) IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="6d835-278">The M2 and M3 profiles fit into a 96 KHz/16 bit/Stereo (3072000 bps) IEC 60958 stream.</span></span>

<span data-ttu-id="6d835-279">Значения, заданные приложением в \_ структуре вавеформатекстенсибле IEC61937 для представления WMA Pro в качестве профиля m2, показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6d835-279">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent WMA Pro as an M2 profile are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a><span data-ttu-id="6d835-280">См. также</span><span class="sxs-lookup"><span data-stu-id="6d835-280">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d835-281">Форматы устройств</span><span class="sxs-lookup"><span data-stu-id="6d835-281">Device Formats</span></span>](device-formats.md)
</dt> </dl>

 

 




