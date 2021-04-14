---
title: Команда MCI_SIGNAL (Ммсистем. h)
description: Команда MCI \_ Signal задает указанную точку в рабочей области. Устройство Digital-Video распознает эту команду. МЦИАВИ поддерживает только один активный сигнал за раз.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415352"
---
# <a name="mci_signal-command"></a><span data-ttu-id="bfdaf-106">Сигнал MCI, \_ команда</span><span class="sxs-lookup"><span data-stu-id="bfdaf-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="bfdaf-107">Команда MCI \_ Signal задает указанную точку в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="bfdaf-108">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="bfdaf-109">МЦИАВИ поддерживает только один активный сигнал за раз.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="bfdaf-110">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="bfdaf-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfdaf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfdaf-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-113">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bfdaf-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-115">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="bfdaf-116">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bfdaf-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfdaf-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*лпсигнал*</span><span class="sxs-lookup"><span data-stu-id="bfdaf-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-118">Указатель на структуру [**\_ \_ \_ пармс сигнала MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .</span><span class="sxs-lookup"><span data-stu-id="bfdaf-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfdaf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfdaf-119">Return Value</span></span>

<span data-ttu-id="bfdaf-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfdaf-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfdaf-121">Remarks</span></span>

<span data-ttu-id="bfdaf-122">Окно, дескриптор которого вы указали в элементе **двкаллбакк** структуры [**\_ \_ \_ пармс сигнала MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) , получает сообщение mm \_ мЦисигнал.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="bfdaf-123">Следующие флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="bfdaf-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="bfdaf-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_сигнал ДГВ \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="bfdaf-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-125">В элемент **двпоситион** структуры, идентифицируемой *лпсигнал*, включается сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="bfdaf-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_ \_ Отмена сигнала ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="bfdaf-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-127">Удаляет значение сигнала, указанное в значении, связанном с \_ ДГВ \_ сигнала MCI \_ усервал.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="bfdaf-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_сигнал ДГВ \_ MCI \_ каждые</span><span class="sxs-lookup"><span data-stu-id="bfdaf-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-129">Значение сигнального периода включено в элемент **двпериод** структуры, идентифицируемой *лпсигнал*.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="bfdaf-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_ \_ Расположение сигнала ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="bfdaf-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-131">Устройство будет отправит значение расположения с сообщением Windows вместо указанного пользователем значения.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="bfdaf-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_ \_ УСЕРВАЛ сигнала MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="bfdaf-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="bfdaf-133">Значение типа данных включается в элемент **двусерпарм** структуры, идентифицируемой *лпсигнал*.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="bfdaf-134">Значение данных, связанное с этим запросом, возвращается в виде сообщения Windows.</span><span class="sxs-lookup"><span data-stu-id="bfdaf-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfdaf-135">Требования</span><span class="sxs-lookup"><span data-stu-id="bfdaf-135">Requirements</span></span>



| <span data-ttu-id="bfdaf-136">Требование</span><span class="sxs-lookup"><span data-stu-id="bfdaf-136">Requirement</span></span> | <span data-ttu-id="bfdaf-137">Значение</span><span class="sxs-lookup"><span data-stu-id="bfdaf-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdaf-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfdaf-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bfdaf-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfdaf-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bfdaf-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfdaf-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bfdaf-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfdaf-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bfdaf-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bfdaf-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfdaf-143"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfdaf-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfdaf-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfdaf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfdaf-145">MCI</span><span class="sxs-lookup"><span data-stu-id="bfdaf-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bfdaf-146">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="bfdaf-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

