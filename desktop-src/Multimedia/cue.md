---
title: Команда подсказки
description: Команда подсказки готовится к воспроизведению или записи. Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Команда подсказки Windows мультимедиа
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892762"
---
# <a name="cue-command"></a><span data-ttu-id="7d8c3-105">Команда подсказки</span><span class="sxs-lookup"><span data-stu-id="7d8c3-105">cue command</span></span>

<span data-ttu-id="7d8c3-106">Команда подсказки готовится к воспроизведению или записи.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="7d8c3-107">Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="7d8c3-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7d8c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d8c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8c3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="7d8c3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7d8c3-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-111">Identifier of an MCI device.</span></span> <span data-ttu-id="7d8c3-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7d8c3-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*лпсзинаутто*</span><span class="sxs-lookup"><span data-stu-id="7d8c3-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="7d8c3-114">Флаг, подготавливающий устройство к воспроизведению или записи.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="7d8c3-115">В следующей таблице перечислены типы устройств, которые распознают команду **подсказки** и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d8c3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7d8c3-116">Value</span></span></th>
<th><span data-ttu-id="7d8c3-117">Сказк</span><span class="sxs-lookup"><span data-stu-id="7d8c3-117">Cue</span></span></th>
<th><span data-ttu-id="7d8c3-118">Сказк</span><span class="sxs-lookup"><span data-stu-id="7d8c3-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d8c3-119">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="7d8c3-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="7d8c3-120">input</span><span class="sxs-lookup"><span data-stu-id="7d8c3-120">input</span></span></li>
<li><span data-ttu-id="7d8c3-121">не показывать</span><span class="sxs-lookup"><span data-stu-id="7d8c3-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7d8c3-122">output</span><span class="sxs-lookup"><span data-stu-id="7d8c3-122">output</span></span></li>
<li><span data-ttu-id="7d8c3-123">в <em>Расположение</em></span><span class="sxs-lookup"><span data-stu-id="7d8c3-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d8c3-124">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="7d8c3-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="7d8c3-125">от <em>расположения</em></span><span class="sxs-lookup"><span data-stu-id="7d8c3-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="7d8c3-126">input</span><span class="sxs-lookup"><span data-stu-id="7d8c3-126">input</span></span></li>
<li><span data-ttu-id="7d8c3-127">output</span><span class="sxs-lookup"><span data-stu-id="7d8c3-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7d8c3-128">сделана предварительная проба</span><span class="sxs-lookup"><span data-stu-id="7d8c3-128">preroll</span></span></li>
<li><span data-ttu-id="7d8c3-129">reverse</span><span class="sxs-lookup"><span data-stu-id="7d8c3-129">reverse</span></span></li>
<li><span data-ttu-id="7d8c3-130">в <em>Расположение</em></span><span class="sxs-lookup"><span data-stu-id="7d8c3-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d8c3-131">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="7d8c3-131">waveaudio</span></span></td>
<td><span data-ttu-id="7d8c3-132">input</span><span class="sxs-lookup"><span data-stu-id="7d8c3-132">input</span></span></td>
<td><span data-ttu-id="7d8c3-133">output</span><span class="sxs-lookup"><span data-stu-id="7d8c3-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7d8c3-134">В следующей таблице перечислены флаги, которые могут быть указаны в параметре *лпсзинаутто* , и их значения.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="7d8c3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7d8c3-135">Value</span></span>           | <span data-ttu-id="7d8c3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7d8c3-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8c3-137">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="7d8c3-137">from *position*</span></span> | <span data-ttu-id="7d8c3-138">Указывает, с чего начать.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7d8c3-139">input</span><span class="sxs-lookup"><span data-stu-id="7d8c3-139">input</span></span>           | <span data-ttu-id="7d8c3-140">Подготовка к записи.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-140">Prepares for recording.</span></span> <span data-ttu-id="7d8c3-141">Для устройств с цифровыми видео этот флаг можно опустить, если текущий источник представления уже является внешним входом.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="7d8c3-142">не показывать</span><span class="sxs-lookup"><span data-stu-id="7d8c3-142">noshow</span></span>          | <span data-ttu-id="7d8c3-143">Готовится к показу кадра без отображения.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="7d8c3-144">Если этот флаг указан, изображение будет отображаться в буфере кадров, даже если соответствующий кадр не является текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="7d8c3-145">Следующая команда подсказки без этого флага и без флага "to" отображает текущий кадр.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="7d8c3-146">output</span><span class="sxs-lookup"><span data-stu-id="7d8c3-146">output</span></span>          | <span data-ttu-id="7d8c3-147">Подготовка к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-147">Prepares for playing.</span></span> <span data-ttu-id="7d8c3-148">Если не указано ни «вход», ни «Output», значение по умолчанию — «Output».</span><span class="sxs-lookup"><span data-stu-id="7d8c3-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="7d8c3-149">сделана предварительная проба</span><span class="sxs-lookup"><span data-stu-id="7d8c3-149">preroll</span></span>         | <span data-ttu-id="7d8c3-150">Перемещает предварительное расстояние от *точки во входном* виде.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="7d8c3-151">Точка в качестве текущей позиции или позиции, заданной флагом "from".</span><span class="sxs-lookup"><span data-stu-id="7d8c3-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="7d8c3-152">reverse</span><span class="sxs-lookup"><span data-stu-id="7d8c3-152">reverse</span></span>         | <span data-ttu-id="7d8c3-153">Указывает направление воспроизведения в обратном направлении (назад).</span><span class="sxs-lookup"><span data-stu-id="7d8c3-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7d8c3-154">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="7d8c3-154">to *position*</span></span>   | <span data-ttu-id="7d8c3-155">Перемещает рабочую область в указанную точку.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="7d8c3-156">Для устройств ВИДЕОМАГНИТОФОНА этот флаг указывает, где следует останавливаться.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="7d8c3-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="7d8c3-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7d8c3-158">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="7d8c3-159">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="7d8c3-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="7d8c3-160">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7d8c3-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8c3-161">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d8c3-161">Return Value</span></span>

