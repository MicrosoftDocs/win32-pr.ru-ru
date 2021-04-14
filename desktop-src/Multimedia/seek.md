---
title: Seek, команда
description: Команда Seek перемещается в указанную положение и останавливается. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- команда поиска мультимедиа Windows
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414800"
---
# <a name="seek-command"></a><span data-ttu-id="304c1-105">Seek, команда</span><span class="sxs-lookup"><span data-stu-id="304c1-105">seek command</span></span>

<span data-ttu-id="304c1-106">Команда Seek перемещается в указанную положение и останавливается.</span><span class="sxs-lookup"><span data-stu-id="304c1-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="304c1-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="304c1-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="304c1-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="304c1-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="304c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="304c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="304c1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="304c1-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="304c1-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="304c1-111">Identifier of an MCI device.</span></span> <span data-ttu-id="304c1-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="304c1-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="304c1-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*лпсзсикфлагс*</span><span class="sxs-lookup"><span data-stu-id="304c1-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="304c1-114">Флаг для перемещения в указанную точку.</span><span class="sxs-lookup"><span data-stu-id="304c1-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="304c1-115">В следующей таблице перечислены типы устройств, которые распознают команду **Seek** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="304c1-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="304c1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="304c1-116">Value</span></span>        | <span data-ttu-id="304c1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="304c1-117">Meaning</span></span>                          | <span data-ttu-id="304c1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="304c1-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="304c1-119">кдаудио</span><span class="sxs-lookup"><span data-stu-id="304c1-119">cdaudio</span></span>      | <span data-ttu-id="304c1-120">*до конца*</span><span class="sxs-lookup"><span data-stu-id="304c1-120">to end to *position*</span></span>             | <span data-ttu-id="304c1-121">для начала</span><span class="sxs-lookup"><span data-stu-id="304c1-121">to start</span></span>                     |
| <span data-ttu-id="304c1-122">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="304c1-122">digitalvideo</span></span> | <span data-ttu-id="304c1-123">*до конца*</span><span class="sxs-lookup"><span data-stu-id="304c1-123">to end to *position*</span></span>             | <span data-ttu-id="304c1-124">для начала</span><span class="sxs-lookup"><span data-stu-id="304c1-124">to start</span></span>                     |
| <span data-ttu-id="304c1-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="304c1-125">sequencer</span></span>    | <span data-ttu-id="304c1-126">*до конца*</span><span class="sxs-lookup"><span data-stu-id="304c1-126">to end to *position*</span></span>             | <span data-ttu-id="304c1-127">для начала</span><span class="sxs-lookup"><span data-stu-id="304c1-127">to start</span></span>                     |
| <span data-ttu-id="304c1-128">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="304c1-128">vcr</span></span>          | <span data-ttu-id="304c1-129">с *отметкой \_* *времени* в виде num Reverse</span><span class="sxs-lookup"><span data-stu-id="304c1-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="304c1-130">Окончание до начального *расположения*</span><span class="sxs-lookup"><span data-stu-id="304c1-130">to end to *position* to start</span></span> |
| <span data-ttu-id="304c1-131">видеодиск</span><span class="sxs-lookup"><span data-stu-id="304c1-131">videodisc</span></span>    | <span data-ttu-id="304c1-132">обратный в конец</span><span class="sxs-lookup"><span data-stu-id="304c1-132">reverse to end</span></span>                   | <span data-ttu-id="304c1-133">*Расположение* для начала</span><span class="sxs-lookup"><span data-stu-id="304c1-133">to *position* to start</span></span>        |
| <span data-ttu-id="304c1-134">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="304c1-134">waveaudio</span></span>    | <span data-ttu-id="304c1-135">*до конца*</span><span class="sxs-lookup"><span data-stu-id="304c1-135">to end to *position*</span></span>             | <span data-ttu-id="304c1-136">для начала</span><span class="sxs-lookup"><span data-stu-id="304c1-136">to start</span></span>                     |



 

