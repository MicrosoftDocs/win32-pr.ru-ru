---
description: Декодер MP3 Windows Media декодирует звуковые файлы, закодированные в следующих форматах.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Декодер MP3 Windows Media (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699074"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="1e4e6-103">Декодер MP3 Windows Media</span><span class="sxs-lookup"><span data-stu-id="1e4e6-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="1e4e6-104">Декодер MP3 Windows Media декодирует звуковые файлы, закодированные в следующих форматах.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="1e4e6-105">ISO/IEC 11172-3 (аудио MPEG-1), уровень 3</span><span class="sxs-lookup"><span data-stu-id="1e4e6-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="1e4e6-106">Стандарт ISO/IEC 13818-3 (MPEG-2 Audio), низкое расширение частоты выборки</span><span class="sxs-lookup"><span data-stu-id="1e4e6-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1e4e6-107">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="1e4e6-107">Class Identifier</span></span>

<span data-ttu-id="1e4e6-108">Идентификатор класса (CLSID) для декодера MP3 Windows Media представлен константой **CLSID \_ CMP3DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="1e4e6-109">Вы можете создать экземпляр декодера MP3, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="1e4e6-110">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1e4e6-110">Interfaces</span></span>

<span data-ttu-id="1e4e6-111">Объект декодера MP3 предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="1e4e6-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="1e4e6-112">Декодер MP3 Windows Media ведет себя как DMO или MFT в зависимости от того, какие интерфейсы получены и какая версия Windows работает.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="1e4e6-113">В следующей таблице показаны условия, при которых декодер MP3 Windows Media ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="1e4e6-114">Операционная система</span><span class="sxs-lookup"><span data-stu-id="1e4e6-114">Operating system</span></span> | <span data-ttu-id="1e4e6-115">Поведение декодера</span><span class="sxs-lookup"><span data-stu-id="1e4e6-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4e6-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e4e6-116">Windows XP</span></span>       | <span data-ttu-id="1e4e6-117">Декодер MP3 Windows Media всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="1e4e6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e4e6-118">Windows Vista</span></span>    | <span data-ttu-id="1e4e6-119">По умолчанию декодер MP3 Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="1e4e6-120">Если вы получаете интерфейс **имфтрансформ** или интерфейс **ипропертисторе** в декодере MP3 Windows Media, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="1e4e6-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e4e6-121">Windows 7</span></span>        | <span data-ttu-id="1e4e6-122">По умолчанию декодер MP3 Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="1e4e6-123">Если вы получаете интерфейс **имфтрансформ** для декодера MP3 Windows Media, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="1e4e6-124">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="1e4e6-124">Input Formats</span></span>

<span data-ttu-id="1e4e6-125">В следующей таблице показан тег формата аудио, который представляет тип входных данных, поддерживаемый декодером MP3 Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="1e4e6-126">Формат константы тега</span><span class="sxs-lookup"><span data-stu-id="1e4e6-126">Format tag constant</span></span>      | <span data-ttu-id="1e4e6-127">Формат значения тега</span><span class="sxs-lookup"><span data-stu-id="1e4e6-127">Format tag value</span></span> | <span data-ttu-id="1e4e6-128">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="1e4e6-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="1e4e6-129">\_Формат волны \_ MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="1e4e6-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="1e4e6-130">0x55</span><span class="sxs-lookup"><span data-stu-id="1e4e6-130">0x55</span></span>             | <span data-ttu-id="1e4e6-131">ISO MPEG, уровень 3</span><span class="sxs-lookup"><span data-stu-id="1e4e6-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="1e4e6-132">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="1e4e6-132">Output Formats</span></span>

<span data-ttu-id="1e4e6-133">В следующей таблице показаны Теги звукового формата, представляющие типы выходных данных, поддерживаемые декодером MP3 Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="1e4e6-134">Формат константы тега</span><span class="sxs-lookup"><span data-stu-id="1e4e6-134">Format tag constant</span></span>       | <span data-ttu-id="1e4e6-135">Формат значения тега</span><span class="sxs-lookup"><span data-stu-id="1e4e6-135">Format tag value</span></span> | <span data-ttu-id="1e4e6-136">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="1e4e6-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1e4e6-137">формат ВОЛНового \_ \_ PCM</span><span class="sxs-lookup"><span data-stu-id="1e4e6-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="1e4e6-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="1e4e6-138">0x0001</span></span>           | <span data-ttu-id="1e4e6-139">Формат PCM (при использовании в качестве DMO или MFT)</span><span class="sxs-lookup"><span data-stu-id="1e4e6-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="1e4e6-140">\_Формат волны \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="1e4e6-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="1e4e6-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="1e4e6-141">0x0003</span></span>           | <span data-ttu-id="1e4e6-142">IEEE с плавающей запятой (при использовании в MFT)</span><span class="sxs-lookup"><span data-stu-id="1e4e6-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="1e4e6-143">формат ВОЛНового \_ \_ расширения</span><span class="sxs-lookup"><span data-stu-id="1e4e6-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="1e4e6-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="1e4e6-144">0xFFFE</span></span>           | <span data-ttu-id="1e4e6-145">Формат PCM/IEEE в структуре **вавеформатекстенсибле** (при использовании в файле MFT)</span><span class="sxs-lookup"><span data-stu-id="1e4e6-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="1e4e6-146">Декодер MP3 Windows Media поддерживает и перечисляет следующие типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="1e4e6-147">Тип выходных данных, который имеет ту же частоту выборки и число каналов, что и тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="1e4e6-148">Выходные данные моно для стерео ввода.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="1e4e6-149">Типы выходных данных с битовыми глубиной 8 и 16.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="1e4e6-150">Вывод с плавающей запятой, если декодер ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="1e4e6-151">Декодер MP3 Windows Media поддерживает, но не перечисляет следующие типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="1e4e6-152">Тип вывода с половиной частоты выборки входного типа.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="1e4e6-153">Тип выходных данных, который имеет одну четвертую частоту выборки для типа входных данных.</span><span class="sxs-lookup"><span data-stu-id="1e4e6-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4e6-154">Требования</span><span class="sxs-lookup"><span data-stu-id="1e4e6-154">Requirements</span></span>



| <span data-ttu-id="1e4e6-155">Требование</span><span class="sxs-lookup"><span data-stu-id="1e4e6-155">Requirement</span></span> | <span data-ttu-id="1e4e6-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1e4e6-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4e6-157">Клиент</span><span class="sxs-lookup"><span data-stu-id="1e4e6-157">Client</span></span><br/> | <span data-ttu-id="1e4e6-158">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e4e6-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="1e4e6-159">Header</span><span class="sxs-lookup"><span data-stu-id="1e4e6-159">Header</span></span><br/> | <dl> <span data-ttu-id="1e4e6-160"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4e6-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1e4e6-161">DLL</span><span class="sxs-lookup"><span data-stu-id="1e4e6-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="1e4e6-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e4e6-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1e4e6-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e4e6-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4e6-164">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="1e4e6-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1e4e6-165">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="1e4e6-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




