---
title: зарезервировать команду
description: Команда Reserve выделяет непрерывное место на диске для рабочей области экземпляра устройства. Устройство Digital-Video распознает эту команду.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- резервирование команды мультимедиа Windows
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988218"
---
# <a name="reserve-command"></a><span data-ttu-id="168b4-105">зарезервировать команду</span><span class="sxs-lookup"><span data-stu-id="168b4-105">reserve command</span></span>

<span data-ttu-id="168b4-106">Команда Reserve выделяет непрерывное место на диске для рабочей области экземпляра устройства.</span><span class="sxs-lookup"><span data-stu-id="168b4-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="168b4-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="168b4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="168b4-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="168b4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="168b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="168b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="168b4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="168b4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="168b4-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="168b4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="168b4-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="168b4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="168b4-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*лпсзресерве*</span><span class="sxs-lookup"><span data-stu-id="168b4-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="168b4-114">Один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="168b4-114">One or more of the following flags.</span></span>



| <span data-ttu-id="168b4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="168b4-115">Value</span></span>           | <span data-ttu-id="168b4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="168b4-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="168b4-117">по *пути*</span><span class="sxs-lookup"><span data-stu-id="168b4-117">in *path*</span></span>       | <span data-ttu-id="168b4-118">Указывает диск и путь к каталогу (но не имя) временного файла, используемого для хранения записанных данных.</span><span class="sxs-lookup"><span data-stu-id="168b4-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="168b4-119">Имя этого файла указывается устройством.</span><span class="sxs-lookup"><span data-stu-id="168b4-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="168b4-120">Временный файл удаляется при закрытии устройства.</span><span class="sxs-lookup"><span data-stu-id="168b4-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="168b4-121">Если этот флаг опущен, устройство указывает расположение места на диске.</span><span class="sxs-lookup"><span data-stu-id="168b4-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="168b4-122">*Длительность* размера</span><span class="sxs-lookup"><span data-stu-id="168b4-122">size *duration*</span></span> | <span data-ttu-id="168b4-123">Указывает приблизительный объем дискового пространства, резервируемого в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="168b4-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="168b4-124">Значение *Duration* указывается в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="168b4-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="168b4-125">Устройство основывает оценку необходимого места на диске в следующих параметрах: запрошенное время, формат файла, алгоритм сжатия видео и звука и значения качества сжатия.</span><span class="sxs-lookup"><span data-stu-id="168b4-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="168b4-126">Если параметр [сетвидео](setvideo.md) "Record" имеет значение "OFF", то пространство резервируется только для аудио.</span><span class="sxs-lookup"><span data-stu-id="168b4-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="168b4-127">Если параметр [сетаудио](setaudio.md) "Record" имеет значение "OFF", то пространство резервируется только для видео.</span><span class="sxs-lookup"><span data-stu-id="168b4-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="168b4-128">Если оба варианта имеют значение OFF или если параметр *Duration* равен нулю, то пространство не резервируется и освобождается все существующие зарезервированные пространства.</span><span class="sxs-lookup"><span data-stu-id="168b4-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="168b4-129">Если этот флаг опущен, устройство будет использовать значение по умолчанию, определенное устройством.</span><span class="sxs-lookup"><span data-stu-id="168b4-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="168b4-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="168b4-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="168b4-131">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="168b4-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="168b4-132">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="168b4-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="168b4-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="168b4-133">Return Value</span></span>

<span data-ttu-id="168b4-134">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="168b4-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="168b4-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="168b4-135">Remarks</span></span>

<span data-ttu-id="168b4-136">При необходимости в последующих командах [записи](record.md) или [сохранения](save.md) используется пространство, зарезервированное этой командой.</span><span class="sxs-lookup"><span data-stu-id="168b4-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="168b4-137">Если Рабочая область содержит несохраненные данные, данные теряются.</span><span class="sxs-lookup"><span data-stu-id="168b4-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="168b4-138">Некоторые устройства не нуждаются в резервировании и игнорируют их.</span><span class="sxs-lookup"><span data-stu-id="168b4-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="168b4-139">Если место на диске не резервируется перед записью, команда Record выполняет неявное резервирование с флагами по умолчанию для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="168b4-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="168b4-140">Используйте явную команду резервирования, если требуется лучше контролировать задержку выделения места на диске, контролировать объем выделяемого пространства и контролировать место выделения места на диске.</span><span class="sxs-lookup"><span data-stu-id="168b4-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="168b4-141">Приложение может изменить объем и расположение ранее зарезервированного места на диске с помощью последующих команд резервирования.</span><span class="sxs-lookup"><span data-stu-id="168b4-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="168b4-142">Все выделенные и по-прежнему неиспользуемые места на диске не освобождаются до тех пор, пока не будут сохранены все записанные данные или пока не закроется экземпляр устройства.</span><span class="sxs-lookup"><span data-stu-id="168b4-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="168b4-143">Требования</span><span class="sxs-lookup"><span data-stu-id="168b4-143">Requirements</span></span>



| <span data-ttu-id="168b4-144">Требование</span><span class="sxs-lookup"><span data-stu-id="168b4-144">Requirement</span></span> | <span data-ttu-id="168b4-145">Значение</span><span class="sxs-lookup"><span data-stu-id="168b4-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="168b4-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="168b4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="168b4-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="168b4-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="168b4-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="168b4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="168b4-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="168b4-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="168b4-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="168b4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="168b4-151">MCI</span><span class="sxs-lookup"><span data-stu-id="168b4-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="168b4-152">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="168b4-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="168b4-153">record</span><span class="sxs-lookup"><span data-stu-id="168b4-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="168b4-154">сохранить</span><span class="sxs-lookup"><span data-stu-id="168b4-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="168b4-155">сетаудио</span><span class="sxs-lookup"><span data-stu-id="168b4-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="168b4-156">сетвидео</span><span class="sxs-lookup"><span data-stu-id="168b4-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

