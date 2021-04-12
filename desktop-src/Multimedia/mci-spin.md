---
title: Команда MCI_SPIN (Ммсистем. h)
description: Команда MCI \_ Spin запускает устройство. Устройства видеодиск распознают эту команду.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- MCI_SPIN команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415349"
---
# <a name="mci_spin-command"></a><span data-ttu-id="e6e7a-105">\_Команда MCI Spin</span><span class="sxs-lookup"><span data-stu-id="e6e7a-105">MCI\_SPIN command</span></span>

<span data-ttu-id="e6e7a-106">Команда MCI \_ Spin запускает устройство.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="e6e7a-107">Устройства видеодиск распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="e6e7a-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="e6e7a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6e7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e7a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="e6e7a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e6e7a-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="e6e7a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e6e7a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e6e7a-113">\_Ожидание с уведомлением MCI или MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="e6e7a-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="e6e7a-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e6e7a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6e7a-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*лпспин*</span><span class="sxs-lookup"><span data-stu-id="e6e7a-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="e6e7a-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e7a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="e6e7a-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="e6e7a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e7a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6e7a-118">Return Value</span></span>

<span data-ttu-id="e6e7a-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e7a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6e7a-120">Remarks</span></span>

<span data-ttu-id="e6e7a-121">Следующие дополнительные флаги применяются к устройствам видеодиск:</span><span class="sxs-lookup"><span data-stu-id="e6e7a-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="e6e7a-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>\_Счетчик VD \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="e6e7a-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="e6e7a-123">Останавливает вращение диска.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="e6e7a-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>\_регулятор MCI \_ VD \_</span><span class="sxs-lookup"><span data-stu-id="e6e7a-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="e6e7a-125">Начинает вращение диска.</span><span class="sxs-lookup"><span data-stu-id="e6e7a-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6e7a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e7a-126">Requirements</span></span>



| <span data-ttu-id="e6e7a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e6e7a-127">Requirement</span></span> | <span data-ttu-id="e6e7a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e6e7a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e7a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6e7a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e7a-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6e7a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e6e7a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6e7a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e7a-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6e7a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6e7a-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e6e7a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e7a-134"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6e7a-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e7a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6e7a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e7a-136">MCI</span><span class="sxs-lookup"><span data-stu-id="e6e7a-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6e7a-137">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="e6e7a-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

