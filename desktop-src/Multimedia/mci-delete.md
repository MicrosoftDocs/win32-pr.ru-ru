---
title: Команда MCI_DELETE (Ммсистем. h)
description: Команда MCI \_ Delete удаляет данные из файла. Эта команда распознает цифровые видеоролики и звуковые устройства аудио-видео.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988964"
---
# <a name="mci_delete-command"></a><span data-ttu-id="81808-105">\_Команда удаления MCI</span><span class="sxs-lookup"><span data-stu-id="81808-105">MCI\_DELETE command</span></span>

<span data-ttu-id="81808-106">Команда MCI \_ Delete удаляет данные из файла.</span><span class="sxs-lookup"><span data-stu-id="81808-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="81808-107">Эта команда распознает цифровые видеоролики и звуковые устройства аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="81808-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="81808-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="81808-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="81808-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="81808-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81808-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="81808-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="81808-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="81808-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="81808-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="81808-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="81808-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="81808-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="81808-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="81808-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="81808-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*лпделете*</span><span class="sxs-lookup"><span data-stu-id="81808-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="81808-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="81808-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="81808-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="81808-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81808-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81808-118">Return Value</span></span>

<span data-ttu-id="81808-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="81808-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="81808-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81808-120">Remarks</span></span>

<span data-ttu-id="81808-121">Следующие флаги применяются к типу устройства **дигиталвидео** :</span><span class="sxs-lookup"><span data-stu-id="81808-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81808-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>\_Удаление MCI \_ ДГВ \_ в</span><span class="sxs-lookup"><span data-stu-id="81808-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="81808-123">Прямоугольник включается в элемент **RC** структуры, идентифицируемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-124">Прямоугольник указывает часть каждого удаляемого кадра.</span><span class="sxs-lookup"><span data-stu-id="81808-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="81808-125">При использовании этого флага фрейм сохраняется в рабочей области, а область, заданная прямоугольником, становится черным.</span><span class="sxs-lookup"><span data-stu-id="81808-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="81808-126">Если флаг опущен, то MCI \_ удаляет по умолчанию весь фрейм и удаляет кадр из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="81808-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="81808-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>\_ \_ Удаление \_ звукового \_ потока MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="81808-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="81808-128">Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-129">Если вы используете этот флаг, а также хотите удалить видео, необходимо также использовать \_ флаг MCI ДГВ \_ удалить \_ \_ видеопоток.</span><span class="sxs-lookup"><span data-stu-id="81808-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="81808-130">(Если ни один из флагов не указан, данные из всех потоков аудио и видео удаляются.)</span><span class="sxs-lookup"><span data-stu-id="81808-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="81808-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_ \_ Удаление \_ \_ видеопотока MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="81808-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="81808-132">Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-133">Если вы используете этот флаг, а также хотите удалить звук, необходимо также использовать \_ флаг MCI ДГВ \_ удалить \_ аудио \_ поток.</span><span class="sxs-lookup"><span data-stu-id="81808-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="81808-134">(Если ни один из флагов не указан, данные из всех потоков аудио и видео удаляются.)</span><span class="sxs-lookup"><span data-stu-id="81808-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="81808-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="81808-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="81808-136">Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-137">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="81808-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="81808-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="81808-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="81808-139">Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-140">Единицы, назначенные значениям позиций, задаются \_ \_ \_ флагом формата MCI Set Time \_ .</span><span class="sxs-lookup"><span data-stu-id="81808-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="81808-141">Для устройств с цифровыми видео параметр *лпделете* указывает на структуру [**MCI \_ ДГВ \_ DELETE \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .</span><span class="sxs-lookup"><span data-stu-id="81808-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="81808-142">Следующие флаги применяются к типу устройства **вавеаудио** :</span><span class="sxs-lookup"><span data-stu-id="81808-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="81808-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="81808-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="81808-144">Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-145">Единицы, назначенные значениям позиций, задаются \_ \_ \_ флагом формата MCI Set Time [. \_ ](mci-set.md)</span><span class="sxs-lookup"><span data-stu-id="81808-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="81808-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="81808-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="81808-147">Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпделете*.</span><span class="sxs-lookup"><span data-stu-id="81808-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="81808-148">Единицы, назначенные значениям позиций, задаются \_ \_ \_ флагом формата MCI Set Time \_ .</span><span class="sxs-lookup"><span data-stu-id="81808-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="81808-149">Для устройств с аудио-волнами параметр *лпделете* указывает на структуру [**MCI \_ волна \_ DELETE \_ пармс**](mci-wave-delete-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="81808-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="81808-150">Требования</span><span class="sxs-lookup"><span data-stu-id="81808-150">Requirements</span></span>



| <span data-ttu-id="81808-151">Требование</span><span class="sxs-lookup"><span data-stu-id="81808-151">Requirement</span></span> | <span data-ttu-id="81808-152">Значение</span><span class="sxs-lookup"><span data-stu-id="81808-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81808-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81808-153">Minimum supported client</span></span><br/> | <span data-ttu-id="81808-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81808-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="81808-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81808-155">Minimum supported server</span></span><br/> | <span data-ttu-id="81808-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="81808-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81808-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="81808-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="81808-158"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81808-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81808-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81808-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81808-160">MCI</span><span class="sxs-lookup"><span data-stu-id="81808-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="81808-161">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="81808-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

