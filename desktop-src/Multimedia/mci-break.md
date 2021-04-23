---
title: Команда MCI_BREAK (Ммсистем. h)
description: Команда MCI \_ break задает ключ разрыва для устройства MCI. MCI поддерживает эту команду напрямую, а не передает ее на устройство. С помощью этой команды можно использовать любое приложение MCI.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490131"
---
# <a name="mci_break-command"></a><span data-ttu-id="3c55b-106">\_Команда MCI Break</span><span class="sxs-lookup"><span data-stu-id="3c55b-106">MCI\_BREAK command</span></span>

<span data-ttu-id="3c55b-107">Команда MCI \_ break задает ключ разрыва для устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="3c55b-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="3c55b-108">MCI поддерживает эту команду напрямую, а не передает ее на устройство.</span><span class="sxs-lookup"><span data-stu-id="3c55b-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="3c55b-109">С помощью этой команды можно использовать любое приложение MCI.</span><span class="sxs-lookup"><span data-stu-id="3c55b-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="3c55b-110">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3c55b-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="3c55b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c55b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c55b-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="3c55b-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3c55b-113">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="3c55b-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="3c55b-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3c55b-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3c55b-115">\_Уведомление MCI, \_ Ожидание MCI или, для устройств записи цифрового видео и видеокассеты (видеомагнитофон), \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="3c55b-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="3c55b-116">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3c55b-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c55b-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*лпбреак*</span><span class="sxs-lookup"><span data-stu-id="3c55b-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="3c55b-118">Указатель на структуру [**\_ \_ пармс для разрыва MCI**](mci-break-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="3c55b-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c55b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c55b-119">Return Value</span></span>

<span data-ttu-id="3c55b-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3c55b-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c55b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c55b-121">Remarks</span></span>

<span data-ttu-id="3c55b-122">Может потребоваться несколько раз нажать клавишу Break, чтобы прервать операцию ожидания.</span><span class="sxs-lookup"><span data-stu-id="3c55b-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="3c55b-123">Нажатие клавиши break после завершения ожидания устройства отменяет возможность отправки перерыва в приложение.</span><span class="sxs-lookup"><span data-stu-id="3c55b-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="3c55b-124">Если приложение содержит действие, определенное для кода виртуального ключа, оно может случайно ответить на прерывание.</span><span class="sxs-lookup"><span data-stu-id="3c55b-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="3c55b-125">Например, приложение, использующее VK \_ Cancel для сочетания клавиш, может ответить на клавишу Ctrl + Break по умолчанию, если она нажата после отмены ожидания.</span><span class="sxs-lookup"><span data-stu-id="3c55b-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="3c55b-126">Следующие дополнительные флаги применяются ко всем устройствам:</span><span class="sxs-lookup"><span data-stu-id="3c55b-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="3c55b-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND разрыва MCI \_</span><span class="sxs-lookup"><span data-stu-id="3c55b-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="3c55b-128">Элемент **хвндбреак** структуры, идентифицируемой *лпбреак* , содержит маркер окна, который должен быть текущим окном, чтобы включить обнаружение прерываний для этого устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="3c55b-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="3c55b-129">Обычно это главное окно приложения.</span><span class="sxs-lookup"><span data-stu-id="3c55b-129">This is usually the application's main window.</span></span> <span data-ttu-id="3c55b-130">Если этот параметр опущен, MCI не проверяет окно текущего окна.</span><span class="sxs-lookup"><span data-stu-id="3c55b-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="3c55b-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_ключ разрыва MCI \_</span><span class="sxs-lookup"><span data-stu-id="3c55b-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="3c55b-132">Элемент **нвирткэй** структуры, определяемой параметром *лпбреак* , указывает код виртуального ключа, используемый для ключа разрыва.</span><span class="sxs-lookup"><span data-stu-id="3c55b-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="3c55b-133">По умолчанию MCI назначает сочетание клавиш CTRL + BREAK в качестве клавиши разрыва.</span><span class="sxs-lookup"><span data-stu-id="3c55b-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="3c55b-134">Этот флаг необходим, если \_ \_ не указан разрыв MCI.</span><span class="sxs-lookup"><span data-stu-id="3c55b-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="3c55b-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>\_разрыв MCI \_ отключен</span><span class="sxs-lookup"><span data-stu-id="3c55b-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="3c55b-136">Отключает любой существующий ключ разрыва для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="3c55b-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c55b-137">Требования</span><span class="sxs-lookup"><span data-stu-id="3c55b-137">Requirements</span></span>



| <span data-ttu-id="3c55b-138">Требование</span><span class="sxs-lookup"><span data-stu-id="3c55b-138">Requirement</span></span> | <span data-ttu-id="3c55b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="3c55b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c55b-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c55b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3c55b-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c55b-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c55b-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c55b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3c55b-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c55b-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c55b-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3c55b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c55b-145"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c55b-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c55b-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c55b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c55b-147">MCI</span><span class="sxs-lookup"><span data-stu-id="3c55b-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3c55b-148">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="3c55b-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

