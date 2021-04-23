---
description: Кодировщик Windows Media Audio Voice оптимизирован для кодирования человеческого голоса при высоком коэффициенте сжатия. Это предпочтительный кодировщик для потоков, состоящих в основном на произнесенных словах.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Кодировщик Windows Media Audio Voice (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699070"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="cbdec-104">Кодировщик Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="cbdec-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="cbdec-105">Кодировщик Windows Media Audio Voice оптимизирован для кодирования человеческого голоса при высоком коэффициенте сжатия.</span><span class="sxs-lookup"><span data-stu-id="cbdec-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="cbdec-106">Это предпочтительный кодировщик для потоков, состоящих в основном на произнесенных словах.</span><span class="sxs-lookup"><span data-stu-id="cbdec-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="cbdec-107">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="cbdec-107">Class Identifier</span></span>

<span data-ttu-id="cbdec-108">Идентификатор класса (CLSID) для кодировщика Windows Media Audio Voice представлен константой **CLSID \_ CWMSPEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="cbdec-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="cbdec-109">Экземпляр речевого кодировщика можно создать, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="cbdec-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="cbdec-110">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="cbdec-110">Output Formats</span></span>

<span data-ttu-id="cbdec-111">Содержимое в кодировке Windows Media Audio Voice определяется тегом формата 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbdec-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="cbdec-112">Свойства кодировщика</span><span class="sxs-lookup"><span data-stu-id="cbdec-112">Encoder Properties</span></span>

<span data-ttu-id="cbdec-113">Кодировщик Windows Media Audio Voice поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cbdec-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cbdec-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="cbdec-114">Property</span></span></th>
<th><span data-ttu-id="cbdec-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cbdec-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbdec-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="cbdec-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="cbdec-117">Указывает окно буфера (в миллисекундах), используемое для речевого кодека.</span><span class="sxs-lookup"><span data-stu-id="cbdec-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="cbdec-118">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="cbdec-118">Windows XP and later.</span></span><br />
<span data-ttu-id="cbdec-119">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="cbdec-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbdec-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="cbdec-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="cbdec-121">Указывает задержку кодировщика в единицах пакетов.</span><span class="sxs-lookup"><span data-stu-id="cbdec-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="cbdec-122">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="cbdec-122">Windows XP and later.</span></span><br />
<span data-ttu-id="cbdec-123">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="cbdec-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbdec-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="cbdec-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="cbdec-125">Указывает фрагменты содержимого, которые должны быть закодированы голосовым кодеком в качестве музыки.</span><span class="sxs-lookup"><span data-stu-id="cbdec-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="cbdec-126">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="cbdec-126">Windows XP and later.</span></span><br />
<span data-ttu-id="cbdec-127">Read/write.</span><span class="sxs-lookup"><span data-stu-id="cbdec-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbdec-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="cbdec-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="cbdec-129">Задает режим работы с голосовым кодеком.</span><span class="sxs-lookup"><span data-stu-id="cbdec-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="cbdec-130">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="cbdec-130">Windows XP and later.</span></span><br />
<span data-ttu-id="cbdec-131">Read/write.</span><span class="sxs-lookup"><span data-stu-id="cbdec-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cbdec-132">Требования</span><span class="sxs-lookup"><span data-stu-id="cbdec-132">Requirements</span></span>



| <span data-ttu-id="cbdec-133">Требование</span><span class="sxs-lookup"><span data-stu-id="cbdec-133">Requirement</span></span> | <span data-ttu-id="cbdec-134">Значение</span><span class="sxs-lookup"><span data-stu-id="cbdec-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdec-135">Клиент</span><span class="sxs-lookup"><span data-stu-id="cbdec-135">Client</span></span><br/> | <span data-ttu-id="cbdec-136">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbdec-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="cbdec-137">Header</span><span class="sxs-lookup"><span data-stu-id="cbdec-137">Header</span></span><br/> | <dl> <span data-ttu-id="cbdec-138"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbdec-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="cbdec-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cbdec-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="cbdec-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbdec-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbdec-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbdec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdec-142">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="cbdec-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="cbdec-143">Использование кодека Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="cbdec-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




