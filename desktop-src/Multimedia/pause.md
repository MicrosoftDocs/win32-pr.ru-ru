---
title: Команда приостановки
description: Команда Pause приостанавливает воспроизведение или запись.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- Приостановка команды мультимедиа Windows
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892746"
---
# <a name="pause-command"></a><span data-ttu-id="b2a09-104">Команда приостановки</span><span class="sxs-lookup"><span data-stu-id="b2a09-104">pause command</span></span>

<span data-ttu-id="b2a09-105">Команда Pause приостанавливает воспроизведение или запись.</span><span class="sxs-lookup"><span data-stu-id="b2a09-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="b2a09-106">Большинство драйверов сохранены в текущей позиции и в конечном итоге возобновляют воспроизведение или запись в этой позиции.</span><span class="sxs-lookup"><span data-stu-id="b2a09-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="b2a09-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="b2a09-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="b2a09-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b2a09-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="b2a09-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2a09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a09-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="b2a09-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b2a09-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="b2a09-111">Identifier of an MCI device.</span></span> <span data-ttu-id="b2a09-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="b2a09-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="b2a09-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="b2a09-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b2a09-114">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="b2a09-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="b2a09-115">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="b2a09-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="b2a09-116">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b2a09-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a09-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2a09-117">Return Value</span></span>

<span data-ttu-id="b2a09-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b2a09-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a09-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2a09-119">Remarks</span></span>

<span data-ttu-id="b2a09-120">При использовании драйверов МЦИКДА, МЦИСЕК и МЦИПИОНР команда Pause работает так же, как команда [остановки](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="b2a09-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="b2a09-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="b2a09-121">Examples</span></span>

<span data-ttu-id="b2a09-122">Следующая команда приостанавливает работу устройства "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="b2a09-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="b2a09-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b2a09-123">Requirements</span></span>



| <span data-ttu-id="b2a09-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b2a09-124">Requirement</span></span> | <span data-ttu-id="b2a09-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b2a09-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b2a09-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2a09-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a09-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2a09-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b2a09-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2a09-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a09-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2a09-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b2a09-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2a09-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a09-131">MCI</span><span class="sxs-lookup"><span data-stu-id="b2a09-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b2a09-132">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="b2a09-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="b2a09-133">stop</span><span class="sxs-lookup"><span data-stu-id="b2a09-133">stop</span></span>](stop.md)
</dt> </dl>

 

