---
description: Использование High-Definition Audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Использование High-Definition Audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812580"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="bb742-103">Использование High-Definition Audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="bb742-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="bb742-104">Высококачественное аудио, в контексте кодеков Windows Media Audio, — это любой тип звука с более чем двумя каналами или более 16 бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="bb742-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="bb742-105">Высококачественное аудио поддерживается в категориях "профессиональная" и "без потерь" [кодировщика Windows Media Audio](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="bb742-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="bb742-106">Несжатые звуковые типы высокой четкости определяются с помощью структуры [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bb742-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="bb742-107">**Вавеформатекстенсибле** — это структурированное расширение структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bb742-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="bb742-108">При использовании дмос элемент **форматтипе** структуры [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) , описывающий тип звука высокой четкости, должен иметь значение вмкформат \_ вавеформатекс, как и для обычного звука; для **вавеформатекстенсибле** не существует специального идентификатора формата.</span><span class="sxs-lookup"><span data-stu-id="bb742-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="bb742-109">Если в формате используется **вавеформатекстенсибле** , необходимо задать для элемента **кбсизе** структуры **вавеформатекс** значение 22.</span><span class="sxs-lookup"><span data-stu-id="bb742-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="bb742-110">При использовании Media Foundation можно создать правильный тип мультимедиа из структуры [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) с помощью функции [**мфинитмедиатипефромвавеформатекс**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span><span class="sxs-lookup"><span data-stu-id="bb742-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="bb742-111">Многоканальные типы вывода, поддерживаемые кодеком Windows Media Audio 10 Professional, не используют [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), но сообщают правильное количество каналов и бит на выборку в структуре [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bb742-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="bb742-112">Как и для всех типов аудио, описывающих сжатое аудио-содержимое Windows Media, в структуру **вавеформатекс** , используемую декодером для распаковки, добавлены дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="bb742-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="bb742-113">Декодирование High-Definition аудио</span><span class="sxs-lookup"><span data-stu-id="bb742-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="bb742-114">Для расшифровки звука высокой четкости необходимо задать для свойства [мфпкэй \_ вмадек \_ хиресаутпут](mfpkey-wmadec-hiresoutputproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="bb742-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="bb742-115">Если это свойство не задано, декодер будет доставлять стерео-содержимое максимум 16 бит на выборку независимо от сжатого формата.</span><span class="sxs-lookup"><span data-stu-id="bb742-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="bb742-116">High-Definition Audio поддерживается только для Windows XP, Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="bb742-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="bb742-117">В более ранних версиях Windows аудио-содержимое Windows Media, закодированное с помощью High Definition, отображается в виде двухканального звука с максимум 16 бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="bb742-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bb742-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bb742-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb742-119">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="bb742-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
