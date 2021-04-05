---
title: заморозить команду
description: Команда Freeze закрепляет видеоввод или видео на ВИДЕОМАГНИТОФОН или отключает получение видео в буфере кадров. Эта команда распознает цифровые видеоролики, наложение видео и устройства ВИДЕОМАГНИТОФОНА.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- заморозить команды мультимедиа Windows
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071096"
---
# <a name="freeze-command"></a><span data-ttu-id="98d5f-105">заморозить команду</span><span class="sxs-lookup"><span data-stu-id="98d5f-105">freeze command</span></span>

<span data-ttu-id="98d5f-106">Команда Freeze закрепляет видеоввод или видео на ВИДЕОМАГНИТОФОН или отключает получение видео в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="98d5f-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="98d5f-107">Эта команда распознает цифровые видеоролики, наложение видео и устройства ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="98d5f-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="98d5f-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="98d5f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="98d5f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="98d5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d5f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="98d5f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="98d5f-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="98d5f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="98d5f-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="98d5f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="98d5f-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*лпсзфризефлагс*</span><span class="sxs-lookup"><span data-stu-id="98d5f-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="98d5f-114">Флаг, указывающий, что следует заморозить.</span><span class="sxs-lookup"><span data-stu-id="98d5f-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="98d5f-115">В следующей таблице перечислены типы устройств, которые распознают команду **Freeze** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="98d5f-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98d5f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-116">Value</span></span></th>
<th><span data-ttu-id="98d5f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-117">Meaning</span></span></th>
<th><span data-ttu-id="98d5f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98d5f-119">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="98d5f-119">digitalvideo</span></span></td>
<td><span data-ttu-id="98d5f-120">в <em>прямоугольнике</em></span><span class="sxs-lookup"><span data-stu-id="98d5f-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="98d5f-121">созданные</span><span class="sxs-lookup"><span data-stu-id="98d5f-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98d5f-122">overlay</span><span class="sxs-lookup"><span data-stu-id="98d5f-122">overlay</span></span></td>
<td><span data-ttu-id="98d5f-123">в <em>прямоугольнике</em></span><span class="sxs-lookup"><span data-stu-id="98d5f-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="98d5f-124">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="98d5f-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="98d5f-125">поле</span><span class="sxs-lookup"><span data-stu-id="98d5f-125">field</span></span></li>
<li><span data-ttu-id="98d5f-126">frame</span><span class="sxs-lookup"><span data-stu-id="98d5f-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="98d5f-127">input</span><span class="sxs-lookup"><span data-stu-id="98d5f-127">input</span></span></li>
<li><span data-ttu-id="98d5f-128">output</span><span class="sxs-lookup"><span data-stu-id="98d5f-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="98d5f-129">В следующей таблице перечислены флаги, которые могут быть указаны в параметре *лпсзфризефлагс* , и их значения.</span><span class="sxs-lookup"><span data-stu-id="98d5f-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="98d5f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-130">Value</span></span>          | <span data-ttu-id="98d5f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d5f-132">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="98d5f-132">at *rectangle*</span></span> | <span data-ttu-id="98d5f-133">Указывает область, которая будет заморожена.</span><span class="sxs-lookup"><span data-stu-id="98d5f-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="98d5f-134">Для устройств с наложением видео в этом регионе будет отключено получение видео.</span><span class="sxs-lookup"><span data-stu-id="98d5f-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="98d5f-135">Для устройств с цифровыми видео Пиксели в прямоугольнике будут включены в качестве бита маски блокировки (если не указан флаг "снаружи").</span><span class="sxs-lookup"><span data-stu-id="98d5f-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="98d5f-136">Прямоугольник задается относительно источника видеобуфера и задается как *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="98d5f-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="98d5f-137">Координаты *x1 Y1* определяют левый верхний угол прямоугольника, а координаты *x2 Y2* определяют ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="98d5f-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="98d5f-138">поле</span><span class="sxs-lookup"><span data-stu-id="98d5f-138">field</span></span>          | <span data-ttu-id="98d5f-139">Закрепляет первое поле.</span><span class="sxs-lookup"><span data-stu-id="98d5f-139">Freezes the first field.</span></span> <span data-ttu-id="98d5f-140">По умолчанию принимает значение поля (если ни фрейм, ни поле не указано).</span><span class="sxs-lookup"><span data-stu-id="98d5f-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="98d5f-141">frame</span><span class="sxs-lookup"><span data-stu-id="98d5f-141">frame</span></span>          | <span data-ttu-id="98d5f-142">Закрепляет весь фрейм, отображая оба поля.</span><span class="sxs-lookup"><span data-stu-id="98d5f-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="98d5f-143">input</span><span class="sxs-lookup"><span data-stu-id="98d5f-143">input</span></span>          | <span data-ttu-id="98d5f-144">Закрепляет текущий кадр входного изображения, будь он приостановлен или запущен.</span><span class="sxs-lookup"><span data-stu-id="98d5f-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="98d5f-145">output</span><span class="sxs-lookup"><span data-stu-id="98d5f-145">output</span></span>         | <span data-ttu-id="98d5f-146">Закрепляет текущий кадр выходных данных с ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="98d5f-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="98d5f-147">Если видеомагнитофон проигрывается при выдаче закрепления, текущий кадр закрепляется, а ВИДЕОМАГНИТОФОН приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="98d5f-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="98d5f-148">Если ВИДЕОМАГНИТОФОН приостановлен при выдаче этой команды, текущий кадр заморожен.</span><span class="sxs-lookup"><span data-stu-id="98d5f-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="98d5f-149">Замороженный образ остается на выходном устройстве до тех пор, пока не будет вызвана команда [unfreeze](unfreeze.md) .</span><span class="sxs-lookup"><span data-stu-id="98d5f-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="98d5f-150">Если не указано ни «вход», ни «Output», то предполагается «Output».</span><span class="sxs-lookup"><span data-stu-id="98d5f-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="98d5f-151">созданные</span><span class="sxs-lookup"><span data-stu-id="98d5f-151">outside</span></span>        | <span data-ttu-id="98d5f-152">Указывает, что область за пределами области, указанной с помощью флага "at", заморожена.</span><span class="sxs-lookup"><span data-stu-id="98d5f-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="98d5f-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="98d5f-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="98d5f-154">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="98d5f-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="98d5f-155">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="98d5f-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="98d5f-156">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="98d5f-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d5f-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-157">Return Value</span></span>

