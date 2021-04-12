---
title: Команда MCI_SAVE (Ммсистем. h)
description: Команда MCI \_ Save сохраняет текущий файл.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489585"
---
# <a name="mci_save-command"></a><span data-ttu-id="51fa5-104">Команда "Сохранить" MCI \_</span><span class="sxs-lookup"><span data-stu-id="51fa5-104">MCI\_SAVE command</span></span>

<span data-ttu-id="51fa5-105">Команда MCI \_ Save сохраняет текущий файл.</span><span class="sxs-lookup"><span data-stu-id="51fa5-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="51fa5-106">Устройства, которые изменяют файлы, не должны уничтожить исходную копию до получения сообщения о сохранении.</span><span class="sxs-lookup"><span data-stu-id="51fa5-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="51fa5-107">Эта команда распознает видео-наложение и аудио-изображения.</span><span class="sxs-lookup"><span data-stu-id="51fa5-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="51fa5-108">Несмотря на то, что Цифровые видеоустройства и средства нумерации MIDI также распознают эту команду, драйверы МЦИАВИ и МЦИСЕК не реализуют их.</span><span class="sxs-lookup"><span data-stu-id="51fa5-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="51fa5-109">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="51fa5-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="51fa5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="51fa5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51fa5-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="51fa5-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-112">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="51fa5-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="51fa5-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="51fa5-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-114">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="51fa5-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="51fa5-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="51fa5-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="51fa5-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*лпсаве*</span><span class="sxs-lookup"><span data-stu-id="51fa5-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-117">Указатель на структуру [**\_ сохранения \_ пармс в MCI**](mci-save-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="51fa5-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="51fa5-118">(Устройства с дополнительными параметрами могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="51fa5-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51fa5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51fa5-119">Return Value</span></span>

<span data-ttu-id="51fa5-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="51fa5-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fa5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51fa5-121">Remarks</span></span>

<span data-ttu-id="51fa5-122">Эта команда поддерживается устройствами, которые возвращают **значение true** при вызове команды [MCI \_ ЖЕТДЕВКАПС](mci-getdevcaps.md) с \_ \_ флагом MCI жетдевкапс \_ .</span><span class="sxs-lookup"><span data-stu-id="51fa5-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="51fa5-123">Следующий дополнительный флаг применяется ко всем устройствам, поддерживающим [MCI \_ Save](/windows):</span><span class="sxs-lookup"><span data-stu-id="51fa5-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="51fa5-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_файл для сохранения MCI \_</span><span class="sxs-lookup"><span data-stu-id="51fa5-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-125">Элемент **лпфиленаме** структуры, идентифицируемой *лпсаве* , содержит адрес буфера, содержащего имя файла назначения.</span><span class="sxs-lookup"><span data-stu-id="51fa5-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="51fa5-126">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="51fa5-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="51fa5-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ ДГВ \_ Rect</span><span class="sxs-lookup"><span data-stu-id="51fa5-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-128">Элемент **RC** структуры, идентифицируемой *лпсаве* , содержит допустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="51fa5-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="51fa5-129">Прямоугольник указывает область буфера фрейма, которая будет сохранена в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="51fa5-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="51fa5-130">Первая пара координат задает верхний левый угол прямоугольника. Вторая пара указывает ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="51fa5-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="51fa5-131">Устройства с цифровыми видео должны использовать команду [ \_ захвата MCI](mci-capture.md) для записи содержимого буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="51fa5-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="51fa5-132">(Устройства с наложением видео также должны использовать MCI \_ ЗАХВАТИТЬ.) Этот флаг предназначен для обеспечения совместимости с существующим набором команд оверлея видео MCI.</span><span class="sxs-lookup"><span data-stu-id="51fa5-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="51fa5-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_ \_ прерывание при СОХРАНЕНИИ ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="51fa5-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-134">Останавливает операцию сохранения.</span><span class="sxs-lookup"><span data-stu-id="51fa5-134">Stops a save operation in progress.</span></span> <span data-ttu-id="51fa5-135">Это должен быть единственный флаг.</span><span class="sxs-lookup"><span data-stu-id="51fa5-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="51fa5-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ ДГВ \_ Сохранить \_ кипресерве</span><span class="sxs-lookup"><span data-stu-id="51fa5-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-137">Неиспользуемое место на диске, оставшееся до первоначальной команды, [ \_ зарезервированной MCI](mci-reserve.md) , не освобождается.</span><span class="sxs-lookup"><span data-stu-id="51fa5-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="51fa5-138">Для устройств с цифровыми видео параметр *лпсаве* указывает на структуру [**MCI \_ ДГВ \_ Save \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="51fa5-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="51fa5-139">Для типа устройства **оверлея** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="51fa5-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="51fa5-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ овли \_ Rect</span><span class="sxs-lookup"><span data-stu-id="51fa5-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="51fa5-141">Элемент **RC** структуры, идентифицируемой *лпсаве* , содержит допустимый отображаемый прямоугольник, указывающий область видеобуфера для сохранения.</span><span class="sxs-lookup"><span data-stu-id="51fa5-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="51fa5-142">Для устройств с наложением параметр *лпсаве* указывает на структуру [**MCI \_ овли \_ Save \_ пармс**](/previous-versions//dd743447(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="51fa5-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fa5-143">Требования</span><span class="sxs-lookup"><span data-stu-id="51fa5-143">Requirements</span></span>



| <span data-ttu-id="51fa5-144">Требование</span><span class="sxs-lookup"><span data-stu-id="51fa5-144">Requirement</span></span> | <span data-ttu-id="51fa5-145">Значение</span><span class="sxs-lookup"><span data-stu-id="51fa5-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fa5-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51fa5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="51fa5-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51fa5-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="51fa5-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51fa5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="51fa5-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51fa5-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="51fa5-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51fa5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="51fa5-151"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51fa5-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fa5-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51fa5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fa5-153">MCI</span><span class="sxs-lookup"><span data-stu-id="51fa5-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="51fa5-154">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="51fa5-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

