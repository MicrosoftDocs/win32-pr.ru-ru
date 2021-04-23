---
title: Команда MCI_RESTORE (Ммсистем. h)
description: Команда MCI \_ RESTORE Копирует растровое изображение из файла в буфер кадров. Устройство Digital-Video распознает эту команду. Эта команда выполняет обратное действие \_ команды захвата MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803257"
---
# <a name="mci_restore-command"></a><span data-ttu-id="3bac5-106">\_Команда восстановления MCI</span><span class="sxs-lookup"><span data-stu-id="3bac5-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="3bac5-107">Команда MCI \_ RESTORE Копирует растровое изображение из файла в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="3bac5-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="3bac5-108">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="3bac5-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="3bac5-109">Эта команда выполняет обратное действие команды [ \_ захвата MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="3bac5-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="3bac5-110">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3bac5-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="3bac5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bac5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bac5-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="3bac5-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3bac5-113">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="3bac5-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="3bac5-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3bac5-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3bac5-115">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="3bac5-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="3bac5-116">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3bac5-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bac5-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*лпресторе*</span><span class="sxs-lookup"><span data-stu-id="3bac5-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="3bac5-118">Указатель на структуру [**\_ \_ \_ пармс восстановления MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="3bac5-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bac5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bac5-119">Return Value</span></span>

<span data-ttu-id="3bac5-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3bac5-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bac5-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3bac5-121">Remarks</span></span>

<span data-ttu-id="3bac5-122">Реализация может распознать различные форматы изображений, но всегда принимается независимый от устройства точечный рисунок Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="3bac5-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="3bac5-123">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="3bac5-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="3bac5-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_Восстановление MCI \_ ДГВ \_ из</span><span class="sxs-lookup"><span data-stu-id="3bac5-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="3bac5-125">Элемент **лпстрфиленаме** структуры, идентифицируемой *лпресторе* , содержит адрес буфера, содержащего имя исходного файла.</span><span class="sxs-lookup"><span data-stu-id="3bac5-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="3bac5-126">Требуется указать имя файла.</span><span class="sxs-lookup"><span data-stu-id="3bac5-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="3bac5-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_Восстановление ДГВ \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="3bac5-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="3bac5-128">Элемент **RC** структуры, идентифицируемой *лпресторе* , содержит допустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="3bac5-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="3bac5-129">Прямоугольник задает область буфера фрейма относительно ее начала.</span><span class="sxs-lookup"><span data-stu-id="3bac5-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="3bac5-130">Первая пара координат задает верхний левый угол прямоугольника. Вторая пара указывает ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="3bac5-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="3bac5-131">Если этот флаг не указан, изображение копируется в левый верхний угол буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="3bac5-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bac5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3bac5-132">Requirements</span></span>



| <span data-ttu-id="3bac5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3bac5-133">Requirement</span></span> | <span data-ttu-id="3bac5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3bac5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bac5-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bac5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3bac5-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bac5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3bac5-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bac5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3bac5-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bac5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3bac5-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3bac5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bac5-140"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bac5-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bac5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bac5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bac5-142">MCI</span><span class="sxs-lookup"><span data-stu-id="3bac5-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3bac5-143">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="3bac5-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

