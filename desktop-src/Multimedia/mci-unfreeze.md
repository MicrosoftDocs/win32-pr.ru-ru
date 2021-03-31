---
title: Команда MCI_UNFREEZE (Ммсистем. h)
description: '\_Команда РАЗморозка MCI восстанавливает движение в область видеобуфера, замороженную \_ командой MCI Freeze. Эта команда распознает цифровые видеоролики, видеомагнитофоны и устройства наложения видео.'
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137387"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="88234-105">Команда "отменить \_ замораживание" MCI</span><span class="sxs-lookup"><span data-stu-id="88234-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="88234-106">\_Команда РАЗморозка MCI восстанавливает движение в область видеобуфера, замороженную командой [MCI \_ Freeze](mci-freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="88234-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="88234-107">Эта команда распознает цифровые видеоролики, видеомагнитофоны и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="88234-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="88234-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="88234-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="88234-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="88234-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88234-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="88234-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="88234-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="88234-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="88234-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="88234-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="88234-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="88234-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="88234-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="88234-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="88234-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*лпунфризе*</span><span class="sxs-lookup"><span data-stu-id="88234-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="88234-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="88234-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="88234-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="88234-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88234-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88234-118">Return Value</span></span>

<span data-ttu-id="88234-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="88234-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88234-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88234-120">Remarks</span></span>

<span data-ttu-id="88234-121">С типом устройства **дигиталвидео** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="88234-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="88234-122">MCI \_ ДГВ \_ Rect</span><span class="sxs-lookup"><span data-stu-id="88234-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="88234-123">Элемент **RC** структуры, идентифицируемой *лпунфризе* , содержит допустимый отображаемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="88234-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="88234-124">Прямоугольник задает область внутри буфера кадров, в пикселях которой должен быть снят бит маски блокировки.</span><span class="sxs-lookup"><span data-stu-id="88234-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="88234-125">Прямоугольные области указываются, как описано [для \_ команды MCI](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="88234-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="88234-126">Если этот параметр опущен, прямоугольником по умолчанию выделяется весь буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="88234-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="88234-127">С помощью последовательности команд Freeze и unfreeze с различными прямоугольниками можно описать произвольные шаблоны битов маски блокировки.</span><span class="sxs-lookup"><span data-stu-id="88234-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="88234-128">Для устройств с цифровыми видео параметр *лпунфризе* указывает на структуру **MCI \_ ДГВ \_ unfreeze \_ пармс** .</span><span class="sxs-lookup"><span data-stu-id="88234-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="88234-129">Дополнительные сведения см. в комментариях к структуре [**MCI \_ ДГВ \_ Rect \_ пармс**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="88234-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="88234-130">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="88234-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="88234-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>видеомагнитофон MCI \_ \_ разморозить \_ входные данные</span><span class="sxs-lookup"><span data-stu-id="88234-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="88234-132">Разморозить входные данные.</span><span class="sxs-lookup"><span data-stu-id="88234-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="88234-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_ \_ незамораживание \_ выходных данных видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="88234-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="88234-134">Разморозить выходные данные.</span><span class="sxs-lookup"><span data-stu-id="88234-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="88234-135">Для типа устройства **оверлея** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="88234-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="88234-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ овли \_ Rect</span><span class="sxs-lookup"><span data-stu-id="88234-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="88234-137">Элемент **RC** структуры, идентифицируемой *лпунфризе* , содержит допустимый отображаемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="88234-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="88234-138">Это обязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="88234-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="88234-139">Для устройств с наложением параметр *лпунфризе* указывает на структуру [**MCI \_ овли \_ Rect \_ пармс**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="88234-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="88234-140">Требования</span><span class="sxs-lookup"><span data-stu-id="88234-140">Requirements</span></span>



| <span data-ttu-id="88234-141">Требование</span><span class="sxs-lookup"><span data-stu-id="88234-141">Requirement</span></span> | <span data-ttu-id="88234-142">Значение</span><span class="sxs-lookup"><span data-stu-id="88234-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88234-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88234-143">Minimum supported client</span></span><br/> | <span data-ttu-id="88234-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="88234-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="88234-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88234-145">Minimum supported server</span></span><br/> | <span data-ttu-id="88234-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="88234-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88234-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="88234-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="88234-148"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88234-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88234-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88234-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88234-150">MCI</span><span class="sxs-lookup"><span data-stu-id="88234-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="88234-151">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="88234-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

