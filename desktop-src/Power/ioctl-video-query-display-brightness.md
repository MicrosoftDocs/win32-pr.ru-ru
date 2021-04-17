---
description: Извлекает текущие уровни подсветки AC и DC и текущее состояние электропитания.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: Код элемента управления IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS (Нтддвдео. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673806"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="9b88b-103">\_ \_ \_ \_ Код управления яркостью экрана запроса видео ioctl</span><span class="sxs-lookup"><span data-stu-id="9b88b-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="9b88b-104">\[Этот управляющий код доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9b88b-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9b88b-105">Поддержка этого кода элемента управления была удалена в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9b88b-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="9b88b-106">Вместо этого используйте класс [**вмимониторбригхтнесс**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) .\]</span><span class="sxs-lookup"><span data-stu-id="9b88b-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="9b88b-107">Извлекает текущие уровни подсветки AC и DC и текущее состояние электропитания.</span><span class="sxs-lookup"><span data-stu-id="9b88b-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="9b88b-108">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="9b88b-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="9b88b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b88b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b88b-110">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="9b88b-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-111">Маркер для \\ \\ . \\ ЖК-устройство.</span><span class="sxs-lookup"><span data-stu-id="9b88b-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="9b88b-112">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-113">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="9b88b-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-114">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="9b88b-114">The control code for the operation.</span></span> <span data-ttu-id="9b88b-115">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b88b-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="9b88b-116">Используйте для этой операции **\_ \_ \_ \_ яркость экрана запроса видео ioctl** .</span><span class="sxs-lookup"><span data-stu-id="9b88b-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-117">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="9b88b-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-118">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b88b-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-119">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="9b88b-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-120">Не используется в этой операции; присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="9b88b-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-121">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="9b88b-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-122">Указатель на буфер, который получит структуру [**\_ яркости экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-123">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="9b88b-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-124">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="9b88b-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-125">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="9b88b-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-126">Указатель на переменную, которая получает размер возвращаемых выходных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="9b88b-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="9b88b-127">Если выходной буфер слишком мал для возвращения каких-либо данных, вызов завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ недостаточный \_ Размер буфера, а возвращенное число байтов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9b88b-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="9b88b-128">Если выходной буфер слишком мал для хранения всех данных, но может содержать некоторые записи, то операционная система возвращает столько, сколько подходит, вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ Дополнительные \_ данные, а *лпбитесретурнед* указывает объем возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="9b88b-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="9b88b-129">Приложение должно повторно вызвать [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с той же операцией, указав новую отправную точку.</span><span class="sxs-lookup"><span data-stu-id="9b88b-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="9b88b-130">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b88b-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="9b88b-131">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b88b-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="9b88b-132">Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="9b88b-133">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="9b88b-134">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="9b88b-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="9b88b-135">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="9b88b-136">Если *хдевице* был открыт с \_ \_ флагом File Flag OVERLAPPED, *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="9b88b-137">В этом случае операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="9b88b-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="9b88b-138">Если устройство было открыто с \_ флагом File Flag \_ OVERLAPPED и *Лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="9b88b-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="9b88b-139">Если *хдевице* был открыт без указания \_ \_ флага File Flag OVERLAPPED, *Лповерлаппед* игнорируется, а [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="9b88b-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b88b-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b88b-140">Return value</span></span>

<span data-ttu-id="9b88b-141">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9b88b-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="9b88b-142">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="9b88b-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="9b88b-143">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9b88b-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b88b-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b88b-144">Remarks</span></span>

<span data-ttu-id="9b88b-145">Файл заголовка, используемый для создания приложений, включающих эту функцию, Нтддвдео. h, входит в состав пакета средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="9b88b-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="9b88b-146">Сведения о получении DDK см. в разделе [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="9b88b-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="9b88b-147">Кроме того, этот код элемента управления можно определить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9b88b-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="9b88b-148">Требования</span><span class="sxs-lookup"><span data-stu-id="9b88b-148">Requirements</span></span>



| <span data-ttu-id="9b88b-149">Требование</span><span class="sxs-lookup"><span data-stu-id="9b88b-149">Requirement</span></span> | <span data-ttu-id="9b88b-150">Значение</span><span class="sxs-lookup"><span data-stu-id="9b88b-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b88b-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b88b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9b88b-152">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b88b-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b88b-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b88b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9b88b-154">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b88b-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b88b-155">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9b88b-155">End of client support</span></span><br/>    | <span data-ttu-id="9b88b-156">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="9b88b-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="9b88b-157">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9b88b-157">End of server support</span></span><br/>    | <span data-ttu-id="9b88b-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b88b-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="9b88b-159">Header</span><span class="sxs-lookup"><span data-stu-id="9b88b-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b88b-160"><dt>Нтддвдео. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b88b-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b88b-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b88b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b88b-162">Интерфейс управления подсветкой</span><span class="sxs-lookup"><span data-stu-id="9b88b-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="9b88b-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="9b88b-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="9b88b-164">[**\_яркость экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b88b-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9b88b-165">**\_ \_ Настройка \_ яркости экрана для видео ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="9b88b-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

