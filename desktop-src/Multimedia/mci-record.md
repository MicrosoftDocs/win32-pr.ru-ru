---
title: Команда MCI_RECORD (Ммсистем. h)
description: Команда MCI \_ Record начинает запись из текущей позиции или из одного указанного расположения в другое указанное расположение.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136119"
---
# <a name="mci_record-command"></a><span data-ttu-id="5d2f3-104">\_Команда MCI Record</span><span class="sxs-lookup"><span data-stu-id="5d2f3-104">MCI\_RECORD command</span></span>

<span data-ttu-id="5d2f3-105">Команда [**MCI \_ Record**](mci-record-parms.md) начинает запись из текущей позиции или из одного указанного расположения в другое указанное расположение.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="5d2f3-106">Видеозаписывающие устройства и аудио-файлы распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="5d2f3-107">Несмотря на то, что Цифровые видеоустройства и средства нумерации MIDI также распознают эту команду, драйверы МЦИАВИ и МЦИСЕК не реализуют их.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="5d2f3-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="5d2f3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d2f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2f3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="5d2f3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5d2f3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="5d2f3-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5d2f3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*лпрекорд*</span><span class="sxs-lookup"><span data-stu-id="5d2f3-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-116">Указатель на структуру [**\_ \_ пармс записи MCI**](mci-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="5d2f3-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="5d2f3-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2f3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d2f3-118">Return Value</span></span>

<span data-ttu-id="5d2f3-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d2f3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d2f3-120">Remarks</span></span>

<span data-ttu-id="5d2f3-121">Эта команда поддерживается устройствами, которые возвращают **значение true** при вызове команды [MCI \_ ЖЕТДЕВКАПС](mci-getdevcaps.md) с \_ \_ флагом MCI жетдевкапс \_ .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="5d2f3-122">Для драйвера МЦИВАВЕ все данные, записанные после открытия файла, отбрасываются, если файл закрывается без сохранения.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="5d2f3-123">Следующие дополнительные флаги применяются ко всем устройствам, поддерживающим \_ запись MCI:</span><span class="sxs-lookup"><span data-stu-id="5d2f3-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="5d2f3-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="5d2f3-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-125">Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпрекорд*.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="5d2f3-126">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="5d2f3-127">Если \_ элемент MCI из не указан, то в качестве начального расположения по умолчанию используется текущая позиция.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_Вставка записи \_ MCI</span><span class="sxs-lookup"><span data-stu-id="5d2f3-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-129">Новые записанные сведения должны вставляться в существующие данные или вставляться в них.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="5d2f3-130">Некоторые устройства могут не поддерживать это.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-130">Some devices might not support this.</span></span> <span data-ttu-id="5d2f3-131">Если поддерживается, это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_перезаписать запись MCI \_</span><span class="sxs-lookup"><span data-stu-id="5d2f3-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-133">Данные должны перезаписывать существующие данные.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-133">Data should overwrite existing data.</span></span> <span data-ttu-id="5d2f3-134">МЦИВАВЕ. \_В ответ на этот флаг устройство DRV ВОЗВРАЩАЕТ мЦиерр НЕподдерживаемую \_ функцию.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="5d2f3-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-136">Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпрекорд*.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="5d2f3-137">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="5d2f3-138">Если \_ элемент MCI не указан, в качестве конечного расположения по умолчанию используется конец содержимого.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="5d2f3-139">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="5d2f3-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5d2f3-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_ \_ \_ поток звука записи ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="5d2f3-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-141">Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лпрекорд*.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="5d2f3-142">Если этот флаг не задан, звуковые данные записываются в первый физический поток.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_ \_ хранение записи ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="5d2f3-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-144">Когда запись останавливается, экран будет содержать Последнее изображение и не будет возобновлено видео до тех пор, пока не выполнится команда [ \_ монитора MCI](mci-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_ \_ \_ поток видео записи MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="5d2f3-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-146">Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лпрекорд*.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="5d2f3-147">Если этот флаг не задан, видеоданные записываются в первый физический поток.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ ДГВ \_ Rect</span><span class="sxs-lookup"><span data-stu-id="5d2f3-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-149">Прямоугольник указывается в элементе **RC** структуры, идентифицируемой *лпрекорд*.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="5d2f3-150">Прямоугольник задает область внешнего входа, используемую в качестве источника для сжатых и сохраняемых пикселей.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="5d2f3-151">Этот прямоугольник по умолчанию имеет значение прямоугольника, заданное (или установленное по умолчанию), с помощью \_ дгва MCI, \_ поместив \_ флаг видео для команды [ \_ MCI](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="5d2f3-152">Если он задан иначе, чем прямоугольник видео, то отображаемое значение не будет записано</span><span class="sxs-lookup"><span data-stu-id="5d2f3-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="5d2f3-153">Для устройств с цифровыми видео *лпрекорд* указывает на структуру [**\_ \_ \_ пармс записи ДГВ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="5d2f3-154">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="5d2f3-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5d2f3-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_запись ВИДЕОМАГНИТОФОНА \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="5d2f3-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-156">Элемент **дват** структуры, идентифицируемой *лпрекорд* , содержит время, когда начинается вся команда, или, если устройство является куед, при достижении устройством значения, указанного в команде подсказки.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f3-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_ \_ Инициализация записи видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="5d2f3-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="5d2f3-158">Выполните поиск устройства в начале носителя, начните запись пустого видео и аудио и запишите временной код, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="5d2f3-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="5d2f3-159">Для устройств ВИДЕОМАГНИТОФОНА *лпрекорд* указывает на структуру [**\_ \_ \_ пармс записи видеомагнитофона MCI**](mci-vcr-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f3-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2f3-160">Требования</span><span class="sxs-lookup"><span data-stu-id="5d2f3-160">Requirements</span></span>



| <span data-ttu-id="5d2f3-161">Требование</span><span class="sxs-lookup"><span data-stu-id="5d2f3-161">Requirement</span></span> | <span data-ttu-id="5d2f3-162">Значение</span><span class="sxs-lookup"><span data-stu-id="5d2f3-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2f3-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d2f3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2f3-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d2f3-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d2f3-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d2f3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2f3-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d2f3-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d2f3-167">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5d2f3-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d2f3-168"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f3-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2f3-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d2f3-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2f3-170">MCI</span><span class="sxs-lookup"><span data-stu-id="5d2f3-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5d2f3-171">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="5d2f3-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