<span data-ttu-id="304c1-137">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзсикфлагс** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="304c1-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="304c1-138">Значение</span><span class="sxs-lookup"><span data-stu-id="304c1-138">Value</span></span>            | <span data-ttu-id="304c1-139">Значение</span><span class="sxs-lookup"><span data-stu-id="304c1-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304c1-140">в *момент времени*</span><span class="sxs-lookup"><span data-stu-id="304c1-140">at *time*</span></span>        | <span data-ttu-id="304c1-141">Указывает, когда устройство должно начать выполнение этой команды, или, если устройство было куед, при запуске команды куед.</span><span class="sxs-lookup"><span data-stu-id="304c1-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="304c1-142">Дополнительные сведения см. в описании команды [Cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="304c1-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="304c1-143">пометить *знак \_ num*</span><span class="sxs-lookup"><span data-stu-id="304c1-143">mark *mark\_num*</span></span> | <span data-ttu-id="304c1-144">Ищет относительную метку, обозначенную *знаком \_ num*, которая должна быть положительным целым числом.</span><span class="sxs-lookup"><span data-stu-id="304c1-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="304c1-145">Метки — это сигналы, записанные на ленту ВИДЕОМАГНИТОФОНА с помощью команды [Mark](mark.md) и используемые для высокоскоростного поиска.</span><span class="sxs-lookup"><span data-stu-id="304c1-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="304c1-146">reverse</span><span class="sxs-lookup"><span data-stu-id="304c1-146">reverse</span></span>          | <span data-ttu-id="304c1-147">Указывает, что направление поиска в видеомагнитофоне и Кав видеодискс — назад.</span><span class="sxs-lookup"><span data-stu-id="304c1-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="304c1-148">Этот флаг является недопустимым, если указан флаг "to".</span><span class="sxs-lookup"><span data-stu-id="304c1-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="304c1-149">Для видеомагнитофонов этот флаг должен использоваться с флагом "Mark".</span><span class="sxs-lookup"><span data-stu-id="304c1-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="304c1-150">в конец</span><span class="sxs-lookup"><span data-stu-id="304c1-150">to end</span></span>           | <span data-ttu-id="304c1-151">Выполняет поиск в конце содержимого.</span><span class="sxs-lookup"><span data-stu-id="304c1-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="304c1-152">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="304c1-152">to *position*</span></span>    | <span data-ttu-id="304c1-153">Указывает положение для отмены поиска.</span><span class="sxs-lookup"><span data-stu-id="304c1-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="304c1-154">Для устройств **КДАУДИО** MCI возвращает ошибку вне диапазона, если указанная длина превышает длину диска.</span><span class="sxs-lookup"><span data-stu-id="304c1-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="304c1-155">для начала</span><span class="sxs-lookup"><span data-stu-id="304c1-155">to start</span></span>         | <span data-ttu-id="304c1-156">Выполняет поиск в начале содержимого.</span><span class="sxs-lookup"><span data-stu-id="304c1-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="304c1-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="304c1-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="304c1-158">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="304c1-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="304c1-159">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="304c1-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="304c1-160">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="304c1-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="304c1-161">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="304c1-161">Return Value</span></span>

<span data-ttu-id="304c1-162">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="304c1-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="304c1-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="304c1-163">Remarks</span></span>

<span data-ttu-id="304c1-164">Перед выполнением команд, использующих значения позиций, необходимо задать требуемый формат времени с помощью команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="304c1-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="304c1-165">Устройства Digital-Video поддерживают два режима поиска, которые можно изменить с помощью команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="304c1-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="304c1-166">Режим поиска в точном режиме приводит к перемещению команды Seek к указанному кадру.</span><span class="sxs-lookup"><span data-stu-id="304c1-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="304c1-167">Режим поиска в режиме «в точности» приводит к тому, что команда Seek переходит к ближайшему ключевому кадру до указанного кадра.</span><span class="sxs-lookup"><span data-stu-id="304c1-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="304c1-168">Если при выполнении команды Seek воспроизводится устройство CD Audio, воспроизведение останавливается.</span><span class="sxs-lookup"><span data-stu-id="304c1-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="304c1-169">Когда команда Seek выдается с устройства видеодиск, устройство выполняет поиск с использованием быстрых или быстрых обратных видео и звука.</span><span class="sxs-lookup"><span data-stu-id="304c1-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="304c1-170">Когда команда Seek выполняется с устройством аудио-аудио, поведение зависит от размера выборки.</span><span class="sxs-lookup"><span data-stu-id="304c1-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="304c1-171">Если размер выборки составляет 16 бит или больше, поиск переходит к началу ближайшего примера, когда указанная положение не совпадает с началом образца.</span><span class="sxs-lookup"><span data-stu-id="304c1-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="304c1-172">Примеры</span><span class="sxs-lookup"><span data-stu-id="304c1-172">Examples</span></span>

<span data-ttu-id="304c1-173">Следующая команда выполняет поиск в начале файла мультимедиа, связанного с устройством "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="304c1-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="304c1-174">Требования</span><span class="sxs-lookup"><span data-stu-id="304c1-174">Requirements</span></span>



| <span data-ttu-id="304c1-175">Требование</span><span class="sxs-lookup"><span data-stu-id="304c1-175">Requirement</span></span> | <span data-ttu-id="304c1-176">Значение</span><span class="sxs-lookup"><span data-stu-id="304c1-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="304c1-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="304c1-177">Minimum supported client</span></span><br/> | <span data-ttu-id="304c1-178">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="304c1-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="304c1-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="304c1-179">Minimum supported server</span></span><br/> | <span data-ttu-id="304c1-180">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="304c1-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="304c1-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="304c1-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304c1-182">MCI</span><span class="sxs-lookup"><span data-stu-id="304c1-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="304c1-183">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="304c1-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="304c1-184">cue</span><span class="sxs-lookup"><span data-stu-id="304c1-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="304c1-185">как</span><span class="sxs-lookup"><span data-stu-id="304c1-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="304c1-186">set</span><span class="sxs-lookup"><span data-stu-id="304c1-186">set</span></span>](set.md)
</dt> </dl>

 

