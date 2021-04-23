---
description: '\_ \_ \_ \_ При считывании данных из удаленного файла или записи данных в удаленный файл с помощью лмра ioctl Disabled Local буферизации отключает кэширование данных на стороне клиента в памяти. Это внутренний определенный код элемента управления, недоступный в общедоступном заголовке.'
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Код элемента управления IOCTL_LMR_DISABLE_LOCAL_BUFFERING
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647137"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="9e9c7-104">IOCTL \_ ЛМР \_ отключение \_ \_ кода управления локальной буферизацией</span><span class="sxs-lookup"><span data-stu-id="9e9c7-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="9e9c7-105">При считывании данных из удаленного файла или записи данных в удаленный файл с помощью **\_ Лмра ioctl \_ disabled \_ Local \_ буферизации** отключает кэширование данных на стороне клиента в памяти.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="9e9c7-106">Это внутренний определенный код элемента управления, недоступный в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="9e9c7-107">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="9e9c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e9c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e9c7-109">*хдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-110">Маркер удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-110">A handle to the remote file.</span></span> <span data-ttu-id="9e9c7-111">Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="9e9c7-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-112">*двиоконтролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-113">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-113">The control code for the operation.</span></span> <span data-ttu-id="9e9c7-114">Используйте значение 0x140390 для этой операции.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-115">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="9e9c7-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9e9c7-116">Не используется, должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-117">*нинбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-118">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="9e9c7-119">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-120">*лпаутбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-121">Не используется, должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-122">*наутбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="9e9c7-124">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-125">*лпбитесретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-126">Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="9e9c7-127">Если выходной буфер слишком мал, вызов завершается неудачно, функция [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ недостаточный \_ Размер буфера**, а *лпбитесретурнед* равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="9e9c7-128">Если параметр *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="9e9c7-129">Даже если операция не возвращает выходные данные и параметр *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="9e9c7-130">После такой операции значение *лпбитесретурнед* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="9e9c7-131">Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="9e9c7-132">Если *лповерлаппед* не равно **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="9e9c7-133">Чтобы получить число возвращаемых байтов, вызовите функцию [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="9e9c7-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="9e9c7-134">Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных путем вызова функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="9e9c7-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="9e9c7-135">*лповерлаппед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e9c7-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9c7-136">Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="9e9c7-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="9e9c7-137">Если параметр *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="9e9c7-138">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="9e9c7-139">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="9e9c7-140">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="9e9c7-141">Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="9e9c7-142">В противном случае функция не возвращает значение до завершения операции или до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e9c7-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e9c7-143">Return value</span></span>

<span data-ttu-id="9e9c7-144">Если операция завершается успешно, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="9e9c7-145">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="9e9c7-146">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9e9c7-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9c7-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e9c7-147">Remarks</span></span>

<span data-ttu-id="9e9c7-148">**ЛМР ioctl \_ отключает код управления \_ \_ локальной \_ буферизации** внутри системы как 0x140390, а не в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="9e9c7-149">Он используется специальными приложениями для отключения локального кэширования данных на стороне клиента в памяти при считывании данных из удаленного файла или записи в него.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="9e9c7-150">После отключения локальной буферизации параметр остается в силе до тех пор, пока все открытые дескрипторы файла не будут закрыты и перенаправитель очистит внутренние структуры данных.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="9e9c7-151">Приложения общего назначения не должны использовать **ioctl \_ ЛМР \_ Отключить \_ локальную \_ буферизацию**, так как это может привести к чрезмерному сетевому трафику и снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="9e9c7-152">**ЛМР ioctl отключает управляющий код \_ \_ \_ локальной \_ буферизации** , который следует использовать только в специализированных приложениях, перемещающих большие объемы данных по сети при попытке максимизировать использование пропускной способности сети.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="9e9c7-153">Например, функции [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) и [**копифиликс**](/windows/win32/api/winbase/nf-winbase-copyfileexa) используют **ioctl \_ ЛМР \_ Отключить \_ локальную \_ буферизацию** для повышения производительности копирования больших файлов.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="9e9c7-154">Запрос **ioctl \_ ЛМР \_ отключение \_ локальной \_ буферизации** не реализовано локальными файловыми системами и завершается с ошибкой **\_ недопустимой \_ функции**.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="9e9c7-155">Выдача **ioctl \_ ЛМР \_ Отключение кода управления \_ локальной \_ буферизацией** в дескрипторах удаленных каталогов завершится ошибкой, так как ошибка **не будет \_ \_ поддерживаться**.</span><span class="sxs-lookup"><span data-stu-id="9e9c7-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e9c7-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e9c7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9c7-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="9e9c7-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