<span data-ttu-id="98d5f-158">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="98d5f-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d5f-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98d5f-159">Remarks</span></span>

<span data-ttu-id="98d5f-160">При использовании с устройствами ВИДЕОМАГНИТОФОНА эта команда предназначена для карт, занятых кадрами.</span><span class="sxs-lookup"><span data-stu-id="98d5f-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="98d5f-161">Чтобы указать нестандартные регионы приобретения с флагом "at", используйте ряд команд "заморозить" и " [разморозить](unfreeze.md) ".</span><span class="sxs-lookup"><span data-stu-id="98d5f-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="98d5f-162">Некоторые устройства наложения видео ограничивают сложность региона приобретения.</span><span class="sxs-lookup"><span data-stu-id="98d5f-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="98d5f-163">Эта команда поддерживается только в том случае, если вызов команды [возможности](capability.md) с флагом "может заморозить" возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="98d5f-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="98d5f-164">Примеры</span><span class="sxs-lookup"><span data-stu-id="98d5f-164">Examples</span></span>

<span data-ttu-id="98d5f-165">Следующая команда отключает получение видео в квадрате 100 пикселей в левом верхнем углу видеобуфера.</span><span class="sxs-lookup"><span data-stu-id="98d5f-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="98d5f-166">Требования</span><span class="sxs-lookup"><span data-stu-id="98d5f-166">Requirements</span></span>



| <span data-ttu-id="98d5f-167">Требование</span><span class="sxs-lookup"><span data-stu-id="98d5f-167">Requirement</span></span> | <span data-ttu-id="98d5f-168">Значение</span><span class="sxs-lookup"><span data-stu-id="98d5f-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="98d5f-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98d5f-169">Minimum supported client</span></span><br/> | <span data-ttu-id="98d5f-170">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98d5f-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98d5f-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98d5f-171">Minimum supported server</span></span><br/> | <span data-ttu-id="98d5f-172">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="98d5f-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="98d5f-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98d5f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d5f-174">MCI</span><span class="sxs-lookup"><span data-stu-id="98d5f-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="98d5f-175">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="98d5f-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

<span data-ttu-id="98d5f-176">[capability](capability.md);</span><span class="sxs-lookup"><span data-stu-id="98d5f-176">[capability](capability.md)</span></span>
</dt> <dt>

[<span data-ttu-id="98d5f-177">освободить</span><span class="sxs-lookup"><span data-stu-id="98d5f-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 

