---
title: удалить команду
description: Команда DELETE удаляет сегмент данных из файла. Эта команда распознает цифровые видеоролики и звуковые устройства аудио-видео.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- Удаление команды мультимедиа Windows
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892582"
---
# <a name="delete-command"></a><span data-ttu-id="4aebc-105">удалить команду</span><span class="sxs-lookup"><span data-stu-id="4aebc-105">delete command</span></span>

<span data-ttu-id="4aebc-106">Команда DELETE удаляет сегмент данных из файла.</span><span class="sxs-lookup"><span data-stu-id="4aebc-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="4aebc-107">Эта команда распознает цифровые видеоролики и звуковые устройства аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="4aebc-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="4aebc-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4aebc-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4aebc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4aebc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aebc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="4aebc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4aebc-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="4aebc-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4aebc-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="4aebc-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*лпсзпоситион*</span><span class="sxs-lookup"><span data-stu-id="4aebc-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="4aebc-114">Флаг, определяющий сегмент данных для удаления.</span><span class="sxs-lookup"><span data-stu-id="4aebc-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="4aebc-115">В следующей таблице перечислены типы устройств, которые распознают команду **Delete** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="4aebc-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4aebc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-116">Value</span></span></th>
<th><span data-ttu-id="4aebc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-117">Meaning</span></span></th>
<th><span data-ttu-id="4aebc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4aebc-119">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="4aebc-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="4aebc-120">в <em>прямоугольнике</em></span><span class="sxs-lookup"><span data-stu-id="4aebc-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="4aebc-121"><em>поток</em> аудиопотока</span><span class="sxs-lookup"><span data-stu-id="4aebc-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="4aebc-122">от <em>расположения</em></span><span class="sxs-lookup"><span data-stu-id="4aebc-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4aebc-123">в <em>Расположение</em></span><span class="sxs-lookup"><span data-stu-id="4aebc-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="4aebc-124"><em>поток</em> видео поток</span><span class="sxs-lookup"><span data-stu-id="4aebc-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4aebc-125">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="4aebc-125">waveaudio</span></span></td>
<td><span data-ttu-id="4aebc-126">от <em>расположения</em></span><span class="sxs-lookup"><span data-stu-id="4aebc-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="4aebc-127">в <em>Расположение</em></span><span class="sxs-lookup"><span data-stu-id="4aebc-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4aebc-128">В следующей таблице перечислены флаги, которые могут быть указаны в параметре *лпсзпоситион* , и их значения.</span><span class="sxs-lookup"><span data-stu-id="4aebc-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="4aebc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-129">Value</span></span>                 | <span data-ttu-id="4aebc-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aebc-131">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="4aebc-131">at *rectangle*</span></span>        | <span data-ttu-id="4aebc-132">Указывает часть каждого кадра, удаленную.</span><span class="sxs-lookup"><span data-stu-id="4aebc-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="4aebc-133">Если этот параметр опущен, по умолчанию используется весь кадр.</span><span class="sxs-lookup"><span data-stu-id="4aebc-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="4aebc-134">Если этот элемент указан, рамки не удаляются.</span><span class="sxs-lookup"><span data-stu-id="4aebc-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="4aebc-135">Вместо этого область внутри прямоугольника становится черным.</span><span class="sxs-lookup"><span data-stu-id="4aebc-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="4aebc-136">*поток* аудиопотока</span><span class="sxs-lookup"><span data-stu-id="4aebc-136">audio stream *stream*</span></span> | <span data-ttu-id="4aebc-137">Указывает аудиопоток в рабочей области, затронутой командой.</span><span class="sxs-lookup"><span data-stu-id="4aebc-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="4aebc-138">Если вы используете этот флаг, а также хотите удалить видео, необходимо также использовать флаг "поток видео".</span><span class="sxs-lookup"><span data-stu-id="4aebc-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="4aebc-139">(Если ни один из флагов не указан, все потоки аудио и видео будут удалены.)</span><span class="sxs-lookup"><span data-stu-id="4aebc-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="4aebc-140">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="4aebc-140">from *position*</span></span>       | <span data-ttu-id="4aebc-141">Указывает расположение, с которого начинается удаление.</span><span class="sxs-lookup"><span data-stu-id="4aebc-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="4aebc-142">Если этот флаг опущен, удаление начинается с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="4aebc-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="4aebc-143">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="4aebc-143">to *position*</span></span>         | <span data-ttu-id="4aebc-144">Указывает расположение, в котором заканчивается удаление.</span><span class="sxs-lookup"><span data-stu-id="4aebc-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="4aebc-145">Если этот флаг опущен, удаление продолжится до конца содержимого или рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4aebc-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="4aebc-146">*поток* видео поток</span><span class="sxs-lookup"><span data-stu-id="4aebc-146">video stream *stream*</span></span> | <span data-ttu-id="4aebc-147">Указывает поток видео в рабочей области, на который влияет команда.</span><span class="sxs-lookup"><span data-stu-id="4aebc-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="4aebc-148">Если вы используете этот флаг, а также хотите удалить аудио, необходимо также использовать флаг "Audio Stream".</span><span class="sxs-lookup"><span data-stu-id="4aebc-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="4aebc-149">(Если ни один из флагов не указан, все потоки аудио и видео будут удалены.)</span><span class="sxs-lookup"><span data-stu-id="4aebc-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="4aebc-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="4aebc-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4aebc-151">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="4aebc-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4aebc-152">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="4aebc-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4aebc-153">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4aebc-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aebc-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-154">Return Value</span></span>

<span data-ttu-id="4aebc-155">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4aebc-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aebc-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aebc-156">Remarks</span></span>

<span data-ttu-id="4aebc-157">Перед выполнением команд, использующих значения позиций, необходимо задать требуемый формат времени с помощью команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="4aebc-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="4aebc-158">Примеры</span><span class="sxs-lookup"><span data-stu-id="4aebc-158">Examples</span></span>

<span data-ttu-id="4aebc-159">Следующая команда удаляет данные звуковой волны с 1 миллисекунда до 900 миллисекунд (при условии, что для формата времени задано значение миллисекунд).</span><span class="sxs-lookup"><span data-stu-id="4aebc-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="4aebc-160">Требования</span><span class="sxs-lookup"><span data-stu-id="4aebc-160">Requirements</span></span>



| <span data-ttu-id="4aebc-161">Требование</span><span class="sxs-lookup"><span data-stu-id="4aebc-161">Requirement</span></span> | <span data-ttu-id="4aebc-162">Значение</span><span class="sxs-lookup"><span data-stu-id="4aebc-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4aebc-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4aebc-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4aebc-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4aebc-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4aebc-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4aebc-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4aebc-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4aebc-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4aebc-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aebc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aebc-168">MCI</span><span class="sxs-lookup"><span data-stu-id="4aebc-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4aebc-169">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="4aebc-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4aebc-170">set</span><span class="sxs-lookup"><span data-stu-id="4aebc-170">set</span></span>](set.md)
</dt> </dl>

 

