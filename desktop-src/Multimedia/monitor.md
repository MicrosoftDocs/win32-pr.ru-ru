---
title: Команда Monitor
description: Команда Monitor указывает источник представления. (В качестве источника представления по умолчанию используется рабочая область.) При переключении источника презентации все аудио и видеопотоки в источнике переключаются. Устройство Digital-Video распознает эту команду.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- команда мониторинга мультимедиа Windows
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802219"
---
# <a name="monitor-command"></a><span data-ttu-id="5cdba-106">Команда Monitor</span><span class="sxs-lookup"><span data-stu-id="5cdba-106">monitor command</span></span>

<span data-ttu-id="5cdba-107">Команда Monitor указывает источник представления.</span><span class="sxs-lookup"><span data-stu-id="5cdba-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="5cdba-108">(В качестве источника представления по умолчанию используется рабочая область.) При переключении источника презентации все аудио и видеопотоки в источнике переключаются.</span><span class="sxs-lookup"><span data-stu-id="5cdba-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="5cdba-109">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="5cdba-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="5cdba-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="5cdba-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5cdba-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cdba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cdba-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="5cdba-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5cdba-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="5cdba-113">Identifier of an MCI device.</span></span> <span data-ttu-id="5cdba-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="5cdba-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5cdba-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*лпсзмонитор*</span><span class="sxs-lookup"><span data-stu-id="5cdba-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="5cdba-116">Один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="5cdba-116">One or more of the following flags.</span></span>



| <span data-ttu-id="5cdba-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5cdba-117">Value</span></span>           | <span data-ttu-id="5cdba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5cdba-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cdba-119">файл</span><span class="sxs-lookup"><span data-stu-id="5cdba-119">file</span></span>            | <span data-ttu-id="5cdba-120">Указывает, что Рабочая область является источником презентации.</span><span class="sxs-lookup"><span data-stu-id="5cdba-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="5cdba-121">Это источник по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cdba-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5cdba-122">input</span><span class="sxs-lookup"><span data-stu-id="5cdba-122">input</span></span>           | <span data-ttu-id="5cdba-123">Указывает, что внешний вход является источником представления.</span><span class="sxs-lookup"><span data-stu-id="5cdba-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="5cdba-124">Если команда [воспроизведения](play.md) выполняется, она сначала приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="5cdba-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="5cdba-125">Если [сетвидео](setvideo.md) имеет значение ON, этот флаг отображает скрытое окно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cdba-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="5cdba-126">Устройства могут ограничивать возможности других экземпляров устройств при наблюдении за входными данными.</span><span class="sxs-lookup"><span data-stu-id="5cdba-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5cdba-127">метод *method*</span><span class="sxs-lookup"><span data-stu-id="5cdba-127">method *method*</span></span> | <span data-ttu-id="5cdba-128">При использовании с **Monitor** "input" Этот флаг выбирает метод мониторинга.</span><span class="sxs-lookup"><span data-stu-id="5cdba-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="5cdba-129">*Метод* имеет значение "Pre", "Post" или "Direct".</span><span class="sxs-lookup"><span data-stu-id="5cdba-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="5cdba-130">Прямые запросы мониторинга, которые устройство должно настроить для оптимального качества отображения во время мониторинга.</span><span class="sxs-lookup"><span data-stu-id="5cdba-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="5cdba-131">Метод прямого мониторинга может быть несовместим с записью видео движения. Перед и после мониторинга разрешается запись видео о движении.</span><span class="sxs-lookup"><span data-stu-id="5cdba-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="5cdba-132">При предварительном мониторинге отображаются внешние входные данные перед сжатием, а после сжатия — внешний вход.</span><span class="sxs-lookup"><span data-stu-id="5cdba-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="5cdba-133">Как правило, различные методы мониторинга имеют различные последствия для оборудования.</span><span class="sxs-lookup"><span data-stu-id="5cdba-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="5cdba-134">На устройстве выбирается метод мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cdba-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5cdba-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="5cdba-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5cdba-136">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="5cdba-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="5cdba-137">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5cdba-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cdba-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cdba-138">Return Value</span></span>

<span data-ttu-id="5cdba-139">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5cdba-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cdba-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cdba-140">Remarks</span></span>

<span data-ttu-id="5cdba-141">Источник презентации автоматически переключается в рабочую область после завершения [воспроизведения](play.md), [шага](step.md), [приостановки](pause.md), [подсказки](cue.md) "Output" или команды [Seek](seek.md) .</span><span class="sxs-lookup"><span data-stu-id="5cdba-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="5cdba-142">Команда [Record](record.md) не переключает источники представления автоматически, что дает приложению возможность не отображать видео во время записи.</span><span class="sxs-lookup"><span data-stu-id="5cdba-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cdba-143">Требования</span><span class="sxs-lookup"><span data-stu-id="5cdba-143">Requirements</span></span>



| <span data-ttu-id="5cdba-144">Требование</span><span class="sxs-lookup"><span data-stu-id="5cdba-144">Requirement</span></span> | <span data-ttu-id="5cdba-145">Значение</span><span class="sxs-lookup"><span data-stu-id="5cdba-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5cdba-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cdba-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5cdba-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5cdba-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5cdba-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cdba-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5cdba-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5cdba-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5cdba-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cdba-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cdba-151">MCI</span><span class="sxs-lookup"><span data-stu-id="5cdba-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5cdba-152">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="5cdba-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="5cdba-153">cue</span><span class="sxs-lookup"><span data-stu-id="5cdba-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="5cdba-154">pause</span><span class="sxs-lookup"><span data-stu-id="5cdba-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="5cdba-155">воспроизводит</span><span class="sxs-lookup"><span data-stu-id="5cdba-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="5cdba-156">record</span><span class="sxs-lookup"><span data-stu-id="5cdba-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="5cdba-157">поиска</span><span class="sxs-lookup"><span data-stu-id="5cdba-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="5cdba-158">первом</span><span class="sxs-lookup"><span data-stu-id="5cdba-158">step</span></span>](step.md)
</dt> </dl>

 

