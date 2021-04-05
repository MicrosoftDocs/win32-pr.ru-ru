---
description: Задает различные сведения о батарее.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: Код элемента управления IOCTL_BATTERY_SET_INFORMATION (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909699"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="78072-103">\_ \_ Контрольный код для настройки аккумулятора с ПАРАМЕТРом ioctl \_</span><span class="sxs-lookup"><span data-stu-id="78072-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="78072-104">Задает различные сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="78072-104">Sets various battery information.</span></span> <span data-ttu-id="78072-105">Структура входных параметров, [**\_ \_ информация о заряде аккумулятора**](battery-set-information-str.md), указывает, какие сведения о состоянии аккумулятора должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="78072-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="78072-106">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="78072-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="78072-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="78072-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78072-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="78072-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-109">Маркер батареи, для которого задаются сведения.</span><span class="sxs-lookup"><span data-stu-id="78072-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="78072-110">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="78072-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="78072-111">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="78072-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-112">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="78072-112">The control code for the operation.</span></span> <span data-ttu-id="78072-113">Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="78072-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="78072-114">Использовать **\_ \_ \_ сведения о настройке аккумулятора** с помощью ioctl для этой операции.</span><span class="sxs-lookup"><span data-stu-id="78072-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="78072-115">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="78072-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-116">Указатель на структуру [**\_ \_ сведений о наборе аккумулятора**](battery-set-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="78072-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="78072-117">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="78072-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-118">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="78072-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="78072-119">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="78072-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-120">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="78072-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="78072-121">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="78072-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-122">Не используется в этой операции; присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="78072-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="78072-123">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="78072-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-124">Указатель на переменную, которая получает размер данных, возвращаемых в буфере *лпаутбуффер* , в байтах.</span><span class="sxs-lookup"><span data-stu-id="78072-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="78072-125">Если выходной буфер слишком мал для возвращения каких-либо данных, вызов завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ недостаточный \_ Размер буфера, а возвращенное число байтов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="78072-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="78072-126">Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**, даже если *лпаутбуффер* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="78072-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="78072-127">Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="78072-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="78072-128">Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="78072-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="78072-129">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="78072-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="78072-130">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="78072-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="78072-131">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="78072-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="78072-132">Если *хдевице* был открыт с \_ \_ флагом File Flag OVERLAPPED, *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="78072-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="78072-133">В этом случае [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="78072-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="78072-134">Если устройство было открыто с \_ флагом File Flag \_ OVERLAPPED и *Лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="78072-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="78072-135">Если *хдевице* был открыт без указания \_ \_ флага File Flag OVERLAPPED, *Лповерлаппед* игнорируется и функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="78072-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78072-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78072-136">Return value</span></span>

<span data-ttu-id="78072-137">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="78072-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="78072-138">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="78072-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="78072-139">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="78072-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="78072-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78072-140">Remarks</span></span>

<span data-ttu-id="78072-141">Все запросы на установку сведений о батарее будут завершаться с состоянием " \_ файл ошибки \_ не \_ найдено", если заданный в запросе тег батареи не соответствует значению текущего тега батареи.</span><span class="sxs-lookup"><span data-stu-id="78072-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="78072-142">Влияние перекрывающегося ввода-вывода на эту операцию см. в разделе "Примечания" раздела [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="78072-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="78072-143">Требования</span><span class="sxs-lookup"><span data-stu-id="78072-143">Requirements</span></span>



| <span data-ttu-id="78072-144">Требование</span><span class="sxs-lookup"><span data-stu-id="78072-144">Requirement</span></span> | <span data-ttu-id="78072-145">Значение</span><span class="sxs-lookup"><span data-stu-id="78072-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78072-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78072-146">Minimum supported client</span></span><br/> | <span data-ttu-id="78072-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="78072-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="78072-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78072-148">Minimum supported server</span></span><br/> | <span data-ttu-id="78072-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78072-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="78072-150">Header</span><span class="sxs-lookup"><span data-stu-id="78072-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="78072-151"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="78072-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78072-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78072-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78072-153">Сведения о батарее</span><span class="sxs-lookup"><span data-stu-id="78072-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="78072-154">Управляющие коды управления питанием</span><span class="sxs-lookup"><span data-stu-id="78072-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="78072-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="78072-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="78072-156">**\_ \_ сведения о настройке аккумулятора**</span><span class="sxs-lookup"><span data-stu-id="78072-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="78072-157">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="78072-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="78072-158">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="78072-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="78072-159">**\_тег запроса на батарею ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="78072-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

