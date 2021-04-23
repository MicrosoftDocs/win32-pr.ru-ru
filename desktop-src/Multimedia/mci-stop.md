---
title: Команда MCI_STOP (Ммсистем. h)
description: Команда MCI \_ Stop останавливает все последовательности воспроизведения и записи, выгружает все буферы воспроизведения и прекращает отображение видеоизображений. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415644"
---
# <a name="mci_stop-command"></a><span data-ttu-id="b1d10-105">\_Команда "прерывать" MCI</span><span class="sxs-lookup"><span data-stu-id="b1d10-105">MCI\_STOP command</span></span>

<span data-ttu-id="b1d10-106">Команда MCI \_ Stop останавливает все последовательности воспроизведения и записи, выгружает все буферы воспроизведения и прекращает отображение видеоизображений.</span><span class="sxs-lookup"><span data-stu-id="b1d10-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="b1d10-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="b1d10-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="b1d10-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="b1d10-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="b1d10-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1d10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1d10-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="b1d10-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b1d10-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="b1d10-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b1d10-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b1d10-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b1d10-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b1d10-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="b1d10-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b1d10-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1d10-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*лпстоп*</span><span class="sxs-lookup"><span data-stu-id="b1d10-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="b1d10-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b1d10-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b1d10-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="b1d10-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1d10-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1d10-118">Return Value</span></span>

<span data-ttu-id="b1d10-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b1d10-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1d10-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1d10-120">Remarks</span></span>

<span data-ttu-id="b1d10-121">Разница между \_ командами остановки и [ \_ приостановки](mci-pause.md) MCI зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="b1d10-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="b1d10-122">Если это возможно, команда MCI \_ приостанавливает операцию устройства, но оставляет устройство готовым к немедленному возобновлению воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b1d10-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="b1d10-123">Для устройства с компакт-диска MCI \_ останавливает сбрасывает текущее расположение дорожки до нуля. в отличие от этого, при [ \_ приостановке MCI](mci-pause.md) сохраняется текущая позиция дорожки, что предполагает, что устройство будет продолжать играть.</span><span class="sxs-lookup"><span data-stu-id="b1d10-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d10-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b1d10-124">Requirements</span></span>



| <span data-ttu-id="b1d10-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b1d10-125">Requirement</span></span> | <span data-ttu-id="b1d10-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b1d10-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d10-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1d10-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d10-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1d10-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b1d10-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1d10-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d10-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1d10-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1d10-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b1d10-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1d10-132"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1d10-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d10-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1d10-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d10-134">MCI</span><span class="sxs-lookup"><span data-stu-id="b1d10-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b1d10-135">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="b1d10-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

