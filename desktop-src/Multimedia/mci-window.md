---
title: Команда MCI_WINDOW (Ммсистем. h)
description: '\_Команда окна MCI задает окно и характеристики для графических устройств. Эта команда распознает цифровые видеоролики и устройства наложения видео.'
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988801"
---
# <a name="mci_window-command"></a><span data-ttu-id="aa709-105">\_Команда окна MCI</span><span class="sxs-lookup"><span data-stu-id="aa709-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="aa709-106">\_Команда окна MCI задает окно и характеристики для графических устройств.</span><span class="sxs-lookup"><span data-stu-id="aa709-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="aa709-107">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="aa709-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="aa709-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="aa709-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="aa709-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa709-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa709-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="aa709-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="aa709-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="aa709-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="aa709-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="aa709-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="aa709-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="aa709-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="aa709-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="aa709-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa709-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*лпвиндов*</span><span class="sxs-lookup"><span data-stu-id="aa709-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="aa709-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="aa709-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="aa709-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="aa709-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa709-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa709-118">Return Value</span></span>

<span data-ttu-id="aa709-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aa709-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa709-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa709-120">Remarks</span></span>

<span data-ttu-id="aa709-121">Графические устройства должны создавать окно по умолчанию, когда устройство открыто, но не должно отображать его, пока не получит команду [MCI \_ Play](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="aa709-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="aa709-122">\_Команда окна MCI используется для передачи на устройство окна, созданного приложением, и для изменения характеристик экрана, определенных приложением или окном просмотра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa709-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="aa709-123">Если приложение предоставляет окно просмотра, оно должно быть подготовлено к обновлению недопустимого прямоугольника в окне.</span><span class="sxs-lookup"><span data-stu-id="aa709-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="aa709-124">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="aa709-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="aa709-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_ \_ HWND окна MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="aa709-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="aa709-126">Дескриптор окна, необходимый для использования в качестве назначения, включается в элемент **HWND** структуры, идентифицируемой *лпвиндов*.</span><span class="sxs-lookup"><span data-stu-id="aa709-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="aa709-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>\_ \_ состояние окна MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="aa709-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="aa709-128">Элемент **нкмдшов** структуры, идентифицируемой *лпвиндов* , содержит параметры для установки состояния окна.</span><span class="sxs-lookup"><span data-stu-id="aa709-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="aa709-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>\_ \_ текст окна MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="aa709-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="aa709-130">Элемент **лпстртекст** структуры, идентифицируемой *лпвиндов* , содержит адрес буфера, содержащего заголовок, используемый в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="aa709-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="aa709-131">Для устройств с цифровыми видео параметр *лпвиндов* указывает на структуру [**\_ ДГВ \_ окна MCI \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="aa709-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="aa709-132">Для типа устройства **наложения** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="aa709-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="aa709-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>\_окно MCI \_ овли \_ Отключить \_ растяжение</span><span class="sxs-lookup"><span data-stu-id="aa709-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="aa709-134">Отключает растяжение изображения.</span><span class="sxs-lookup"><span data-stu-id="aa709-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="aa709-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_окно MCI \_ овли \_ включить \_ растяжение</span><span class="sxs-lookup"><span data-stu-id="aa709-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="aa709-136">Включает растяжение изображения.</span><span class="sxs-lookup"><span data-stu-id="aa709-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="aa709-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_ \_ HWND окна MCI \_ овли</span><span class="sxs-lookup"><span data-stu-id="aa709-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="aa709-138">Дескриптор окна, используемого для назначения, включается в элемент **HWND** структуры, идентифицируемой *лпвиндов*.</span><span class="sxs-lookup"><span data-stu-id="aa709-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="aa709-139">Установите этот флаг в \_ окне MCI овли \_ Window Default, \_ чтобы вернуться в окно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa709-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="aa709-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_ \_ состояние окна MCI \_ овли</span><span class="sxs-lookup"><span data-stu-id="aa709-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="aa709-141">Элемент **нкмдшов** структуры *лпвиндов* содержит параметры для установки состояния окна.</span><span class="sxs-lookup"><span data-stu-id="aa709-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="aa709-142">Этот флаг эквивалентен вызову [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) с параметром *State* .</span><span class="sxs-lookup"><span data-stu-id="aa709-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="aa709-143">Константы аналогичны тем, которые определены в WINDOWS. H (например, скрытие программного отображения, программное \_ \_ СВЕРНУТЬ или SW \_ шовнормал).</span><span class="sxs-lookup"><span data-stu-id="aa709-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="aa709-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>\_ \_ текст окна MCI \_ овли</span><span class="sxs-lookup"><span data-stu-id="aa709-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="aa709-145">Элемент **лпстртекст** структуры, идентифицируемой *лпвиндов* , содержит адрес буфера, содержащего заголовок, используемый для окна.</span><span class="sxs-lookup"><span data-stu-id="aa709-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="aa709-146">Для устройств с наложением параметр *лпвиндов* указывает на структуру [**\_ овли окна MCI \_ \_ пармс**](mci-ovly-window-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="aa709-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa709-147">Требования</span><span class="sxs-lookup"><span data-stu-id="aa709-147">Requirements</span></span>



| <span data-ttu-id="aa709-148">Требование</span><span class="sxs-lookup"><span data-stu-id="aa709-148">Requirement</span></span> | <span data-ttu-id="aa709-149">Значение</span><span class="sxs-lookup"><span data-stu-id="aa709-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa709-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa709-150">Minimum supported client</span></span><br/> | <span data-ttu-id="aa709-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa709-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa709-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa709-152">Minimum supported server</span></span><br/> | <span data-ttu-id="aa709-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa709-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa709-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aa709-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa709-155"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa709-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa709-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa709-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa709-157">MCI</span><span class="sxs-lookup"><span data-stu-id="aa709-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="aa709-158">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="aa709-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

