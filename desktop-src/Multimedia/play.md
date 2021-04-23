---
title: Команда "Воспроизвести"
description: Команда Play запускает воспроизведение устройства. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- Воспроизведение команды мультимедиа Windows
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672606"
---
# <a name="play-command"></a><span data-ttu-id="07aff-105">Команда "Воспроизвести"</span><span class="sxs-lookup"><span data-stu-id="07aff-105">play command</span></span>

<span data-ttu-id="07aff-106">Команда Play запускает воспроизведение устройства.</span><span class="sxs-lookup"><span data-stu-id="07aff-106">The play command starts playing a device.</span></span> <span data-ttu-id="07aff-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="07aff-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="07aff-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="07aff-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="07aff-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07aff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07aff-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="07aff-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="07aff-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="07aff-111">Identifier of an MCI device.</span></span> <span data-ttu-id="07aff-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="07aff-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="07aff-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*лпсзплайфлагс*</span><span class="sxs-lookup"><span data-stu-id="07aff-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="07aff-114">Флаг для воспроизведения устройства.</span><span class="sxs-lookup"><span data-stu-id="07aff-114">Flag for playing a device.</span></span> <span data-ttu-id="07aff-115">В следующей таблице перечислены типы устройств, которые распознают команду **Play** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="07aff-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="07aff-116">Значение</span><span class="sxs-lookup"><span data-stu-id="07aff-116">Value</span></span>        | <span data-ttu-id="07aff-117">Значение</span><span class="sxs-lookup"><span data-stu-id="07aff-117">Meaning</span></span>                          | <span data-ttu-id="07aff-118">Значение</span><span class="sxs-lookup"><span data-stu-id="07aff-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="07aff-119">кдаудио</span><span class="sxs-lookup"><span data-stu-id="07aff-119">cdaudio</span></span>      | <span data-ttu-id="07aff-120">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="07aff-120">from *position*</span></span>                  | <span data-ttu-id="07aff-121">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="07aff-121">to *position*</span></span>                     |
| <span data-ttu-id="07aff-122">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="07aff-122">digitalvideo</span></span> | <span data-ttu-id="07aff-123">из полноэкранного *расположения* повтор</span><span class="sxs-lookup"><span data-stu-id="07aff-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="07aff-124">обратить в окно *расположения*</span><span class="sxs-lookup"><span data-stu-id="07aff-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="07aff-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="07aff-125">sequencer</span></span>    | <span data-ttu-id="07aff-126">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="07aff-126">from *position*</span></span>                  | <span data-ttu-id="07aff-127">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="07aff-127">to *position*</span></span>                     |
| <span data-ttu-id="07aff-128">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="07aff-128">vcr</span></span>          | <span data-ttu-id="07aff-129">в *момент времени* от обратной *позиции*</span><span class="sxs-lookup"><span data-stu-id="07aff-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="07aff-130">сканировать до *расположения*</span><span class="sxs-lookup"><span data-stu-id="07aff-130">scan to *position*</span></span>                |
| <span data-ttu-id="07aff-131">видеодиск</span><span class="sxs-lookup"><span data-stu-id="07aff-131">videodisc</span></span>    | <span data-ttu-id="07aff-132">быстрое обратное сканирование на *месте*</span><span class="sxs-lookup"><span data-stu-id="07aff-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="07aff-133">Медленная скорость —  *целое число*</span><span class="sxs-lookup"><span data-stu-id="07aff-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="07aff-134">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="07aff-134">waveaudio</span></span>    | <span data-ttu-id="07aff-135">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="07aff-135">from *position*</span></span>                  | <span data-ttu-id="07aff-136">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="07aff-136">to *position*</span></span>                     |



 

