---
title: Команда MCI_CUE (Ммсистем. h)
description: Команда MCI \_ Cue подписывает устройство, чтобы воспроизведение или запись начинались с минимальной задержкой. Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672768"
---
# <a name="mci_cue-command"></a><span data-ttu-id="903e5-105">\_Команда MCI Cue</span><span class="sxs-lookup"><span data-stu-id="903e5-105">MCI\_CUE command</span></span>

<span data-ttu-id="903e5-106">Команда MCI \_ Cue подписывает устройство, чтобы воспроизведение или запись начинались с минимальной задержкой.</span><span class="sxs-lookup"><span data-stu-id="903e5-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="903e5-107">Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="903e5-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="903e5-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="903e5-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="903e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="903e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="903e5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="903e5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="903e5-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="903e5-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="903e5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="903e5-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="903e5-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="903e5-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="903e5-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="903e5-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*лпкуе*</span><span class="sxs-lookup"><span data-stu-id="903e5-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="903e5-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="903e5-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="903e5-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="903e5-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="903e5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="903e5-118">Return Value</span></span>

<span data-ttu-id="903e5-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="903e5-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="903e5-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="903e5-120">Remarks</span></span>

<span data-ttu-id="903e5-121">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="903e5-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="903e5-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_ \_ Ввод подсказки MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="903e5-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="903e5-123">Экземпляр цифрового видео должен подготовиться к записи.</span><span class="sxs-lookup"><span data-stu-id="903e5-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="903e5-124">Если приложение не зарезервирует место на диске, оно резервирует место на диске, используя параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="903e5-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="903e5-125">Приложение может опустить этот флаг, если текущий источник представления уже является внешним входом.</span><span class="sxs-lookup"><span data-stu-id="903e5-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="903e5-126">(Этот флаг не влияет на выбор источника презентации.)</span><span class="sxs-lookup"><span data-stu-id="903e5-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="903e5-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>\_ДГВ с \_ подсказкой MCI \_</span><span class="sxs-lookup"><span data-stu-id="903e5-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="903e5-128">Экземпляр цифрового видео должен подготовиться к воспроизведению кадра, указанного с помощью команды, без отображения.</span><span class="sxs-lookup"><span data-stu-id="903e5-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="903e5-129">Если этот флаг указан, изображение будет отображаться в буфере кадров, даже если соответствующий кадр не является текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="903e5-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="903e5-130">Например, если буфер фрейма содержит изображение из кадра 7, устройство продолжит отображать кадр 7, если этот флаг используется для перестановки устройства в любую другую точку.</span><span class="sxs-lookup"><span data-stu-id="903e5-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="903e5-131">Следующая команда подсказки без этого флага и без \_ флага MCI отображает текущий кадр.</span><span class="sxs-lookup"><span data-stu-id="903e5-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>\_ \_ \_ выходные данные ДГВ для MCI</span><span class="sxs-lookup"><span data-stu-id="903e5-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="903e5-133">Экземпляр цифрового видео должен подготовиться к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="903e5-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="903e5-134">Если Рабочая область приостановлена, позиционирование не выполняется.</span><span class="sxs-lookup"><span data-stu-id="903e5-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="903e5-135">Если Рабочая область остановлена, она может измениться на предыдущее изображение с ключевым кадром.</span><span class="sxs-lookup"><span data-stu-id="903e5-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="903e5-136">Приложение может опустить этот флаг, если текущий источник презентации уже является рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="903e5-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="903e5-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="903e5-138">Расположение рабочей области включается в элемент **двто** структуры, определяемой *лпкуе*.</span><span class="sxs-lookup"><span data-stu-id="903e5-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="903e5-139">Единицы, назначенные значениям позиций, указываются с \_ помощью \_ \_ флага формата времени MCI для команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="903e5-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="903e5-140">Это эквивалентно поиску в положении, за исключением того, что устройство приостановлено после выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="903e5-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="903e5-141">Для устройств **дигиталвидео** параметр *лпкуе* указывает на структуру [**MCI \_ ДГВ \_ Cue \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .</span><span class="sxs-lookup"><span data-stu-id="903e5-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="903e5-142">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="903e5-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="903e5-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="903e5-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="903e5-144">Элемент **двфром** структуры, на который указывает *лпкуе* , содержит начальное расположение, указанное в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="903e5-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="903e5-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="903e5-146">Элемент **двто** структуры, на который указывает *лпкуе* , содержит конечное (Приостановка) расположение, указанное в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="903e5-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_ \_ \_ входные данные подсказки видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="903e5-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="903e5-148">Подготовка к записи.</span><span class="sxs-lookup"><span data-stu-id="903e5-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_ \_ выходные данные Cue видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="903e5-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="903e5-150">Подготовка к воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="903e5-150">Prepare for playing.</span></span> <span data-ttu-id="903e5-151">Если \_ \_ не указаны ни входная подсказка видеомагнитофона MCI \_ \_ , ни \_ выходные данные Cue видеомагнитофона MCI \_ , \_ \_ предполагается вывод подсказки для видеомагнитофона MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="903e5-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>\_ \_ предпробная подсказка видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="903e5-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="903e5-153">Подсказка устройства к текущему положению или положению **двфром** за вычетом длительности.</span><span class="sxs-lookup"><span data-stu-id="903e5-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="903e5-154">Это позволит устройству подготовиться к работе перед переходом в режим записи или воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="903e5-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>\_ \_ обратный контрольный видеомагнитофон MCI \_</span><span class="sxs-lookup"><span data-stu-id="903e5-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="903e5-156">Направление следующей команды воспроизведения или записи — обратный.</span><span class="sxs-lookup"><span data-stu-id="903e5-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="903e5-157">При cueing для воспроизведения с помощью команды MCI \_ Cue с \_ \_ \_ флагом выходных данных "Cue видеомагнитофона" MCI можно отменить \_ подсказку MCI, выполнив команду [MCI \_ Play](mci-play.md) с помощью MCI \_ , \_ а также MCI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="903e5-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="903e5-158">При cueing для записи с помощью \_ команды MCI, помеченной \_ \_ \_ флагом входа MCI, можно отменить \_ подсказку MCI, выполнив команду MCI [ \_ Record](mci-record.md) с помощью MCI с \_ , MCI \_ или \_ записи видеомагнитофона MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="903e5-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="903e5-159">Для устройств **видеомагнитофона** параметр *лпкуе* указывает на структуру [**\_ \_ \_ пармс видеомагнитофона Cue**](mci-vcr-cue-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="903e5-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="903e5-160">С типом устройства **вавеаудио** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="903e5-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="903e5-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_звуковые \_ входные данные MCI</span><span class="sxs-lookup"><span data-stu-id="903e5-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="903e5-162">Устройство ввода аудио-сигнала должно быть куед.</span><span class="sxs-lookup"><span data-stu-id="903e5-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="903e5-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_звуковые \_ выходные данные MCI</span><span class="sxs-lookup"><span data-stu-id="903e5-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="903e5-164">Устройство вывода аудио-файлов должно быть куед.</span><span class="sxs-lookup"><span data-stu-id="903e5-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="903e5-165">Этот флаг используется по умолчанию, если не указан флаг.</span><span class="sxs-lookup"><span data-stu-id="903e5-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="903e5-166">Требования</span><span class="sxs-lookup"><span data-stu-id="903e5-166">Requirements</span></span>



| <span data-ttu-id="903e5-167">Требование</span><span class="sxs-lookup"><span data-stu-id="903e5-167">Requirement</span></span> | <span data-ttu-id="903e5-168">Значение</span><span class="sxs-lookup"><span data-stu-id="903e5-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903e5-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="903e5-169">Minimum supported client</span></span><br/> | <span data-ttu-id="903e5-170">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="903e5-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="903e5-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="903e5-171">Minimum supported server</span></span><br/> | <span data-ttu-id="903e5-172">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="903e5-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="903e5-173">Заголовок</span><span class="sxs-lookup"><span data-stu-id="903e5-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="903e5-174"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="903e5-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="903e5-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="903e5-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="903e5-176">MCI</span><span class="sxs-lookup"><span data-stu-id="903e5-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="903e5-177">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="903e5-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

