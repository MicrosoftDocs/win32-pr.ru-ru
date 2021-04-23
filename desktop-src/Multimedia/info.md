---
title: INFO, команда
description: Команда info Извлекает описание оборудования с устройства. Все устройства MCI распознают эту команду.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- INFO, команда мультимедиа Windows
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416016"
---
# <a name="info-command"></a><span data-ttu-id="02d19-105">INFO, команда</span><span class="sxs-lookup"><span data-stu-id="02d19-105">info command</span></span>

<span data-ttu-id="02d19-106">Команда info Извлекает описание оборудования с устройства.</span><span class="sxs-lookup"><span data-stu-id="02d19-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="02d19-107">Все устройства MCI распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="02d19-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="02d19-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="02d19-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="02d19-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="02d19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d19-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="02d19-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="02d19-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="02d19-111">Identifier of an MCI device.</span></span> <span data-ttu-id="02d19-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="02d19-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="02d19-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*лпсзинфотипе*</span><span class="sxs-lookup"><span data-stu-id="02d19-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="02d19-114">Флаг, определяющий тип требуемой информации.</span><span class="sxs-lookup"><span data-stu-id="02d19-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="02d19-115">В следующей таблице перечислены типы устройств, которые распознают команду **info** и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="02d19-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="02d19-116">Значение</span><span class="sxs-lookup"><span data-stu-id="02d19-116">Value</span></span>        | <span data-ttu-id="02d19-117">Значение</span><span class="sxs-lookup"><span data-stu-id="02d19-117">Meaning</span></span>                                                             | <span data-ttu-id="02d19-118">Значение</span><span class="sxs-lookup"><span data-stu-id="02d19-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="02d19-119">кдаудио</span><span class="sxs-lookup"><span data-stu-id="02d19-119">cdaudio</span></span>      | <span data-ttu-id="02d19-120">info идентитинфо UPC</span><span class="sxs-lookup"><span data-stu-id="02d19-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="02d19-121">product</span><span class="sxs-lookup"><span data-stu-id="02d19-121">product</span></span>                                             |
| <span data-ttu-id="02d19-122">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="02d19-122">digitalvideo</span></span> | <span data-ttu-id="02d19-123">качество звука алгорисмаудио куалитифилепродуктстилл алгорисмстилл</span><span class="sxs-lookup"><span data-stu-id="02d19-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="02d19-124">усажеверсионвидео алгорисмвидео куалитивиндов Text</span><span class="sxs-lookup"><span data-stu-id="02d19-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="02d19-125">overlay</span><span class="sxs-lookup"><span data-stu-id="02d19-125">overlay</span></span>      | <span data-ttu-id="02d19-126">филепродукт</span><span class="sxs-lookup"><span data-stu-id="02d19-126">fileproduct</span></span>                                                         | <span data-ttu-id="02d19-127">текст окна</span><span class="sxs-lookup"><span data-stu-id="02d19-127">window text</span></span>                                         |
| <span data-ttu-id="02d19-128">sequencer</span><span class="sxs-lookup"><span data-stu-id="02d19-128">sequencer</span></span>    | <span data-ttu-id="02d19-129">копиригхтфиле</span><span class="sxs-lookup"><span data-stu-id="02d19-129">copyrightfile</span></span>                                                       | <span data-ttu-id="02d19-130">намепродукт</span><span class="sxs-lookup"><span data-stu-id="02d19-130">nameproduct</span></span>                                         |
| <span data-ttu-id="02d19-131">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="02d19-131">vcr</span></span>          | <span data-ttu-id="02d19-132">product</span><span class="sxs-lookup"><span data-stu-id="02d19-132">product</span></span>                                                             | <span data-ttu-id="02d19-133">version</span><span class="sxs-lookup"><span data-stu-id="02d19-133">version</span></span>                                             |
| <span data-ttu-id="02d19-134">видеодиск</span><span class="sxs-lookup"><span data-stu-id="02d19-134">videodisk</span></span>    | <span data-ttu-id="02d19-135">product</span><span class="sxs-lookup"><span data-stu-id="02d19-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="02d19-136">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="02d19-136">waveaudio</span></span>    | <span data-ttu-id="02d19-137">филеинпут</span><span class="sxs-lookup"><span data-stu-id="02d19-137">fileinput</span></span>                                                           | <span data-ttu-id="02d19-138">аутпутпродукт</span><span class="sxs-lookup"><span data-stu-id="02d19-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="02d19-139">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзинфотипе** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="02d19-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="02d19-140">Значение</span><span class="sxs-lookup"><span data-stu-id="02d19-140">Value</span></span>           | <span data-ttu-id="02d19-141">Значение</span><span class="sxs-lookup"><span data-stu-id="02d19-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d19-142">алгоритм аудио</span><span class="sxs-lookup"><span data-stu-id="02d19-142">audio algorithm</span></span> | <span data-ttu-id="02d19-143">Возвращает имя текущего алгоритма сжатия звука.</span><span class="sxs-lookup"><span data-stu-id="02d19-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="02d19-144">качество звука</span><span class="sxs-lookup"><span data-stu-id="02d19-144">audio quality</span></span>   | <span data-ttu-id="02d19-145">Возвращает имя текущего дескриптора качества звука.</span><span class="sxs-lookup"><span data-stu-id="02d19-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="02d19-146">Это может вернуть "неизвестно", если приложение установило параметры для определенных значений, которые не соответствуют определенным показателям.</span><span class="sxs-lookup"><span data-stu-id="02d19-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="02d19-147">авторские права</span><span class="sxs-lookup"><span data-stu-id="02d19-147">copyright</span></span>       | <span data-ttu-id="02d19-148">Извлекает уведомление об авторских правах на файл MIDI из мета события об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="02d19-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="02d19-149">файл</span><span class="sxs-lookup"><span data-stu-id="02d19-149">file</span></span>            | <span data-ttu-id="02d19-150">Извлекает имя файла, используемого составным устройством.</span><span class="sxs-lookup"><span data-stu-id="02d19-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="02d19-151">Если устройство открывается без файла и команда [Load](load.md) не использовалась, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="02d19-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="02d19-152">удостоверение сведений</span><span class="sxs-lookup"><span data-stu-id="02d19-152">info identity</span></span>   | <span data-ttu-id="02d19-153">Создает уникальный идентификатор для аудио компакт-диска, который в данный момент загружен в запрашиваемый проигрыватель.</span><span class="sxs-lookup"><span data-stu-id="02d19-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="02d19-154">info UPC</span><span class="sxs-lookup"><span data-stu-id="02d19-154">info upc</span></span>        | <span data-ttu-id="02d19-155">Создает универсальный код продукта (UPC), закодированный на аудио компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="02d19-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="02d19-156">UPC — это строка цифр.</span><span class="sxs-lookup"><span data-stu-id="02d19-156">The UPC is a string of digits.</span></span> <span data-ttu-id="02d19-157">Она может быть недоступна для всех компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="02d19-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="02d19-158">input</span><span class="sxs-lookup"><span data-stu-id="02d19-158">input</span></span>           | <span data-ttu-id="02d19-159">Извлекает описание текущего входного устройства.</span><span class="sxs-lookup"><span data-stu-id="02d19-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="02d19-160">Возвращает значение None, если устройство ввода не задано.</span><span class="sxs-lookup"><span data-stu-id="02d19-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="02d19-161">name</span><span class="sxs-lookup"><span data-stu-id="02d19-161">name</span></span>            | <span data-ttu-id="02d19-162">Извлекает имя последовательности из мета-события Sequence/Track Name.</span><span class="sxs-lookup"><span data-stu-id="02d19-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="02d19-163">output</span><span class="sxs-lookup"><span data-stu-id="02d19-163">output</span></span>          | <span data-ttu-id="02d19-164">Возвращает описание текущего устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="02d19-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="02d19-165">Возвращает значение "нет", если выходное устройство не задано.</span><span class="sxs-lookup"><span data-stu-id="02d19-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="02d19-166">product</span><span class="sxs-lookup"><span data-stu-id="02d19-166">product</span></span>         | <span data-ttu-id="02d19-167">Извлекает описание устройства.</span><span class="sxs-lookup"><span data-stu-id="02d19-167">Retrieves a description of the device.</span></span> <span data-ttu-id="02d19-168">Эти сведения часто включают название продукта и модель.</span><span class="sxs-lookup"><span data-stu-id="02d19-168">This information often includes the product name and model.</span></span> <span data-ttu-id="02d19-169">Длина строки не должна превышать 31 символ.</span><span class="sxs-lookup"><span data-stu-id="02d19-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="02d19-170">алгоритм по-прежнему</span><span class="sxs-lookup"><span data-stu-id="02d19-170">still algorithm</span></span> | <span data-ttu-id="02d19-171">Возвращает имя текущего алгоритма сжатия изображений.</span><span class="sxs-lookup"><span data-stu-id="02d19-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="02d19-172">по-прежнему качество</span><span class="sxs-lookup"><span data-stu-id="02d19-172">still quality</span></span>   | <span data-ttu-id="02d19-173">Возвращает имя текущего дескриптора качества изображения.</span><span class="sxs-lookup"><span data-stu-id="02d19-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="02d19-174">Это может вернуть "неизвестно", если приложение установило параметры для определенных значений, которые не соответствуют определенным показателям.</span><span class="sxs-lookup"><span data-stu-id="02d19-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="02d19-175">usage</span><span class="sxs-lookup"><span data-stu-id="02d19-175">usage</span></span>           | <span data-ttu-id="02d19-176">Возвращает строку, описывающую ограничения использования, которые могут быть накладываются владельцем визуальных или звуковых данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="02d19-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="02d19-177">version</span><span class="sxs-lookup"><span data-stu-id="02d19-177">version</span></span>         | <span data-ttu-id="02d19-178">Возвращает уровень выпуска драйвера и оборудования устройства.</span><span class="sxs-lookup"><span data-stu-id="02d19-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="02d19-179">алгоритм видео</span><span class="sxs-lookup"><span data-stu-id="02d19-179">video algorithm</span></span> | <span data-ttu-id="02d19-180">Возвращает имя текущего алгоритма сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="02d19-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="02d19-181">качество видео</span><span class="sxs-lookup"><span data-stu-id="02d19-181">video quality</span></span>   | <span data-ttu-id="02d19-182">Возвращает имя текущего дескриптора качества видео.</span><span class="sxs-lookup"><span data-stu-id="02d19-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="02d19-183">Это может вернуть "неизвестно", если приложение установило параметры для определенных значений, которые не соответствуют определенным показателям.</span><span class="sxs-lookup"><span data-stu-id="02d19-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="02d19-184">текст окна</span><span class="sxs-lookup"><span data-stu-id="02d19-184">window text</span></span>     | <span data-ttu-id="02d19-185">Извлекает заголовок окна, используемого устройством.</span><span class="sxs-lookup"><span data-stu-id="02d19-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="02d19-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="02d19-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="02d19-187">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="02d19-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="02d19-188">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="02d19-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="02d19-189">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="02d19-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d19-190">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02d19-190">Return Value</span></span>

<span data-ttu-id="02d19-191">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="02d19-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="02d19-192">Примеры</span><span class="sxs-lookup"><span data-stu-id="02d19-192">Examples</span></span>

<span data-ttu-id="02d19-193">Следующая команда извлекает описание оборудования, связанного с устройством "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="02d19-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="02d19-194">Требования</span><span class="sxs-lookup"><span data-stu-id="02d19-194">Requirements</span></span>



| <span data-ttu-id="02d19-195">Требование</span><span class="sxs-lookup"><span data-stu-id="02d19-195">Requirement</span></span> | <span data-ttu-id="02d19-196">Значение</span><span class="sxs-lookup"><span data-stu-id="02d19-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="02d19-197">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02d19-197">Minimum supported client</span></span><br/> | <span data-ttu-id="02d19-198">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02d19-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="02d19-199">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02d19-199">Minimum supported server</span></span><br/> | <span data-ttu-id="02d19-200">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02d19-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="02d19-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02d19-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d19-202">MCI</span><span class="sxs-lookup"><span data-stu-id="02d19-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="02d19-203">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="02d19-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="02d19-204">загрузка</span><span class="sxs-lookup"><span data-stu-id="02d19-204">load</span></span>](load.md)
</dt> </dl>

 

