---
title: Команда MCI_ESCAPE (Ммсистем. h)
description: '\_Управляющая команда MCI передает строку непосредственно на устройство. Устройства видеодиск распознают эту команду.'
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- MCI_ESCAPE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672681"
---
# <a name="mci_escape-command"></a><span data-ttu-id="d7471-105">\_Управляющая команда MCI</span><span class="sxs-lookup"><span data-stu-id="d7471-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="d7471-106">\_Управляющая команда MCI передает строку непосредственно на устройство.</span><span class="sxs-lookup"><span data-stu-id="d7471-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="d7471-107">Устройства видеодиск распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="d7471-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="d7471-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="d7471-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="d7471-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7471-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7471-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="d7471-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d7471-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="d7471-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d7471-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d7471-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d7471-113">\_Ожидание с уведомлением MCI или MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d7471-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="d7471-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d7471-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7471-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*лпескапе*</span><span class="sxs-lookup"><span data-stu-id="d7471-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="d7471-116">Указатель на структуру [**\_ \_ \_ пармс ESC VD**](mci-vd-escape-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d7471-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7471-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7471-117">Return Value</span></span>

<span data-ttu-id="d7471-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d7471-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7471-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7471-119">Remarks</span></span>

<span data-ttu-id="d7471-120">Данные, отправляемые с помощью управляющей клавиши MCI, \_ зависят от устройства и обычно передаются непосредственно на оборудование, связанное с устройством.</span><span class="sxs-lookup"><span data-stu-id="d7471-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="d7471-121">К устройствам видеодиск применяется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="d7471-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="d7471-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>\_Escape- \_ \_ строка VD MCI</span><span class="sxs-lookup"><span data-stu-id="d7471-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="d7471-123">Командная строка указывается в элементе **лпстркомманд** структуры, определенной параметром *лпескапе*.</span><span class="sxs-lookup"><span data-stu-id="d7471-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="d7471-124">Этот флаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d7471-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7471-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d7471-125">Requirements</span></span>



| <span data-ttu-id="d7471-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d7471-126">Requirement</span></span> | <span data-ttu-id="d7471-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d7471-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7471-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7471-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7471-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7471-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7471-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7471-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7471-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7471-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7471-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d7471-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7471-133"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7471-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7471-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7471-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7471-135">MCI</span><span class="sxs-lookup"><span data-stu-id="d7471-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d7471-136">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="d7471-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

