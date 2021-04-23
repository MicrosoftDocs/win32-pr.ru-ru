---
title: Команда MCI_PASTE (Ммсистем. h)
description: Команда MCI \_ Paste вставляет данные из буфера обмена в файл. Устройство Digital-Video распознает эту команду.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801019"
---
# <a name="mci_paste-command"></a><span data-ttu-id="9da25-105">\_Команда MCI Paste</span><span class="sxs-lookup"><span data-stu-id="9da25-105">MCI\_PASTE command</span></span>

<span data-ttu-id="9da25-106">Команда MCI \_ Paste вставляет данные из буфера обмена в файл.</span><span class="sxs-lookup"><span data-stu-id="9da25-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="9da25-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="9da25-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="9da25-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="9da25-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="9da25-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9da25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da25-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="9da25-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9da25-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="9da25-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9da25-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9da25-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9da25-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="9da25-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="9da25-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9da25-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9da25-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*лппасте*</span><span class="sxs-lookup"><span data-stu-id="9da25-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="9da25-116">Указатель на структуру [**\_ ДГВ \_ вставки \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .</span><span class="sxs-lookup"><span data-stu-id="9da25-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da25-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9da25-117">Return Value</span></span>

<span data-ttu-id="9da25-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9da25-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9da25-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9da25-119">Remarks</span></span>

<span data-ttu-id="9da25-120">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="9da25-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="9da25-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_Вставка MCI \_ ДГВ \_ в</span><span class="sxs-lookup"><span data-stu-id="9da25-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="9da25-122">Прямоугольник включается в элемент **RC** структуры, идентифицируемой *лппасте*.</span><span class="sxs-lookup"><span data-stu-id="9da25-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="9da25-123">Первые два значения прямоугольника указывают точку внутри фрейма для размещения данных в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="9da25-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="9da25-124">Если высота и ширина прямоугольника не равны нулю, содержимое буфера обмена масштабируется по этим измерениям при их вставлении в кадр.</span><span class="sxs-lookup"><span data-stu-id="9da25-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="9da25-125">Если флаг опущен, \_ то при вставке по умолчанию в MCI выделяется весь прямоугольник фрейма.</span><span class="sxs-lookup"><span data-stu-id="9da25-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="9da25-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>\_ \_ Вставка \_ звукового \_ потока MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="9da25-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="9da25-127">Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лппасте*.</span><span class="sxs-lookup"><span data-stu-id="9da25-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="9da25-128">Если в буфере обмена существует только один звуковой поток, звуковые данные вставляются в указанный поток.</span><span class="sxs-lookup"><span data-stu-id="9da25-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="9da25-129">Если в буфере обмена существует более одного звукового потока, поток указывает начальное число для последовательностей потока.</span><span class="sxs-lookup"><span data-stu-id="9da25-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="9da25-130">Если вы используете этот флаг, а также хотите вставить видео, необходимо также использовать \_ флаг MCI ДГВ \_ Вставить \_ \_ видеопоток.</span><span class="sxs-lookup"><span data-stu-id="9da25-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="9da25-131">(Если ни один из флагов не указан, все аудио-и видеопотоки вставляются, начиная с первого потока аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="9da25-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="9da25-132">В каждом вставленном потоке остается исходный номер потока.)</span><span class="sxs-lookup"><span data-stu-id="9da25-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="9da25-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI \_ ДГВ \_ Вставить \_ вставку</span><span class="sxs-lookup"><span data-stu-id="9da25-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="9da25-134">Данные из буфера обмена должны быть вставлены в существующую рабочую область в положении, указанном MCI \_ для отметки.</span><span class="sxs-lookup"><span data-stu-id="9da25-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="9da25-135">Все существующие данные после точки вставки перемещаются в рабочую область, чтобы освободить место.</span><span class="sxs-lookup"><span data-stu-id="9da25-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="9da25-136">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9da25-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="9da25-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>Команда MCI \_ ДГВ \_ Вставить \_ Перезапись</span><span class="sxs-lookup"><span data-stu-id="9da25-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="9da25-138">Данные в буфере обмена должны заменять данные, уже имеющиеся в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9da25-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="9da25-139">Данные рабочей области, замененные, следуют точке вставки.</span><span class="sxs-lookup"><span data-stu-id="9da25-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="9da25-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_ \_ \_ поток вставки видео \_ MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="9da25-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="9da25-141">Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лппасте*.</span><span class="sxs-lookup"><span data-stu-id="9da25-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="9da25-142">Если в буфере обмена существует только один видеопоток, данные видео вставляются в указанный поток.</span><span class="sxs-lookup"><span data-stu-id="9da25-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="9da25-143">Если в буфере обмена существует более одного видеопотока, поток указывает начальное число для последовательностей потока.</span><span class="sxs-lookup"><span data-stu-id="9da25-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="9da25-144">Если вы используете этот флаг, а также хотите вставить звук, необходимо также использовать \_ флаг MCI ДГВ \_ вставку \_ аудиопотока \_ .</span><span class="sxs-lookup"><span data-stu-id="9da25-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="9da25-145">(Если ни один из флагов не указан, все аудио-и видеопотоки вставляются, начиная с первого потока аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="9da25-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="9da25-146">В каждом вставленном потоке остается исходный номер потока.)</span><span class="sxs-lookup"><span data-stu-id="9da25-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="9da25-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="9da25-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="9da25-148">Значение расположения включается в элемент **двто** структуры, идентифицируемой *лппасте*.</span><span class="sxs-lookup"><span data-stu-id="9da25-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="9da25-149">Значение позиции задает расположение, в которое следует начинать вставлять данные в рабочую область.</span><span class="sxs-lookup"><span data-stu-id="9da25-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="9da25-150">Если этот флаг опущен, то по умолчанию устанавливается текущая позицией.</span><span class="sxs-lookup"><span data-stu-id="9da25-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9da25-151">Требования</span><span class="sxs-lookup"><span data-stu-id="9da25-151">Requirements</span></span>



| <span data-ttu-id="9da25-152">Требование</span><span class="sxs-lookup"><span data-stu-id="9da25-152">Requirement</span></span> | <span data-ttu-id="9da25-153">Значение</span><span class="sxs-lookup"><span data-stu-id="9da25-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da25-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9da25-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9da25-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9da25-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9da25-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9da25-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9da25-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9da25-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9da25-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9da25-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="9da25-159"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9da25-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da25-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9da25-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da25-161">MCI</span><span class="sxs-lookup"><span data-stu-id="9da25-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9da25-162">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="9da25-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

