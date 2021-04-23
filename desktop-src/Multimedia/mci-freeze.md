---
title: Команда MCI_FREEZE (Ммсистем. h)
description: Команда « \_ замораживание» MCI закрепляет движение на экране. Эта команда распознает цифровые видеоролики, наложение видео и устройства ВИДЕОМАГНИТОФОНА.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071318"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="1506c-105">\_Команда заморозить MCI</span><span class="sxs-lookup"><span data-stu-id="1506c-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="1506c-106">Команда « \_ замораживание» MCI закрепляет движение на экране.</span><span class="sxs-lookup"><span data-stu-id="1506c-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="1506c-107">Эта команда распознает цифровые видеоролики, наложение видео и устройства ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="1506c-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="1506c-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="1506c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="1506c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1506c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1506c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="1506c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1506c-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="1506c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1506c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1506c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1506c-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1506c-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="1506c-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1506c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1506c-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*лпфризе*</span><span class="sxs-lookup"><span data-stu-id="1506c-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="1506c-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1506c-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="1506c-117">(Устройства с дополнительными параметрами могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="1506c-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1506c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1506c-118">Return Value</span></span>

<span data-ttu-id="1506c-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1506c-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1506c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1506c-120">Remarks</span></span>

<span data-ttu-id="1506c-121">Тип устройства **дигиталвидео** использует следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="1506c-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1506c-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_ДГВ MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1506c-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="1506c-123">Элемент **RC** структуры, идентифицируемой *лпфризе* , содержит допустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="1506c-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="1506c-124">Прямоугольник задает область внутри буфера кадров, для которой включен бит маски блокировки для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="1506c-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="1506c-125">Указанные пиксели не будут обновлены до тех пор, пока не будет снят бит маски блокировки.</span><span class="sxs-lookup"><span data-stu-id="1506c-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="1506c-126">Если этот флаг не указан, прямоугольником по умолчанию выделяется весь буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="1506c-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="1506c-127">Этот флаг поддерживается только в том случае, если команда [MCI \_ Жетдевкапс](mci-getdevcaps.md) возвращает **значение true** для параметра ДГВ MCI, \_ \_ жетдевкапс \_ может \_ блокировать флаг.</span><span class="sxs-lookup"><span data-stu-id="1506c-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="1506c-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ ДГВ \_ заморозить \_ снаружи</span><span class="sxs-lookup"><span data-stu-id="1506c-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="1506c-129">Область за пределами региона, указанного для \_ \_ флага MCI ДГВ Freeze On \_ , зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="1506c-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="1506c-130">Для устройств с цифровыми видео параметр *лпфризе* указывает на структуру [**MCI \_ ДГВ \_ Freeze \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="1506c-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="1506c-131">Тип устройства **видеомагнитофона** использует следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="1506c-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1506c-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_ \_ поле замораживания видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="1506c-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="1506c-133">Заморозить только один член текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="1506c-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="1506c-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_ \_ кадр замораживания видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="1506c-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="1506c-135">Закрепить оба поля текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="1506c-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="1506c-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_ \_ Ввод данных о замораживании видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="1506c-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="1506c-137">Закрепление текущего кадра на экране (используется для записи).</span><span class="sxs-lookup"><span data-stu-id="1506c-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="1506c-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_закрепление \_ \_ выходных данных MCI видеомагнитофона</span><span class="sxs-lookup"><span data-stu-id="1506c-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="1506c-139">Закрепление текущего кадра из ВИДЕОМАГНИТОФОНА (используется с записью кадров).</span><span class="sxs-lookup"><span data-stu-id="1506c-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="1506c-140">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпфризе* указывает на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1506c-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="1506c-141">Для типа устройства **оверлея** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="1506c-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1506c-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ овли \_ Rect</span><span class="sxs-lookup"><span data-stu-id="1506c-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="1506c-143">Элемент **RC** структуры, идентифицируемой *лпфризе* , содержит допустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="1506c-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="1506c-144">Если этот флаг не указан, драйвер устройства будет закреплять весь кадр.</span><span class="sxs-lookup"><span data-stu-id="1506c-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="1506c-145">Для устройств с наложением параметр *лпфризе* указывает на структуру [**MCI \_ овли \_ Rect \_ пармс**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1506c-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1506c-146">Требования</span><span class="sxs-lookup"><span data-stu-id="1506c-146">Requirements</span></span>



| <span data-ttu-id="1506c-147">Требование</span><span class="sxs-lookup"><span data-stu-id="1506c-147">Requirement</span></span> | <span data-ttu-id="1506c-148">Значение</span><span class="sxs-lookup"><span data-stu-id="1506c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1506c-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1506c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1506c-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1506c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1506c-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1506c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1506c-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1506c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1506c-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1506c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1506c-154"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1506c-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1506c-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1506c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1506c-156">MCI</span><span class="sxs-lookup"><span data-stu-id="1506c-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1506c-157">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="1506c-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

