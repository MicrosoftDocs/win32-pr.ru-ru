---
title: Команда MCI_UPDATE (Ммсистем. h)
description: '\_Команда обновления MCI обновляет прямоугольник экрана. Устройство Digital-Video распознает эту команду.'
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137386"
---
# <a name="mci_update-command"></a><span data-ttu-id="92acc-105">\_Команда обновления MCI</span><span class="sxs-lookup"><span data-stu-id="92acc-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="92acc-106">\_Команда обновления MCI обновляет прямоугольник экрана.</span><span class="sxs-lookup"><span data-stu-id="92acc-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="92acc-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="92acc-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="92acc-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="92acc-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="92acc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92acc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92acc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="92acc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="92acc-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="92acc-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="92acc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="92acc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="92acc-113">**MCI \_ УВЕДОМЛЕНИЕ**, **\_ Ожидание MCI** или, для устройств с цифровыми видео, **\_ тест MCI**.</span><span class="sxs-lookup"><span data-stu-id="92acc-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="92acc-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="92acc-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="92acc-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*лпдест*</span><span class="sxs-lookup"><span data-stu-id="92acc-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="92acc-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="92acc-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="92acc-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="92acc-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92acc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92acc-118">Return Value</span></span>

<span data-ttu-id="92acc-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="92acc-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92acc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92acc-120">Remarks</span></span>

<span data-ttu-id="92acc-121">С типом устройства "дигиталвидео" используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="92acc-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="92acc-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>ДГВ MCI, \_ \_ Обновление \_ HDC</span><span class="sxs-lookup"><span data-stu-id="92acc-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="92acc-123">Элемент **HDC** структуры, идентифицируемой *лпдест* , содержит допустимое окно контроллера домена для рисования.</span><span class="sxs-lookup"><span data-stu-id="92acc-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="92acc-124">Этот флаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="92acc-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="92acc-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ ДГВ \_ Rect</span><span class="sxs-lookup"><span data-stu-id="92acc-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="92acc-126">Элемент **RC** структуры, идентифицируемой *лпунфризе* , содержит допустимый отображаемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="92acc-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="92acc-127">Прямоугольник задает прямоугольник обрезки относительно прямоугольника клиента.</span><span class="sxs-lookup"><span data-stu-id="92acc-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="92acc-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_прорисовка ДГВ MCI с \_ обновлением \_</span><span class="sxs-lookup"><span data-stu-id="92acc-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="92acc-129">Приложение использует этот флаг при получении сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , предназначенного для экрана контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="92acc-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="92acc-130">Устройство буфера кадров обычно окрашивает ключевой цвет.</span><span class="sxs-lookup"><span data-stu-id="92acc-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="92acc-131">Если устройство вывода не имеет буфера кадров, команда MCI может игнорироваться \_ при использовании флага **\_ рисования MCI ДГВ \_ Update \_ Paint** , так как во время операции воспроизведения экран будет перерисовываться.</span><span class="sxs-lookup"><span data-stu-id="92acc-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="92acc-132">Для устройств с цифровыми видео параметр *лпдест* указывает на структуру [**MCI \_ ДГВ \_ Update \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .</span><span class="sxs-lookup"><span data-stu-id="92acc-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="92acc-133">Требования</span><span class="sxs-lookup"><span data-stu-id="92acc-133">Requirements</span></span>



| <span data-ttu-id="92acc-134">Требование</span><span class="sxs-lookup"><span data-stu-id="92acc-134">Requirement</span></span> | <span data-ttu-id="92acc-135">Значение</span><span class="sxs-lookup"><span data-stu-id="92acc-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92acc-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92acc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="92acc-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="92acc-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="92acc-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92acc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="92acc-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="92acc-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="92acc-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="92acc-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="92acc-141"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92acc-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92acc-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92acc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92acc-143">MCI</span><span class="sxs-lookup"><span data-stu-id="92acc-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="92acc-144">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="92acc-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

