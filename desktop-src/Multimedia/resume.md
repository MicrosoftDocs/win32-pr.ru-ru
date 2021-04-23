---
title: Команда возобновления
description: Команда Resume продолжает воспроизведение или запись на устройстве, которое было приостановлено с помощью команды Pause.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- возобновление команды мультимедиа Windows
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672476"
---
# <a name="resume-command"></a><span data-ttu-id="4da09-104">Команда возобновления</span><span class="sxs-lookup"><span data-stu-id="4da09-104">resume command</span></span>

<span data-ttu-id="4da09-105">Команда Resume продолжает воспроизведение или запись на устройстве, которое было приостановлено с помощью команды [Pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="4da09-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="4da09-106">Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="4da09-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="4da09-107">Хотя аудио компакт-диск, программа MIDI Sequencer и устройства видеодиск также распознают эту команду, драйверы устройств МЦИКДА, МЦИСЕК и МЦИПИОНР не поддерживают эти команды.</span><span class="sxs-lookup"><span data-stu-id="4da09-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="4da09-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4da09-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4da09-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4da09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da09-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="4da09-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4da09-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="4da09-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4da09-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="4da09-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4da09-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="4da09-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4da09-114">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="4da09-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4da09-115">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="4da09-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4da09-116">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4da09-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da09-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4da09-117">Return Value</span></span>

<span data-ttu-id="4da09-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4da09-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="4da09-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="4da09-119">Examples</span></span>

<span data-ttu-id="4da09-120">Следующая команда продолжит воспроизведение или запись устройства "невсаунд".</span><span class="sxs-lookup"><span data-stu-id="4da09-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="4da09-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4da09-121">Requirements</span></span>



| <span data-ttu-id="4da09-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4da09-122">Requirement</span></span> | <span data-ttu-id="4da09-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4da09-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4da09-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4da09-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4da09-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4da09-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4da09-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4da09-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4da09-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4da09-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4da09-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4da09-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da09-129">MCI</span><span class="sxs-lookup"><span data-stu-id="4da09-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4da09-130">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="4da09-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4da09-131">pause</span><span class="sxs-lookup"><span data-stu-id="4da09-131">pause</span></span>](pause.md)
</dt> </dl>

 

