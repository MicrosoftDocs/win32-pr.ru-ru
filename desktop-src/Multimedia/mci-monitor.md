---
title: Команда MCI_MONITOR (Ммсистем. h)
description: '\_Команда монитора MCI указывает источник представления. Устройство Digital-Video распознает эту команду.'
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988963"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="512f6-105">\_Команда монитора MCI</span><span class="sxs-lookup"><span data-stu-id="512f6-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="512f6-106">\_Команда монитора MCI указывает источник представления.</span><span class="sxs-lookup"><span data-stu-id="512f6-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="512f6-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="512f6-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="512f6-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="512f6-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="512f6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="512f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="512f6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="512f6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="512f6-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="512f6-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="512f6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="512f6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="512f6-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="512f6-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="512f6-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="512f6-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="512f6-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*лпмонитор*</span><span class="sxs-lookup"><span data-stu-id="512f6-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="512f6-116">Указатель на структуру [**\_ \_ \_ пармс монитора MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .</span><span class="sxs-lookup"><span data-stu-id="512f6-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="512f6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="512f6-117">Return Value</span></span>

<span data-ttu-id="512f6-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="512f6-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="512f6-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="512f6-119">Remarks</span></span>

<span data-ttu-id="512f6-120">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="512f6-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="512f6-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_ \_ метод монитора MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="512f6-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="512f6-122">Константа, указывающая метод мониторинга, включается в элемент **двмесод** структуры, идентифицируемой *лпмонитор*.</span><span class="sxs-lookup"><span data-stu-id="512f6-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="512f6-123">Если в элементе \_ \_ \_ **ДВСАУРЦЕ** используется флаг ввода MCI ДГВ, выбирается метод мониторинга.</span><span class="sxs-lookup"><span data-stu-id="512f6-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="512f6-124">Как правило, различные методы мониторинга имеют различные последствия использования оборудования.</span><span class="sxs-lookup"><span data-stu-id="512f6-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="512f6-125">На устройстве выбирается метод мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="512f6-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="512f6-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_ \_ источник монитора MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="512f6-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="512f6-127">Константа, указывающая, что источник монитора включен в элемент **двсаурце** структуры, идентифицируемой *лпмонитор*.</span><span class="sxs-lookup"><span data-stu-id="512f6-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="512f6-128">Требования</span><span class="sxs-lookup"><span data-stu-id="512f6-128">Requirements</span></span>



| <span data-ttu-id="512f6-129">Требование</span><span class="sxs-lookup"><span data-stu-id="512f6-129">Requirement</span></span> | <span data-ttu-id="512f6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="512f6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="512f6-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="512f6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="512f6-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="512f6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="512f6-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="512f6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="512f6-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="512f6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="512f6-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="512f6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="512f6-136"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="512f6-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="512f6-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="512f6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512f6-138">MCI</span><span class="sxs-lookup"><span data-stu-id="512f6-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="512f6-139">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="512f6-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

