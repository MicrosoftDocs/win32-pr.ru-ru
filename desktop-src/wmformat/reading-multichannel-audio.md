---
title: Чтение многоканального звука
description: Чтение многоканального звука
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, чтение многоканального звука
- Расширенный формат систем (ASF), чтение многоканального звука
- ASF (Расширенный системный формат), чтение многоканального звука
- Расширенный формат систем (ASF), многоканальный звук
- ASF (Расширенный системный формат), многоканальный звук
- кодеки, чтение многоканального звука
- многоканальное аудио, чтение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793242"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="ae0bb-110">Чтение многоканального звука</span><span class="sxs-lookup"><span data-stu-id="ae0bb-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="ae0bb-111">Кодек Windows Media Audio 9 Professional позволяет кодировать многоканальное аудио (более двух каналов).</span><span class="sxs-lookup"><span data-stu-id="ae0bb-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="ae0bb-112">При чтении файла с многоканальным звуком необходимо правильно настроить выходные данные, а звук будет доставляться с более низким качеством и стерео.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="ae0bb-113">Чтобы задать выходные данные для многоканальной звуковой доставки, необходимо задать два выходных параметра: g \_ всзенабледискретеаутпут и g \_ всзспеакерконфиг.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="ae0bb-114">Установка параметра g \_ всзенабледискретеаутпут в **значение true** задает кодек для доставки звуковых данных высокой четкости.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="ae0bb-115">Звук с высокой степенью четкости кодируется кодеком Windows Media Audio 9 с 24-разрядными примерами на стерео или нескольких каналах.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="ae0bb-116">Если этот параметр имеет **значение false**, будут доставляться только 16-разрядные выходные данные стерео.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="ae0bb-117">Число динамиков на воспроизводимом компьютере задается с помощью g \_ всзспеакерконфиг.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="ae0bb-118">Этот параметр имеет значение **DWORD** , равное одной из констант динамика DirectSound, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="ae0bb-119">Чтобы разрешить эти константные имена для компилятора, необходимо включить дсаунд. h.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="ae0bb-120">Константа</span><span class="sxs-lookup"><span data-stu-id="ae0bb-120">Constant</span></span>             | <span data-ttu-id="ae0bb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ae0bb-121">Value</span></span>      | <span data-ttu-id="ae0bb-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ae0bb-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ae0bb-123">ДССПЕАКЕР \_</span><span class="sxs-lookup"><span data-stu-id="ae0bb-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="ae0bb-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae0bb-124">0x00000000</span></span> | <span data-ttu-id="ae0bb-125">Звук передается напрямую, без настройки для динамиков.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="ae0bb-126">\_наушники дсспеакер</span><span class="sxs-lookup"><span data-stu-id="ae0bb-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="ae0bb-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae0bb-127">0x00000001</span></span> | <span data-ttu-id="ae0bb-128">Клиентский компьютер оснащен наушниками.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="ae0bb-129">ДССПЕАКЕР \_ Mono</span><span class="sxs-lookup"><span data-stu-id="ae0bb-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="ae0bb-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ae0bb-130">0x00000002</span></span> | <span data-ttu-id="ae0bb-131">Клиентский компьютер оснащен монауралным докладчиком.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="ae0bb-132">ДССПЕАКЕР \_ Quad</span><span class="sxs-lookup"><span data-stu-id="ae0bb-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="ae0bb-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ae0bb-133">0x00000003</span></span> | <span data-ttu-id="ae0bb-134">Клиентский компьютер оснащен куадрафоник колонками.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="ae0bb-135">\_стерео дсспеакер</span><span class="sxs-lookup"><span data-stu-id="ae0bb-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="ae0bb-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ae0bb-136">0x00000004</span></span> | <span data-ttu-id="ae0bb-137">Клиентский компьютер оснащен стереодинамиками.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="ae0bb-138">ДССПЕАКЕР \_ вокруг</span><span class="sxs-lookup"><span data-stu-id="ae0bb-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="ae0bb-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ae0bb-139">0x00000005</span></span> | <span data-ttu-id="ae0bb-140">Клиентский компьютер оснащен динамиками с четырьмя каналами.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="ae0bb-141">ДССПЕАКЕР \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="ae0bb-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="ae0bb-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="ae0bb-142">0x00000006</span></span> | <span data-ttu-id="ae0bb-143">Клиентский компьютер оснащен пятью динамиками и сабвуфером.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="ae0bb-144">ДССПЕАКЕР \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="ae0bb-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="ae0bb-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="ae0bb-145">0x00000007</span></span> | <span data-ttu-id="ae0bb-146">Клиентский компьютер оснащен семью динамиками и сабвуфером.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="ae0bb-147">Чтобы задать эти параметры, используйте [**IWMReaderAdvanced2:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="ae0bb-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="ae0bb-148">Наконец, для вывода каналов дискретными без свертывания в стерео необходимо задать правильный тип носителя для выходных данных, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="ae0bb-149">Вызовите метод [**ивмреадер:: жетаутпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) , чтобы получить количество поддерживаемых форматов для соответствующих выходных данных звука.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="ae0bb-150">Индексы формата выходных данных отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="ae0bb-151">Для каждого поддерживаемого формата вызовите [**ивмреадер:: жетаутпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) , чтобы получить интерфейс [**ивмаутпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) в выходном объекте свойств мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="ae0bb-152">Вызовите [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) , чтобы получить тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="ae0bb-153">Если полученный тип мультимедиа является нужным типом многоканального типа, установите его, вызвав [**ивмреадер:: сетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span><span class="sxs-lookup"><span data-stu-id="ae0bb-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="ae0bb-154">После установки дискретных выходных данных и конфигурации динамиков выходные форматы, перечисленные модулем чтения, должны включать многоканальные форматы, в которых используется структура [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae0bb-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="ae0bb-155">Если перечислить форматы вывода перед заданием свойств, то будут включаться только форматы с 1 или 2 каналами и максимум 16 бит на канал.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="ae0bb-156">Как и в случае с другими звуковыми форматами, следует использовать только форматы, перечисленные в модуле чтения. не настраивайте собственный.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="ae0bb-157">Вы можете вывести многоканальный звук только в том случае, если приложение работает под управлением Microsoft Windows XP или более поздней версии Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ae0bb-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ae0bb-158">См. также</span><span class="sxs-lookup"><span data-stu-id="ae0bb-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae0bb-159">**Входы, потоки и выходные данные**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="ae0bb-160">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="ae0bb-161">**Параметры вывода**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="ae0bb-162">**Работа с аудио High-Resolution PCM**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 