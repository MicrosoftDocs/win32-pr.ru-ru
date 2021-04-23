---
description: Получает текущее состояние аккумулятора.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: Код элемента управления IOCTL_BATTERY_QUERY_STATUS (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663119"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="31e1e-103">\_ \_ \_ Управляющий код состояния запроса аккумулятора ioctl</span><span class="sxs-lookup"><span data-stu-id="31e1e-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="31e1e-104">Получает текущее состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="31e1e-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="31e1e-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="31e1e-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="31e1e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31e1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e1e-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="31e1e-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-108">Маркер аккумулятора, из которого возвращаются сведения.</span><span class="sxs-lookup"><span data-stu-id="31e1e-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="31e1e-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="31e1e-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="31e1e-111">The control code for the operation.</span></span> <span data-ttu-id="31e1e-112">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="31e1e-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="31e1e-113">Использовать **\_ \_ \_ состояние запроса аккумулятора** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="31e1e-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="31e1e-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-115">Указатель на структуру [**\_ \_ состояния ожидания аккумулятора**](battery-wait-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-116">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="31e1e-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="31e1e-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-118">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="31e1e-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-119">Указатель на структуру [**\_ состояния аккумулятора**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-120">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="31e1e-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-121">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="31e1e-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-122">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="31e1e-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-123">Указатель на переменную, которая получает размер данных, возвращаемых в буфере *лпаутбуффер* , в байтах.</span><span class="sxs-lookup"><span data-stu-id="31e1e-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="31e1e-124">Если выходной буфер слишком мал для возвращения каких-либо данных, то вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки **\_ недостаточный \_ Размер буфера**, а возвращенное число байтов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="31e1e-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="31e1e-125">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="31e1e-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="31e1e-126">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="31e1e-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="31e1e-127">Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="31e1e-128">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="31e1e-129">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="31e1e-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="31e1e-130">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="31e1e-131">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , *ЛПОВЕРЛАППЕД* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="31e1e-132">В этом случае [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="31e1e-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="31e1e-133">Если устройство было открыто с флагом **File \_ Flag \_ OVERLAPPED** и *лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="31e1e-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="31e1e-134">Если *хдевице* был открыт без указания флага **File \_ Flag \_ OVERLAPPED** , *лповерлаппед* игнорируется и функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="31e1e-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e1e-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31e1e-135">Return value</span></span>

<span data-ttu-id="31e1e-136">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="31e1e-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="31e1e-137">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="31e1e-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="31e1e-138">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="31e1e-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="31e1e-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31e1e-139">Remarks</span></span>

<span data-ttu-id="31e1e-140">Этот параметр аккумулятора IOCTL получает состояние аккумулятора на момент возвращения операции.</span><span class="sxs-lookup"><span data-stu-id="31e1e-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="31e1e-141">Структура входных параметров, [**\_ \_ состояние ожидания аккумулятора**](battery-wait-status-str.md), указывает, когда состояние аккумулятора должно быть обработано и возвращено.</span><span class="sxs-lookup"><span data-stu-id="31e1e-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="31e1e-142">Запросы на состояние аккумулятора могут быть доступны для немедленного возврата или могут быть настроены на ожидание определенного условия перед завершением.</span><span class="sxs-lookup"><span data-stu-id="31e1e-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="31e1e-143">Например, можно установить запрос сведений о батарее, который ожидает, пока заряд батареи не достигнет заданной точки или не изменится состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="31e1e-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="31e1e-144">Все запросы сведений о батарее будут завершены с состоянием " **\_ файл ошибки \_ не \_ найден** ", если элемент **баттеритаг** запроса не соответствует значению текущего тега батареи.</span><span class="sxs-lookup"><span data-stu-id="31e1e-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="31e1e-145">(Дополнительные сведения см. в разделе " [теги батареи](battery-information.md) ".) Это используется, чтобы убедиться, что возвращенные сведения о батарее соответствуют запрошенному аккумулятору.</span><span class="sxs-lookup"><span data-stu-id="31e1e-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="31e1e-146">Влияние перекрывающегося ввода-вывода на эту операцию см. в разделе "Примечания" раздела [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="31e1e-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="31e1e-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="31e1e-147">Examples</span></span>

<span data-ttu-id="31e1e-148">Пример см. в разделе [Перечисление устройств аккумулятора](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="31e1e-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31e1e-149">Требования</span><span class="sxs-lookup"><span data-stu-id="31e1e-149">Requirements</span></span>



| <span data-ttu-id="31e1e-150">Требование</span><span class="sxs-lookup"><span data-stu-id="31e1e-150">Requirement</span></span> | <span data-ttu-id="31e1e-151">Значение</span><span class="sxs-lookup"><span data-stu-id="31e1e-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e1e-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31e1e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="31e1e-153">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31e1e-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="31e1e-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31e1e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="31e1e-155">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31e1e-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="31e1e-156">Header</span><span class="sxs-lookup"><span data-stu-id="31e1e-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e1e-157"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="31e1e-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e1e-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31e1e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e1e-159">Сведения о батарее</span><span class="sxs-lookup"><span data-stu-id="31e1e-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="31e1e-160">Управляющие коды управления питанием</span><span class="sxs-lookup"><span data-stu-id="31e1e-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="31e1e-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="31e1e-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="31e1e-162">**\_состояние аккумулятора**</span><span class="sxs-lookup"><span data-stu-id="31e1e-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="31e1e-163">**\_состояние ожидания \_ аккумулятора**</span><span class="sxs-lookup"><span data-stu-id="31e1e-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="31e1e-164">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="31e1e-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="31e1e-165">**\_тег запроса на батарею ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31e1e-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="31e1e-166">**\_ \_ сведения о настройке аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="31e1e-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

