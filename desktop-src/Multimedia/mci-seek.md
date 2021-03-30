---
title: Команда MCI_SEEK (Ммсистем. h)
description: Команда MCI \_ Seek изменяет текущую положение в содержимом как можно быстрее.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- MCI_SEEK команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071313"
---
# <a name="mci_seek-command"></a><span data-ttu-id="60039-104">\_Команда MCI Seek</span><span class="sxs-lookup"><span data-stu-id="60039-104">MCI\_SEEK command</span></span>

<span data-ttu-id="60039-105">Команда MCI \_ Seek изменяет текущую положение в содержимом как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="60039-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="60039-106">Во время поиска выходные данные видео и звука отключаются.</span><span class="sxs-lookup"><span data-stu-id="60039-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="60039-107">После завершения поиска устройство будет остановлено.</span><span class="sxs-lookup"><span data-stu-id="60039-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="60039-108">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="60039-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="60039-109">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="60039-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="60039-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="60039-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60039-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="60039-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="60039-112">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="60039-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="60039-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="60039-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="60039-114">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="60039-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="60039-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="60039-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="60039-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*лпсик*</span><span class="sxs-lookup"><span data-stu-id="60039-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="60039-117">Указатель на структуру [**\_ \_ пармс поиска MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="60039-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="60039-118">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="60039-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60039-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60039-119">Return Value</span></span>

<span data-ttu-id="60039-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="60039-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="60039-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60039-121">Remarks</span></span>

<span data-ttu-id="60039-122">Если размер выборки данных для устройства превышает 1 байт (например, с стерео-аудио), эта команда перемещается в начало ближайшего примера, когда указанная координата не совпадает с началом образца.</span><span class="sxs-lookup"><span data-stu-id="60039-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="60039-123">Следующие дополнительные флаги применяются ко всем устройствам, поддерживающим MCI \_ Seek:</span><span class="sxs-lookup"><span data-stu-id="60039-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="60039-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_Поиск \_ в \_ конце MCI</span><span class="sxs-lookup"><span data-stu-id="60039-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="60039-125">Поиск в конце содержимого.</span><span class="sxs-lookup"><span data-stu-id="60039-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="60039-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>\_Начало поиска \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="60039-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="60039-127">Поиск в начале содержимого.</span><span class="sxs-lookup"><span data-stu-id="60039-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="60039-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="60039-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="60039-129">В элемент **двто** структуры, идентифицируемой *лпсик*, входит расположение.</span><span class="sxs-lookup"><span data-stu-id="60039-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="60039-130">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="60039-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="60039-131">Не используйте этот флаг для запуска с помощью MCI \_ Seek \_ to \_ End или MCI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="60039-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="60039-132">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="60039-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="60039-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>\_Поиск видеомагнитофонов MCI \_ \_ по адресу</span><span class="sxs-lookup"><span data-stu-id="60039-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="60039-134">Элемент **дват** структуры, идентифицируемой *лпсик* , содержит время, когда начинается вся команда.</span><span class="sxs-lookup"><span data-stu-id="60039-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="60039-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_ \_ Метка поиска видеомагнитофона \_ видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="60039-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="60039-136">Элемент **двмарк** структуры, идентифицируемой *лпсик* , содержит пронумерованную отметку для поиска.</span><span class="sxs-lookup"><span data-stu-id="60039-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="60039-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>\_обратный поиск видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="60039-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="60039-138">Направление поиска — обратный; Он используется только с \_ \_ \_ флагом Метки поиска видеомагнитофона видеомагнитофон.</span><span class="sxs-lookup"><span data-stu-id="60039-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="60039-139">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпсик* указывает на структуру [**\_ \_ \_ пармс в видеомагнитофоне MCI**](mci-vcr-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="60039-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="60039-140">С типом устройства **видеодиск** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="60039-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="60039-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>\_ \_ обратный поиск VD \_ MCI</span><span class="sxs-lookup"><span data-stu-id="60039-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="60039-142">Направление поиска — обратный.</span><span class="sxs-lookup"><span data-stu-id="60039-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60039-143">Требования</span><span class="sxs-lookup"><span data-stu-id="60039-143">Requirements</span></span>



| <span data-ttu-id="60039-144">Требование</span><span class="sxs-lookup"><span data-stu-id="60039-144">Requirement</span></span> | <span data-ttu-id="60039-145">Значение</span><span class="sxs-lookup"><span data-stu-id="60039-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60039-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60039-146">Minimum supported client</span></span><br/> | <span data-ttu-id="60039-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="60039-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60039-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60039-148">Minimum supported server</span></span><br/> | <span data-ttu-id="60039-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="60039-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60039-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="60039-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="60039-151"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60039-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60039-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60039-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60039-153">MCI</span><span class="sxs-lookup"><span data-stu-id="60039-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="60039-154">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="60039-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

