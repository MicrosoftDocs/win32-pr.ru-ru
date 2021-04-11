---
title: запись, команда
description: Команда Record запускает запись данных. Видеозаписывающие устройства и аудио-файлы распознают эту команду. Несмотря на то, что Цифровые видеоустройства и средства нумерации MIDI также распознают эту команду, драйверы МЦИАВИ и МЦИСЕК не реализуют их.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- запись команды мультимедиа Windows
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891473"
---
# <a name="record-command"></a><span data-ttu-id="2f583-106">запись, команда</span><span class="sxs-lookup"><span data-stu-id="2f583-106">record command</span></span>

<span data-ttu-id="2f583-107">Команда Record запускает запись данных.</span><span class="sxs-lookup"><span data-stu-id="2f583-107">The record command starts recording data.</span></span> <span data-ttu-id="2f583-108">Видеозаписывающие устройства и аудио-файлы распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="2f583-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="2f583-109">Несмотря на то, что Цифровые видеоустройства и средства нумерации MIDI также распознают эту команду, драйверы МЦИАВИ и МЦИСЕК не реализуют их.</span><span class="sxs-lookup"><span data-stu-id="2f583-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="2f583-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="2f583-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="2f583-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f583-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f583-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="2f583-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2f583-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="2f583-113">Identifier of an MCI device.</span></span> <span data-ttu-id="2f583-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="2f583-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="2f583-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*лпсзрекордфлагс*</span><span class="sxs-lookup"><span data-stu-id="2f583-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2f583-116">Флаг для записи данных.</span><span class="sxs-lookup"><span data-stu-id="2f583-116">Flag for recording data.</span></span> <span data-ttu-id="2f583-117">В следующей таблице перечислены типы устройств, которые распознают команду **записи** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="2f583-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="2f583-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2f583-118">Value</span></span>        | <span data-ttu-id="2f583-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2f583-119">Meaning</span></span>                                                | <span data-ttu-id="2f583-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2f583-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="2f583-121">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="2f583-121">digitalvideo</span></span> | <span data-ttu-id="2f583-122">поток *аудиопотока* потокового потока из удержания *позиции*</span><span class="sxs-lookup"><span data-stu-id="2f583-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="2f583-123">вставить перезапись в  *поток* видео потока</span><span class="sxs-lookup"><span data-stu-id="2f583-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="2f583-124">sequencer</span><span class="sxs-lookup"><span data-stu-id="2f583-124">sequencer</span></span>    | <span data-ttu-id="2f583-125">от вставки *расположения*</span><span class="sxs-lookup"><span data-stu-id="2f583-125">from *position* insert</span></span>                                  | <span data-ttu-id="2f583-126">перезапись в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="2f583-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="2f583-127">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="2f583-127">vcr</span></span>          | <span data-ttu-id="2f583-128">во *время* инициализации *позиции*</span><span class="sxs-lookup"><span data-stu-id="2f583-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="2f583-129">вставить перезапись в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="2f583-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="2f583-130">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="2f583-130">waveaudio</span></span>    | <span data-ttu-id="2f583-131">от вставки *расположения*</span><span class="sxs-lookup"><span data-stu-id="2f583-131">from *position* insert</span></span>                                  | <span data-ttu-id="2f583-132">перезапись в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="2f583-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="2f583-133">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзрекордфлагс** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="2f583-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="2f583-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2f583-134">Value</span></span>                 | <span data-ttu-id="2f583-135">Значение</span><span class="sxs-lookup"><span data-stu-id="2f583-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f583-136">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="2f583-136">at *rectangle*</span></span>        | <span data-ttu-id="2f583-137">Задает прямоугольную область внешних входных данных, используемую в качестве источника для сжатых и сохраняемых пикселей.</span><span class="sxs-lookup"><span data-stu-id="2f583-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="2f583-138">Если не указано, прямоугольником по умолчанию является прямоугольник, указанный для [размещения](put.md) "Video".</span><span class="sxs-lookup"><span data-stu-id="2f583-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="2f583-139">Если это значение отличается от прямоугольника "видео", отображаемое изображение не будет записано.</span><span class="sxs-lookup"><span data-stu-id="2f583-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="2f583-140">в *момент времени*</span><span class="sxs-lookup"><span data-stu-id="2f583-140">at *time*</span></span>             | <span data-ttu-id="2f583-141">Указывает, когда устройство должно начать выполнение этой команды, или, если устройство было куед, при запуске команды куед.</span><span class="sxs-lookup"><span data-stu-id="2f583-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="2f583-142">Дополнительные сведения см. в описании команды [Cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="2f583-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="2f583-143">*поток* аудиопотока</span><span class="sxs-lookup"><span data-stu-id="2f583-143">audio stream *stream*</span></span> | <span data-ttu-id="2f583-144">Указывает аудиопоток, используемый для записи.</span><span class="sxs-lookup"><span data-stu-id="2f583-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="2f583-145">Если этот флаг не указан и формат файла не определяет значение по умолчанию, он записывается в поток, который физически является первым.</span><span class="sxs-lookup"><span data-stu-id="2f583-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="2f583-146">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="2f583-146">from *position*</span></span>       | <span data-ttu-id="2f583-147">Задает начальную точку записи.</span><span class="sxs-lookup"><span data-stu-id="2f583-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="2f583-148">Если не указан флаг "from", устройство начинает запись в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="2f583-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="2f583-149">Нажмите</span><span class="sxs-lookup"><span data-stu-id="2f583-149">hold</span></span>                  | <span data-ttu-id="2f583-150">Закрепляет образ при завершении записи, а не отображая видео в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="2f583-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="2f583-151">При остановке записи выполняется команда автоматического [мониторинга](monitor.md) "файл".</span><span class="sxs-lookup"><span data-stu-id="2f583-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="2f583-152">Чтобы вернуться в динамическое видео, выполните команду **Monitor** "input".</span><span class="sxs-lookup"><span data-stu-id="2f583-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="2f583-153">устанавливает</span><span class="sxs-lookup"><span data-stu-id="2f583-153">initialize</span></span>            | <span data-ttu-id="2f583-154">Инициализируйте ленту (носитель), которая включает в себя запись времени (если возможно) для пустого видео и звука.</span><span class="sxs-lookup"><span data-stu-id="2f583-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="2f583-155">Выполнение этой команды может занять несколько часов, если вся лента должна быть инициализирована.</span><span class="sxs-lookup"><span data-stu-id="2f583-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="2f583-156">insert</span><span class="sxs-lookup"><span data-stu-id="2f583-156">insert</span></span>                | <span data-ttu-id="2f583-157">Указывает, что новые данные добавляются в файл в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="2f583-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="2f583-158">перезапись</span><span class="sxs-lookup"><span data-stu-id="2f583-158">overwrite</span></span>             | <span data-ttu-id="2f583-159">Указывает, что новые данные будут заменять данные в файле.</span><span class="sxs-lookup"><span data-stu-id="2f583-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2f583-160">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="2f583-160">to *position*</span></span>         | <span data-ttu-id="2f583-161">Задает конечную точку записи.</span><span class="sxs-lookup"><span data-stu-id="2f583-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="2f583-162">Если флаг "to" не указан, устройство записывается до получения команды [остановки](stop.md) или [приостановки](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="2f583-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="2f583-163">*поток* видео поток</span><span class="sxs-lookup"><span data-stu-id="2f583-163">video stream *stream*</span></span> | <span data-ttu-id="2f583-164">Указывает поток видео, используемый для записи.</span><span class="sxs-lookup"><span data-stu-id="2f583-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="2f583-165">Если этот параметр не указан и формат файла не определяет значение по умолчанию, он записывается в поток, который физически является первым.</span><span class="sxs-lookup"><span data-stu-id="2f583-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="2f583-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="2f583-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2f583-167">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="2f583-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="2f583-168">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="2f583-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="2f583-169">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2f583-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f583-170">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f583-170">Return Value</span></span>

<span data-ttu-id="2f583-171">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2f583-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f583-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f583-172">Remarks</span></span>

<span data-ttu-id="2f583-173">Запись останавливается при выдаче команды [Stop](stop.md) или [Pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="2f583-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="2f583-174">Для драйвера МЦИВАВЕ все данные, записанные после открытия файла, отбрасываются, если файл закрывается без сохранения.</span><span class="sxs-lookup"><span data-stu-id="2f583-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="2f583-175">Перед выполнением команд, использующих значения позиций, необходимо задать требуемый формат времени с помощью команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="2f583-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="2f583-176">Записываемые дорожки задаются [сеттимекоде](settimecode.md) "запись", устанавливаются команды "собрать запись", [сетвидео](setvideo.md) "Record" и [сетаудио](setaudio.md) "Record".</span><span class="sxs-lookup"><span data-stu-id="2f583-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="2f583-177">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f583-177">Examples</span></span>

<span data-ttu-id="2f583-178">Следующая команда запускает запись в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="2f583-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="2f583-179">Требования</span><span class="sxs-lookup"><span data-stu-id="2f583-179">Requirements</span></span>



| <span data-ttu-id="2f583-180">Требование</span><span class="sxs-lookup"><span data-stu-id="2f583-180">Requirement</span></span> | <span data-ttu-id="2f583-181">Значение</span><span class="sxs-lookup"><span data-stu-id="2f583-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2f583-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f583-182">Minimum supported client</span></span><br/> | <span data-ttu-id="2f583-183">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f583-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2f583-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f583-184">Minimum supported server</span></span><br/> | <span data-ttu-id="2f583-185">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f583-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2f583-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f583-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f583-187">MCI</span><span class="sxs-lookup"><span data-stu-id="2f583-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f583-188">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="2f583-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="2f583-189">cue</span><span class="sxs-lookup"><span data-stu-id="2f583-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="2f583-190">слежен</span><span class="sxs-lookup"><span data-stu-id="2f583-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="2f583-191">pause</span><span class="sxs-lookup"><span data-stu-id="2f583-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="2f583-192">PUT</span><span class="sxs-lookup"><span data-stu-id="2f583-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="2f583-193">set</span><span class="sxs-lookup"><span data-stu-id="2f583-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="2f583-194">сетаудио</span><span class="sxs-lookup"><span data-stu-id="2f583-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="2f583-195">сеттимекоде</span><span class="sxs-lookup"><span data-stu-id="2f583-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="2f583-196">сетвидео</span><span class="sxs-lookup"><span data-stu-id="2f583-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="2f583-197">stop</span><span class="sxs-lookup"><span data-stu-id="2f583-197">stop</span></span>](stop.md)
</dt> </dl>

 