<span data-ttu-id="7d8c3-162">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d8c3-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d8c3-163">Remarks</span></span>

<span data-ttu-id="7d8c3-164">Хотя это необязательно, выдача команды подсказки перед воспроизведением или записью на некоторых устройствах может снизить задержку, прежде чем устройство запустит действие.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="7d8c3-165">Эта команда завершается ошибкой, если выполняется воспроизведение или запись, или если устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="7d8c3-166">При cueing для воспроизведения (с использованием подсказки "Output") команда [Play](play.md) с флагом "from", "to" или "Reverse" отменяет команду подсказки.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="7d8c3-167">При cueing записи (с помощью подсказки "входные") выдача команды [записи](record.md) с флагом "from", "to" или "Initialize" отменяет команду подсказки.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="7d8c3-168">Примеры</span><span class="sxs-lookup"><span data-stu-id="7d8c3-168">Examples</span></span>

<span data-ttu-id="7d8c3-169">Следующая команда подготавливает устройство "мисаунд" для записи.</span><span class="sxs-lookup"><span data-stu-id="7d8c3-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="7d8c3-170">Требования</span><span class="sxs-lookup"><span data-stu-id="7d8c3-170">Requirements</span></span>



| <span data-ttu-id="7d8c3-171">Требование</span><span class="sxs-lookup"><span data-stu-id="7d8c3-171">Requirement</span></span> | <span data-ttu-id="7d8c3-172">Значение</span><span class="sxs-lookup"><span data-stu-id="7d8c3-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7d8c3-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d8c3-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8c3-174">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d8c3-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7d8c3-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d8c3-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8c3-176">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d8c3-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7d8c3-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d8c3-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8c3-178">MCI</span><span class="sxs-lookup"><span data-stu-id="7d8c3-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7d8c3-179">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="7d8c3-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7d8c3-180">воспроизводит</span><span class="sxs-lookup"><span data-stu-id="7d8c3-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="7d8c3-181">record</span><span class="sxs-lookup"><span data-stu-id="7d8c3-181">record</span></span>](record.md)
</dt> </dl>

 

