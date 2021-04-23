---
title: Команда MCI_PAUSE (Ммсистем. h)
description: Команда MCI \_ Pause приостанавливает текущее действие. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- MCI_PAUSE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801018"
---
# <a name="mci_pause-command"></a><span data-ttu-id="af7d1-105">\_Команда приостановки MCI</span><span class="sxs-lookup"><span data-stu-id="af7d1-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="af7d1-106">Команда MCI \_ Pause приостанавливает текущее действие.</span><span class="sxs-lookup"><span data-stu-id="af7d1-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="af7d1-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="af7d1-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="af7d1-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="af7d1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="af7d1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af7d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af7d1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="af7d1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="af7d1-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="af7d1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="af7d1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="af7d1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="af7d1-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="af7d1-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="af7d1-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="af7d1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d1-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*лппаусе*</span><span class="sxs-lookup"><span data-stu-id="af7d1-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="af7d1-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="af7d1-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="af7d1-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="af7d1-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af7d1-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af7d1-118">Return Value</span></span>

<span data-ttu-id="af7d1-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af7d1-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af7d1-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af7d1-120">Remarks</span></span>

<span data-ttu-id="af7d1-121">Разница между командами [ \_ остановки](mci-stop.md) и \_ приостановки MCI зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d1-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="af7d1-122">Если это возможно, команда MCI \_ приостанавливает операцию устройства, но оставляет устройство готовым к немедленному возобновлению воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="af7d1-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="af7d1-123">При использовании драйверов МЦИКДА, МЦИСЕК и МЦИПИОНР \_ Команда приостановки MCI работает так же, как \_ команда MCI остановить.</span><span class="sxs-lookup"><span data-stu-id="af7d1-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="af7d1-124">Для устройств с цифровыми видео параметр *лппаусе* указывает на структуру [**MCI \_ ДГВ \_ Pause \_ пармс**](/previous-versions//dd743395(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="af7d1-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="af7d1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="af7d1-125">Requirements</span></span>



| <span data-ttu-id="af7d1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="af7d1-126">Requirement</span></span> | <span data-ttu-id="af7d1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="af7d1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af7d1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af7d1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="af7d1-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="af7d1-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="af7d1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af7d1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="af7d1-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="af7d1-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="af7d1-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="af7d1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="af7d1-133"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af7d1-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af7d1-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af7d1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7d1-135">MCI</span><span class="sxs-lookup"><span data-stu-id="af7d1-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="af7d1-136">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="af7d1-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

