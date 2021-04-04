---
title: Команда MCI_CAPTURE (Ммсистем. h)
description: '\_Команда захвата MCI захватывает содержимое буфера кадров и сохраняет его в указанном файле. Устройство Digital-Video распознает эту команду.'
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988966"
---
# <a name="mci_capture-command"></a><span data-ttu-id="6bb1e-105">\_Команда захвата MCI</span><span class="sxs-lookup"><span data-stu-id="6bb1e-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="6bb1e-106">\_Команда захвата MCI захватывает содержимое буфера кадров и сохраняет его в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="6bb1e-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6bb1e-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="6bb1e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bb1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb1e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="6bb1e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6bb1e-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6bb1e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6bb1e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6bb1e-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6bb1e-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6bb1e-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb1e-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*лпкаптуре*</span><span class="sxs-lookup"><span data-stu-id="6bb1e-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="6bb1e-116">Указатель на структуру [**\_ \_ \_ пармс захвата ДГВ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="6bb1e-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb1e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bb1e-117">Return Value</span></span>

<span data-ttu-id="6bb1e-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb1e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bb1e-119">Remarks</span></span>

<span data-ttu-id="6bb1e-120">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="6bb1e-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="6bb1e-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_захват ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="6bb1e-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="6bb1e-122">Элемент **лпстрфиленаме** структуры, идентифицируемой *лпкаптуре* , содержит адрес буфера, указывающего путь назначения и имя файла.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="6bb1e-123">(Этот флаг является обязательным.)</span><span class="sxs-lookup"><span data-stu-id="6bb1e-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="6bb1e-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_захват ДГВ \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="6bb1e-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="6bb1e-125">Элемент **RC** структуры, идентифицируемой *лпкаптуре* , содержит допустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="6bb1e-126">Прямоугольник указывает прямоугольную область внутри буфера фрейма, которая обрезается и сохраняется на диске.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="6bb1e-127">Если этот параметр опущен, то в обрезанной области по умолчанию используется прямоугольник, указанный или установленный по умолчанию в предыдущей команде [MCI \_ ](mci-put.md) , которая указывает исходную область для данного экземпляра драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="6bb1e-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bb1e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="6bb1e-128">Requirements</span></span>



| <span data-ttu-id="6bb1e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="6bb1e-129">Requirement</span></span> | <span data-ttu-id="6bb1e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6bb1e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb1e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bb1e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb1e-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6bb1e-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6bb1e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bb1e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb1e-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6bb1e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6bb1e-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6bb1e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb1e-136"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb1e-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb1e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bb1e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb1e-138">MCI</span><span class="sxs-lookup"><span data-stu-id="6bb1e-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6bb1e-139">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="6bb1e-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

