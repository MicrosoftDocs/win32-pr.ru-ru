---
description: Извлекает текущий тег аккумулятора.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: Код элемента управления IOCTL_BATTERY_QUERY_TAG (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673808"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="7d92f-103">\_ \_ \_ Код элемента управления тега запроса на батарею ioctl</span><span class="sxs-lookup"><span data-stu-id="7d92f-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="7d92f-104">Извлекает текущий тег батареи.</span><span class="sxs-lookup"><span data-stu-id="7d92f-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="7d92f-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="7d92f-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="7d92f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d92f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d92f-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="7d92f-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-108">Маркер батареи, из которого извлекается тег.</span><span class="sxs-lookup"><span data-stu-id="7d92f-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="7d92f-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="7d92f-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="7d92f-111">The control code for the operation.</span></span> <span data-ttu-id="7d92f-112">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d92f-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="7d92f-113">Для этой операции используйте **\_ \_ \_ тег запроса на батарею от аккумулятора** .</span><span class="sxs-lookup"><span data-stu-id="7d92f-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="7d92f-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-115">Указатель на входной буфер типа **ulong** .</span><span class="sxs-lookup"><span data-stu-id="7d92f-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="7d92f-116">Значение указывает время ожидания в миллисекундах при отсутствии аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="7d92f-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="7d92f-117">Значение-1 указывает на то, что запрос будет ждать бесконечно (или пока не отменяется другим событием).</span><span class="sxs-lookup"><span data-stu-id="7d92f-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-118">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="7d92f-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-119">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7d92f-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-120">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="7d92f-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-121">Указатель на выходной буфер **ulong** .</span><span class="sxs-lookup"><span data-stu-id="7d92f-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="7d92f-122">При успешном выполнении этот буфер содержит тег текущего аккумулятора, который может быть любым значением, кроме тега батареи, является \_ \_ недопустимым.</span><span class="sxs-lookup"><span data-stu-id="7d92f-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="7d92f-123">В случае сбоя, если [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает файл с кодом ошибки **\_ \_ не \_ найден**, этот буфер содержит **\_ \_ Недопустимый тег** значения для батареи.</span><span class="sxs-lookup"><span data-stu-id="7d92f-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-124">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="7d92f-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-125">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7d92f-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-126">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="7d92f-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-127">Указатель на переменную, которая получает размер данных, хранящихся в буфере *лпаутбуффер* , в байтах.</span><span class="sxs-lookup"><span data-stu-id="7d92f-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="7d92f-128">Если выходной буфер слишком мал для возвращения каких-либо данных, то вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки **\_ недостаточный \_ Размер буфера**, а возвращенное число байтов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d92f-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="7d92f-129">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7d92f-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="7d92f-130">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7d92f-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="7d92f-131">Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="7d92f-132">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="7d92f-133">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="7d92f-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="7d92f-134">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="7d92f-135">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , *ЛПОВЕРЛАППЕД* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="7d92f-136">В этом случае [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="7d92f-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="7d92f-137">Если устройство было открыто с флагом **File \_ Flag \_ OVERLAPPED** и *лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="7d92f-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="7d92f-138">Если *хдевице* был открыт без указания флага **File \_ Flag \_ OVERLAPPED** , *лповерлаппед* игнорируется и функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d92f-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d92f-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d92f-139">Return value</span></span>

<span data-ttu-id="7d92f-140">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7d92f-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="7d92f-141">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7d92f-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="7d92f-142">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7d92f-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d92f-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d92f-143">Remarks</span></span>

<span data-ttu-id="7d92f-144">Этот параметр аккумулятора IOCTL получает текущий тег батареи.</span><span class="sxs-lookup"><span data-stu-id="7d92f-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="7d92f-145">Тег батареи — это уникальное ненулевое значение, которое изменяется при повторной вставке, замене или изменении характеристик физической батареи.</span><span class="sxs-lookup"><span data-stu-id="7d92f-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="7d92f-146">Дополнительные сведения об изменении тега аккумулятора, обнаружении изменений и возможностях работы приложения после изменения тега батареи см. в разделе "Теги батареи" в разделе "Общие [сведения о батарее](battery-information.md) ".</span><span class="sxs-lookup"><span data-stu-id="7d92f-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="7d92f-147">Если батарея отсутствует, этот запрос будет ждать указанного времени, и если батарея по-прежнему отсутствует, то будет возвращен **файл ошибки, который \_ \_ не \_ найден** , и установлен тег аккумулятора на **\_ \_ Недопустимый тег** аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="7d92f-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="7d92f-148">(Дополнительные сведения см. в разделе сведения о батарее.)</span><span class="sxs-lookup"><span data-stu-id="7d92f-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="7d92f-149">Для всех запросов других сведений о батарее требуется, чтобы вызывающий объект предоставил соответствующий тег батареи.</span><span class="sxs-lookup"><span data-stu-id="7d92f-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="7d92f-150">Это гарантирует, что вызывающий объект получает информацию для одного и того же аккумулятора для каждого запроса и гарантирует, что вызывающий объект знает об изменениях аккумулятора без постоянного опроса.</span><span class="sxs-lookup"><span data-stu-id="7d92f-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="7d92f-151">Влияние перекрывающегося ввода-вывода на эту операцию см. в разделе "Примечания" раздела [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="7d92f-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="7d92f-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="7d92f-152">Examples</span></span>

<span data-ttu-id="7d92f-153">Пример см. в разделе [Перечисление устройств аккумулятора](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="7d92f-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d92f-154">Требования</span><span class="sxs-lookup"><span data-stu-id="7d92f-154">Requirements</span></span>



| <span data-ttu-id="7d92f-155">Требование</span><span class="sxs-lookup"><span data-stu-id="7d92f-155">Requirement</span></span> | <span data-ttu-id="7d92f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="7d92f-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d92f-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d92f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7d92f-158">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7d92f-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="7d92f-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d92f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7d92f-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d92f-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="7d92f-161">Header</span><span class="sxs-lookup"><span data-stu-id="7d92f-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d92f-162"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="7d92f-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d92f-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d92f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d92f-164">Сведения о батарее</span><span class="sxs-lookup"><span data-stu-id="7d92f-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="7d92f-165">Управляющие коды управления питанием</span><span class="sxs-lookup"><span data-stu-id="7d92f-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="7d92f-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="7d92f-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="7d92f-167">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="7d92f-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="7d92f-168">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="7d92f-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="7d92f-169">**\_ \_ сведения о настройке аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="7d92f-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

