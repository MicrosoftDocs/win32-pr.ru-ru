---
title: Команда "прерывать"
description: Команда Stop останавливает воспроизведение или запись. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Команда "прерывать мультимедиа Windows"
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415516"
---
# <a name="stop-command"></a><span data-ttu-id="6c029-105">Команда "прерывать"</span><span class="sxs-lookup"><span data-stu-id="6c029-105">stop command</span></span>

<span data-ttu-id="6c029-106">Команда Stop останавливает воспроизведение или запись.</span><span class="sxs-lookup"><span data-stu-id="6c029-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="6c029-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="6c029-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="6c029-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6c029-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6c029-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c029-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c029-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="6c029-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6c029-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="6c029-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6c029-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="6c029-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6c029-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*лпсзстопфлагс*</span><span class="sxs-lookup"><span data-stu-id="6c029-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6c029-114">Для устройств с цифровыми видео это может быть следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="6c029-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="6c029-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6c029-115">Value</span></span> | <span data-ttu-id="6c029-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6c029-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c029-117">Нажмите</span><span class="sxs-lookup"><span data-stu-id="6c029-117">hold</span></span>  | <span data-ttu-id="6c029-118">Предотвращает освобождение ресурсов, необходимых для перерисовки изображения на экране.</span><span class="sxs-lookup"><span data-stu-id="6c029-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="6c029-119">Буфер фрейма остается доступным для использования при обновлении экрана, если, например, перемещается окно.</span><span class="sxs-lookup"><span data-stu-id="6c029-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6c029-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="6c029-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6c029-121">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="6c029-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="6c029-122">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="6c029-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="6c029-123">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6c029-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c029-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c029-124">Return Value</span></span>

<span data-ttu-id="6c029-125">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c029-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c029-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c029-126">Remarks</span></span>

<span data-ttu-id="6c029-127">Для устройств с компакт-дисков команда Stop останавливает воспроизведение и сбрасывает текущее расположение дорожки в ноль.</span><span class="sxs-lookup"><span data-stu-id="6c029-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="6c029-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="6c029-128">Examples</span></span>

<span data-ttu-id="6c029-129">Следующая команда останавливает воспроизведение или запись на устройстве "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="6c029-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="6c029-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6c029-130">Requirements</span></span>



| <span data-ttu-id="6c029-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6c029-131">Requirement</span></span> | <span data-ttu-id="6c029-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6c029-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6c029-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c029-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6c029-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c029-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6c029-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c029-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6c029-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c029-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6c029-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c029-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c029-138">MCI</span><span class="sxs-lookup"><span data-stu-id="6c029-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6c029-139">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="6c029-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