<span data-ttu-id="07aff-137">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзплайфлагс** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="07aff-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="07aff-138">Значение</span><span class="sxs-lookup"><span data-stu-id="07aff-138">Value</span></span>           | <span data-ttu-id="07aff-139">Значение</span><span class="sxs-lookup"><span data-stu-id="07aff-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07aff-140">в *момент времени*</span><span class="sxs-lookup"><span data-stu-id="07aff-140">at *time*</span></span>       | <span data-ttu-id="07aff-141">Указывает, когда устройство должно начать выполнение этой команды, или, если устройство было куед, при запуске команды куед.</span><span class="sxs-lookup"><span data-stu-id="07aff-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="07aff-142">Дополнительные сведения см. в описании команды [Cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="07aff-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="07aff-143">быстрая</span><span class="sxs-lookup"><span data-stu-id="07aff-143">fast</span></span>            | <span data-ttu-id="07aff-144">Указывает, что устройство должно воспроизводиться быстрее, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="07aff-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="07aff-145">Чтобы определить точную скорость в проигрывателе видеодиск, используйте флаг "Speed" команды [Status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="07aff-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="07aff-146">Чтобы точнее указать скорость, используйте флаг "Speed" этой команды.</span><span class="sxs-lookup"><span data-stu-id="07aff-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="07aff-147">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="07aff-147">from *position*</span></span> | <span data-ttu-id="07aff-148">Задает начальную точку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="07aff-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="07aff-149">Если не указан флаг "from", воспроизведение начинается с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="07aff-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="07aff-150">Для устройств **кдаудио** , если значение параметра "от" больше конечного расположения диска или если значение "от" больше, чем значение "до", драйвер возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="07aff-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="07aff-151">Для устройств **видеодиск** позиции по умолчанию находятся в кадрах для дисков Кав и в часах, минутах и секундах для дисков CLV.</span><span class="sxs-lookup"><span data-stu-id="07aff-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="07aff-152">полноэкранный</span><span class="sxs-lookup"><span data-stu-id="07aff-152">fullscreen</span></span>      | <span data-ttu-id="07aff-153">Указывает, что следует использовать полноэкранный режим отображения.</span><span class="sxs-lookup"><span data-stu-id="07aff-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="07aff-154">Используйте этот флаг только при воспроизведении сжатых файлов.</span><span class="sxs-lookup"><span data-stu-id="07aff-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="07aff-155">(Несжатые файлы не воспроизводятся в полноэкранном режиме.)</span><span class="sxs-lookup"><span data-stu-id="07aff-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="07aff-156">придется</span><span class="sxs-lookup"><span data-stu-id="07aff-156">repeat</span></span>          | <span data-ttu-id="07aff-157">Указывает, что воспроизведение должно перезапускаться после достижения конца содержимого.</span><span class="sxs-lookup"><span data-stu-id="07aff-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="07aff-158">reverse</span><span class="sxs-lookup"><span data-stu-id="07aff-158">reverse</span></span>         | <span data-ttu-id="07aff-159">Указывает, что направление воспроизведения — обратное.</span><span class="sxs-lookup"><span data-stu-id="07aff-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="07aff-160">Невозможно указать конечное расположение с флагом "Reverse".</span><span class="sxs-lookup"><span data-stu-id="07aff-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="07aff-161">Для видеодискс параметр "Scan" применяется только к формату Кав.</span><span class="sxs-lookup"><span data-stu-id="07aff-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="07aff-162">наличия</span><span class="sxs-lookup"><span data-stu-id="07aff-162">scan</span></span>            | <span data-ttu-id="07aff-163">Воспроизведение выполняется как можно быстрее без отключения видео (хотя звук может быть отключен).</span><span class="sxs-lookup"><span data-stu-id="07aff-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="07aff-164">Для видеодискс параметр "Scan" применяется только к формату Кав.</span><span class="sxs-lookup"><span data-stu-id="07aff-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="07aff-165">медленный</span><span class="sxs-lookup"><span data-stu-id="07aff-165">slow</span></span>            | <span data-ttu-id="07aff-166">Медленное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="07aff-166">Plays slowly.</span></span> <span data-ttu-id="07aff-167">Чтобы определить точную скорость в проигрывателе видеодиск, используйте флаг "Speed" команды [Status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="07aff-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="07aff-168">Чтобы точнее указать скорость, используйте флаг "Speed" этой команды.</span><span class="sxs-lookup"><span data-stu-id="07aff-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="07aff-169">Для видеодискс применяется параметр "замедляют" только для формата Кав.</span><span class="sxs-lookup"><span data-stu-id="07aff-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="07aff-170">скорость — *целое число*</span><span class="sxs-lookup"><span data-stu-id="07aff-170">speed *integer*</span></span> | <span data-ttu-id="07aff-171">Воспроизводит видеодиск с заданной скоростью в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="07aff-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="07aff-172">Этот флаг применяется только к Кав дискам.</span><span class="sxs-lookup"><span data-stu-id="07aff-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="07aff-173">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="07aff-173">to *position*</span></span>   | <span data-ttu-id="07aff-174">Задает конечную точку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="07aff-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="07aff-175">Если флаг "to" не указан, воспроизведение останавливается в конце содержимого.</span><span class="sxs-lookup"><span data-stu-id="07aff-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="07aff-176">Для устройств **кдаудио** , если расположение "to" больше конечного расположения диска, драйвер возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="07aff-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="07aff-177">Для устройств **видеодиск** позиции по умолчанию находятся в кадрах для дисков Кав и в часах, минутах и секундах для дисков CLV.</span><span class="sxs-lookup"><span data-stu-id="07aff-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="07aff-178">window</span><span class="sxs-lookup"><span data-stu-id="07aff-178">window</span></span>          | <span data-ttu-id="07aff-179">Указывает, что при воспроизведении следует использовать окно, связанное с экземпляром устройства.</span><span class="sxs-lookup"><span data-stu-id="07aff-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="07aff-180">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07aff-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="07aff-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="07aff-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="07aff-182">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="07aff-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="07aff-183">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="07aff-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="07aff-184">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="07aff-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07aff-185">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07aff-185">Return Value</span></span>

<span data-ttu-id="07aff-186">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="07aff-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07aff-187">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07aff-187">Remarks</span></span>

<span data-ttu-id="07aff-188">Перед выполнением команд, использующих значения позиций, необходимо задать требуемый формат времени с помощью команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="07aff-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="07aff-189">Эта команда начинает играть с текущей скоростью, как задано командой "Speed".</span><span class="sxs-lookup"><span data-stu-id="07aff-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="07aff-190">Направление является обратным, если указан флаг "Reverse", или если флаг "to" задан как значение меньше, чем флаг "от".</span><span class="sxs-lookup"><span data-stu-id="07aff-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="07aff-191">Если не указан флаг "from", воспроизведение начинается с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="07aff-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="07aff-192">Флаги "to" и "Reverse" не могут использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="07aff-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="07aff-193">Примеры</span><span class="sxs-lookup"><span data-stu-id="07aff-193">Examples</span></span>

<span data-ttu-id="07aff-194">Следующая команда воспроизводит устройство "мисаунд" из расположения 1000 в положении 2000, отправляя сообщение уведомления после завершения воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="07aff-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="07aff-195">Требования</span><span class="sxs-lookup"><span data-stu-id="07aff-195">Requirements</span></span>



| <span data-ttu-id="07aff-196">Требование</span><span class="sxs-lookup"><span data-stu-id="07aff-196">Requirement</span></span> | <span data-ttu-id="07aff-197">Значение</span><span class="sxs-lookup"><span data-stu-id="07aff-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="07aff-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07aff-198">Minimum supported client</span></span><br/> | <span data-ttu-id="07aff-199">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07aff-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="07aff-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07aff-200">Minimum supported server</span></span><br/> | <span data-ttu-id="07aff-201">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07aff-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="07aff-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07aff-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07aff-203">MCI</span><span class="sxs-lookup"><span data-stu-id="07aff-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="07aff-204">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="07aff-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="07aff-205">cue</span><span class="sxs-lookup"><span data-stu-id="07aff-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="07aff-206">set</span><span class="sxs-lookup"><span data-stu-id="07aff-206">set</span></span>](set.md)
</dt> </dl>

 

