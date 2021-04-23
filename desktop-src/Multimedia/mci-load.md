---
title: Команда MCI_LOAD (Ммсистем. h)
description: Команда MCI \_ Load загружает файл. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988180"
---
# <a name="mci_load-command"></a><span data-ttu-id="ac759-105">\_Команда загрузки MCI</span><span class="sxs-lookup"><span data-stu-id="ac759-105">MCI\_LOAD command</span></span>

<span data-ttu-id="ac759-106">Команда MCI \_ Load загружает файл.</span><span class="sxs-lookup"><span data-stu-id="ac759-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="ac759-107">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="ac759-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="ac759-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ac759-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="ac759-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac759-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac759-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="ac759-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ac759-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="ac759-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ac759-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ac759-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ac759-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="ac759-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="ac759-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ac759-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac759-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*лплоад*</span><span class="sxs-lookup"><span data-stu-id="ac759-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="ac759-116">Указатель на структуру [**\_ \_ пармс нагрузки MCI**](mci-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ac759-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="ac759-117">(Устройства с дополнительными параметрами могут заменить эту структуру структурой, зависящей от устройства.</span><span class="sxs-lookup"><span data-stu-id="ac759-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="ac759-118">Для устройств с цифровыми видео параметр **лплоад** указывает на структуру [**MCI \_ ДГВ \_ Load \_ пармс**](/previous-versions//dd743391(v=vs.85)) .)</span><span class="sxs-lookup"><span data-stu-id="ac759-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac759-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac759-119">Return Value</span></span>

<span data-ttu-id="ac759-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ac759-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac759-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac759-121">Remarks</span></span>

<span data-ttu-id="ac759-122">Следующий дополнительный флаг применяется ко всем устройствам, поддерживающим \_ загрузку MCI:</span><span class="sxs-lookup"><span data-stu-id="ac759-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="ac759-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_файл загрузки \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ac759-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="ac759-124">Элемент **лпфиленаме** структуры, идентифицируемой *лплоад* , содержит адрес буфера, содержащего имя файла.</span><span class="sxs-lookup"><span data-stu-id="ac759-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="ac759-125">Для типа устройства **оверлея** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="ac759-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ac759-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ овли \_ Rect</span><span class="sxs-lookup"><span data-stu-id="ac759-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="ac759-127">Элемент **RC** структуры, идентифицируемой *лплоад* , содержит допустимый экранный прямоугольник, определяющий область обновляемого видеобуфера.</span><span class="sxs-lookup"><span data-stu-id="ac759-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="ac759-128">Для устройств с наложением параметр *лплоад* указывает на структуру [**MCI \_ овли \_ Load \_ пармс**](mci-ovly-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ac759-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac759-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ac759-129">Requirements</span></span>



| <span data-ttu-id="ac759-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ac759-130">Requirement</span></span> | <span data-ttu-id="ac759-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ac759-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac759-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac759-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ac759-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac759-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac759-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac759-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ac759-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac759-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac759-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ac759-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac759-137"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac759-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac759-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac759-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac759-139">MCI</span><span class="sxs-lookup"><span data-stu-id="ac759-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ac759-140">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="ac759-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

