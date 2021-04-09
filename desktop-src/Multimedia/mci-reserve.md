---
title: Команда MCI_RESERVE (Ммсистем. h)
description: Команда " \_ резервировать" MCI выделяет непрерывное место на диске для рабочей области экземпляра драйвера устройства для использования с последующей записью. Устройство Digital-Video распознает эту команду.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989121"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="2670b-105">Команда "резервировать" MCI \_</span><span class="sxs-lookup"><span data-stu-id="2670b-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="2670b-106">Команда " \_ резервировать" MCI выделяет непрерывное место на диске для рабочей области экземпляра драйвера устройства для использования с последующей записью.</span><span class="sxs-lookup"><span data-stu-id="2670b-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="2670b-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="2670b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="2670b-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="2670b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="2670b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2670b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2670b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="2670b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2670b-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2670b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2670b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2670b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2670b-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="2670b-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2670b-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2670b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2670b-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*лпресерве*</span><span class="sxs-lookup"><span data-stu-id="2670b-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="2670b-116">Указатель на структуру [**\_ \_ \_ пармс ДГВ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="2670b-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2670b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2670b-117">Return Value</span></span>

<span data-ttu-id="2670b-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2670b-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2670b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2670b-119">Remarks</span></span>

<span data-ttu-id="2670b-120">Если Рабочая область содержит несохраненные данные, эти данные теряются.</span><span class="sxs-lookup"><span data-stu-id="2670b-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="2670b-121">Если место на диске не резервируется перед записью, команда [MCI \_ Record](mci-record.md) выполняет неявное резервирование с параметрами по умолчанию для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="2670b-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="2670b-122">В некоторых реализациях резервирование не требуется и может игнорироваться драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="2670b-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="2670b-123">Явное резервирование пространства позволяет лучше контролировать время задержки выделения места на диске, объем выделяемого пространства и место, где выделяется место на диске.</span><span class="sxs-lookup"><span data-stu-id="2670b-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="2670b-124">Объем и расположение места на диске, уже зарезервированные для этого экземпляра устройства, можно изменить, выполнив \_ повторный ввод MCI.</span><span class="sxs-lookup"><span data-stu-id="2670b-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="2670b-125">Все выделенные и по-прежнему неиспользуемые места на диске не освобождаются до тех пор, пока не будут сохранены все записанные данные или не будет закрыт экземпляр драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="2670b-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="2670b-126">Если видео отключено с \_ флагом MCI Off команды [MCI \_ сетвидео](mci-setvideo.md) , зарезервированное пространство не включает видео.</span><span class="sxs-lookup"><span data-stu-id="2670b-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="2670b-127">Если звук выключен с \_ флагом MCI Off команды [MCI \_ сетаудио](mci-setaudio.md) , зарезервированное пространство не включает звук.</span><span class="sxs-lookup"><span data-stu-id="2670b-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="2670b-128">Если звук и видео отключены или если запрошенный размер равен нулю, пространство не резервируется и освобождается все существующие зарезервированные пространства.</span><span class="sxs-lookup"><span data-stu-id="2670b-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="2670b-129">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="2670b-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="2670b-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_резерв ДГВ \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="2670b-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="2670b-131">Элемент **лпстрпас** структуры, идентифицируемой *лпресерве* , содержит адрес буфера, содержащего расположение временного файла.</span><span class="sxs-lookup"><span data-stu-id="2670b-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="2670b-132">Буфер содержит только диск и путь к каталогу файла, который используется для хранения записанных данных. имя файла указывается драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="2670b-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="2670b-133">Этот временный файл удаляется при закрытии экземпляра устройства, если он не сохранен явным образом.</span><span class="sxs-lookup"><span data-stu-id="2670b-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="2670b-134">Если этот флаг опущен, драйвер устройства указывает, где выделяется место на диске.</span><span class="sxs-lookup"><span data-stu-id="2670b-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="2670b-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_ \_ резервный размер MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="2670b-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="2670b-136">Элемент **двсизе** структуры, идентифицируемой *лпресерве* , указывает приблизительный объем дискового пространства, резервируемого в рабочей области для записи.</span><span class="sxs-lookup"><span data-stu-id="2670b-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="2670b-137">Значение указывается в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="2670b-137">The value is specified in the current time format.</span></span> <span data-ttu-id="2670b-138">Оценка объема дискового пространства определяется по запрошенному времени и от формата файла, используемого алгоритма видео и звука и значений качества.</span><span class="sxs-lookup"><span data-stu-id="2670b-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="2670b-139">Если этот флаг опущен, драйвер устройства может использовать значение по умолчанию, которое он определяет.</span><span class="sxs-lookup"><span data-stu-id="2670b-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2670b-140">Требования</span><span class="sxs-lookup"><span data-stu-id="2670b-140">Requirements</span></span>



| <span data-ttu-id="2670b-141">Требование</span><span class="sxs-lookup"><span data-stu-id="2670b-141">Requirement</span></span> | <span data-ttu-id="2670b-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2670b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2670b-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2670b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2670b-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2670b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2670b-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2670b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2670b-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2670b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2670b-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2670b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2670b-148"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2670b-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2670b-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2670b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2670b-150">MCI</span><span class="sxs-lookup"><span data-stu-id="2670b-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2670b-151">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="2670b-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

