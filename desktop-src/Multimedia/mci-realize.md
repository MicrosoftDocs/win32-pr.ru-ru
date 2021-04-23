---
title: Команда MCI_REALIZE (Ммсистем. h)
description: Команда MCI \_ понимает, что графическое устройство реализует свою палитру в контексте устройства (DC). Устройство Digital-Video распознает эту команду.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650372"
---
# <a name="mci_realize-command"></a><span data-ttu-id="3caf0-105">\_Команда MCI</span><span class="sxs-lookup"><span data-stu-id="3caf0-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="3caf0-106">Команда MCI \_ понимает, что графическое устройство реализует свою палитру в контексте устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="3caf0-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="3caf0-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="3caf0-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="3caf0-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3caf0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="3caf0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3caf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3caf0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="3caf0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3caf0-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="3caf0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="3caf0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3caf0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3caf0-113">**MCI \_ УВЕДОМЛЕНИЕ**, **\_ Ожидание MCI** или, для устройств с цифровыми видео, **\_ тест MCI**.</span><span class="sxs-lookup"><span data-stu-id="3caf0-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="3caf0-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3caf0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3caf0-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*лпреализе*</span><span class="sxs-lookup"><span data-stu-id="3caf0-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="3caf0-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="3caf0-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="3caf0-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="3caf0-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3caf0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3caf0-118">Return Value</span></span>

<span data-ttu-id="3caf0-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3caf0-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3caf0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3caf0-120">Remarks</span></span>

<span data-ttu-id="3caf0-121">Эту команду следует использовать, когда приложение получает сообщение [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="3caf0-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="3caf0-122">С типом устройства "дигиталвидео" используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="3caf0-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="3caf0-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ ДГВ \_ \_ бкгд</span><span class="sxs-lookup"><span data-stu-id="3caf0-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="3caf0-124">Реализует палитру в виде палитры фона.</span><span class="sxs-lookup"><span data-stu-id="3caf0-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="3caf0-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>\_ \_ норма реализации MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="3caf0-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="3caf0-126">Реализует палитру в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="3caf0-126">Realizes the palette normally.</span></span> <span data-ttu-id="3caf0-127">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3caf0-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="3caf0-128">Для устройств с цифровыми видео параметр *лпреализе* указывает на структуру **MCI \_ \_ пармс** .</span><span class="sxs-lookup"><span data-stu-id="3caf0-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="3caf0-129">Дополнительные сведения см. в разделе комментарии в структуре [**MCI \_ Generic \_ пармс**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="3caf0-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3caf0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3caf0-130">Requirements</span></span>



| <span data-ttu-id="3caf0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3caf0-131">Requirement</span></span> | <span data-ttu-id="3caf0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3caf0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3caf0-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3caf0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3caf0-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3caf0-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3caf0-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3caf0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3caf0-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3caf0-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3caf0-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3caf0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3caf0-138"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3caf0-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3caf0-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3caf0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3caf0-140">MCI</span><span class="sxs-lookup"><span data-stu-id="3caf0-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3caf0-141">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="3caf0-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

