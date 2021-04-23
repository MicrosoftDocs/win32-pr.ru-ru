---
title: Команда MCI_PLAY (Ммсистем. h)
description: Команда MCI \_ Play сообщает устройству о необходимости начать передачу выходных данных. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- MCI_PLAY команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892757"
---
# <a name="mci_play-command"></a><span data-ttu-id="1573f-105">\_Команда MCI Play</span><span class="sxs-lookup"><span data-stu-id="1573f-105">MCI\_PLAY command</span></span>

<span data-ttu-id="1573f-106">Команда MCI \_ Play сообщает устройству о необходимости начать передачу выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1573f-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="1573f-107">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, видеодиск, ВИДЕОМАГНИТОФОН и волна-аудиоустройства.</span><span class="sxs-lookup"><span data-stu-id="1573f-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="1573f-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="1573f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="1573f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1573f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1573f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="1573f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1573f-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="1573f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1573f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1573f-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1573f-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="1573f-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1573f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1573f-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*лпплай*</span><span class="sxs-lookup"><span data-stu-id="1573f-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="1573f-116">Указатель на структуру [**MCI \_ Play \_ пармс**](mci-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1573f-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="1573f-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="1573f-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1573f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1573f-118">Return Value</span></span>

<span data-ttu-id="1573f-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1573f-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1573f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1573f-120">Remarks</span></span>

<span data-ttu-id="1573f-121">Следующие дополнительные флаги применяются ко всем устройствам, поддерживающим MCI \_ Play:</span><span class="sxs-lookup"><span data-stu-id="1573f-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="1573f-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="1573f-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="1573f-123">Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпплай*.</span><span class="sxs-lookup"><span data-stu-id="1573f-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="1573f-124">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="1573f-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="1573f-125">Если \_ элемент MCI из не указан, то в качестве начального расположения по умолчанию используется текущая позиция.</span><span class="sxs-lookup"><span data-stu-id="1573f-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="1573f-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="1573f-127">Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпплай*.</span><span class="sxs-lookup"><span data-stu-id="1573f-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="1573f-128">Единицы, назначенные значениям позиций, задаются \_ \_ \_ флагом формата MCI Set Time \_ .</span><span class="sxs-lookup"><span data-stu-id="1573f-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="1573f-129">Если \_ элемент MCI не указан, в качестве конечного расположения по умолчанию используется конец носителя.</span><span class="sxs-lookup"><span data-stu-id="1573f-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="1573f-130">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="1573f-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1573f-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_Воспроизведение MCI ДГВ \_ воспроизведения \_ повторено</span><span class="sxs-lookup"><span data-stu-id="1573f-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="1573f-132">Воспроизведение должно начаться снова в начале после достижения конца содержимого.</span><span class="sxs-lookup"><span data-stu-id="1573f-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>\_ДГВ MCI \_ воспроизводить \_ обратный</span><span class="sxs-lookup"><span data-stu-id="1573f-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1573f-134">Воспроизведение должно выполняться в обратную.</span><span class="sxs-lookup"><span data-stu-id="1573f-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>\_окно MCI мЦиави \_ Play \_</span><span class="sxs-lookup"><span data-stu-id="1573f-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="1573f-136">Воспроизведение должно выполняться в окне, связанном с экземпляром устройства (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1573f-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="1573f-137">(Этот флаг относится только к МЦИАВИ. DRV.)</span><span class="sxs-lookup"><span data-stu-id="1573f-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="1573f-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>\_Воспроизведение MCI мЦиави в \_ \_ полноэкранном режим</span><span class="sxs-lookup"><span data-stu-id="1573f-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="1573f-139">Воспроизведение должно использовать полноэкранный экран.</span><span class="sxs-lookup"><span data-stu-id="1573f-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="1573f-140">Используйте этот флаг только при воспроизведении сжатых или 8-разрядных файлов.</span><span class="sxs-lookup"><span data-stu-id="1573f-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="1573f-141">Для устройств с цифровыми видео *лпплай* указывает на структуру [**MCI \_ ДГВ \_ Play \_ пармс**](/previous-versions//dd743396(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1573f-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="1573f-142">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="1573f-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1573f-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_Воспроизведение ВИДЕОМАГНИТОФОНА \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="1573f-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="1573f-144">Элемент **дват** структуры, идентифицируемой *лпплай* , содержит время, когда начинается вся команда, или, если устройство находится в куед, когда устройство достигает расположения от, заданного командой [MCI \_ Cue](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="1573f-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>\_Воспроизведение видеомагнитофона MCI — \_ \_ обратный</span><span class="sxs-lookup"><span data-stu-id="1573f-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1573f-146">Воспроизведение должно выполняться в обратную.</span><span class="sxs-lookup"><span data-stu-id="1573f-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_Просмотр воспроизведения видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1573f-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="1573f-148">Воспроизведение должно выполняться максимально быстро при сохранении вывода видео.</span><span class="sxs-lookup"><span data-stu-id="1573f-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="1573f-149">Для устройств ВИДЕОМАГНИТОФОНА *лпплай* указывает структуру [**\_ видеомагнитофона MCI \_ Play \_ пармс**](mci-vcr-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1573f-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="1573f-150">С типом устройства **видеодиск** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="1573f-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1573f-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>\_ \_ быстрое воспроизведение MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="1573f-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="1573f-152">Быстрое воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="1573f-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>\_VD MCI \_ воспроизводить \_ обратный</span><span class="sxs-lookup"><span data-stu-id="1573f-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1573f-154">Воспроизвести в обратную.</span><span class="sxs-lookup"><span data-stu-id="1573f-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI \_ VD \_ Play \_ сканирование</span><span class="sxs-lookup"><span data-stu-id="1573f-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="1573f-156">Быстро сканировать.</span><span class="sxs-lookup"><span data-stu-id="1573f-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>\_Воспроизведение MCI \_ VD \_ работает слишком долго</span><span class="sxs-lookup"><span data-stu-id="1573f-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="1573f-158">Медленное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="1573f-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="1573f-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_ \_ скорость воспроизведения MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="1573f-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="1573f-160">Скорость воспроизведения включается в элемент **двспид** в структуре, определяемой *лпплай*.</span><span class="sxs-lookup"><span data-stu-id="1573f-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1573f-161">Требования</span><span class="sxs-lookup"><span data-stu-id="1573f-161">Requirements</span></span>



| <span data-ttu-id="1573f-162">Требование</span><span class="sxs-lookup"><span data-stu-id="1573f-162">Requirement</span></span> | <span data-ttu-id="1573f-163">Значение</span><span class="sxs-lookup"><span data-stu-id="1573f-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1573f-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1573f-164">Minimum supported client</span></span><br/> | <span data-ttu-id="1573f-165">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1573f-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1573f-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1573f-166">Minimum supported server</span></span><br/> | <span data-ttu-id="1573f-167">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1573f-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1573f-168">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1573f-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="1573f-169"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1573f-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1573f-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1573f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1573f-171">MCI</span><span class="sxs-lookup"><span data-stu-id="1573f-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1573f-172">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="1573f-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

