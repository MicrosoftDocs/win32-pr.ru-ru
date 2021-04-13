---
title: Управляющий код FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: Код элемента управления FSCTL_DFS_GET_PKT_ENTRY_STATE может получить те же сведения, что и функция Нетдфсжетклиентинфо, но может обеспечить лучшую производительность в некоторых конфигурациях с высокой задержкой для серверов DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539176"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="ff84e-103">Код элемента управления FSCTL_DFS_GET_PKT_ENTRY_STATE</span><span class="sxs-lookup"><span data-stu-id="ff84e-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="ff84e-104">Код элемента управления **FSCTL_DFS_GET_PKT_ENTRY_STATE** может получить те же сведения, что и функция [**нетдфсжетклиентинфо**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , но может обеспечить лучшую производительность в некоторых конфигурациях с высокой задержкой для серверов DFS.</span><span class="sxs-lookup"><span data-stu-id="ff84e-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="ff84e-105">Не рекомендуется использовать управляющий код **FSCTL_DFS_GET_PKT_ENTRY_STATE** , если нет проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="ff84e-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="ff84e-106">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ff84e-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="ff84e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff84e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff84e-108">*хдевице* [in]</span><span class="sxs-lookup"><span data-stu-id="ff84e-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-109">Маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="ff84e-109">A handle to the device.</span></span> <span data-ttu-id="ff84e-110">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="ff84e-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-111">*двиоконтролкоде* [in]</span><span class="sxs-lookup"><span data-stu-id="ff84e-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-112">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="ff84e-112">The control code for the operation.</span></span> <span data-ttu-id="ff84e-113">Для этой операции используйте **FSCTL_DFS_GET_PKT_ENTRY_STATE** .</span><span class="sxs-lookup"><span data-stu-id="ff84e-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="ff84e-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ff84e-115">Адрес структуры [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) и следующих 1-3 строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="ff84e-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-116">*нинбуфферсизе* [in]</span><span class="sxs-lookup"><span data-stu-id="ff84e-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-117">Размер (в байтах) буфера, на который указывает параметр *лпинбуффер* .</span><span class="sxs-lookup"><span data-stu-id="ff84e-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-118">*лпаутбуффер* [out]</span><span class="sxs-lookup"><span data-stu-id="ff84e-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-119">Адрес структуры **DFS_INFO_ \#** и любых строк и структур, на которые указывает структура **DFS_INFO_ \#** .</span><span class="sxs-lookup"><span data-stu-id="ff84e-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="ff84e-120">Возвращаемая структура зависит от элемента **уровня** в структуре [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) , передаваемой во входном буфере.</span><span class="sxs-lookup"><span data-stu-id="ff84e-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-121">*наутбуфферсизе* [in]</span><span class="sxs-lookup"><span data-stu-id="ff84e-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-122">Размер (в байтах) буфера, на который указывает параметр *лпаутбуффер* .</span><span class="sxs-lookup"><span data-stu-id="ff84e-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="ff84e-123">Из-за строк и структур, на которые ссылается возвращенная **DFS_INFO_ная \#** структура, которые также находятся в выходном буфере, этот буфер должен быть больше, чем указанная структура **DFS_INFO_ \#** .</span><span class="sxs-lookup"><span data-stu-id="ff84e-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-124">*лпбитесретурнед* [out]</span><span class="sxs-lookup"><span data-stu-id="ff84e-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-125">Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="ff84e-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="ff84e-126">Если выходной буфер слишком мал, но, по крайней мере, достаточно большой для хранения **DWORD**, происходит сбой вызова, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ERROR_MORE_DATA**, а первый **DWORD** выходного буфера содержит необходимый размер.</span><span class="sxs-lookup"><span data-stu-id="ff84e-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="ff84e-127">Если выходной буфер не может содержать **DWORD** , вызов завершается с **ERROR_INSUFFICIENT_BUFFER**, а *лпбитесретурнед* — нулем.</span><span class="sxs-lookup"><span data-stu-id="ff84e-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="ff84e-128">Если *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ff84e-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="ff84e-129">Даже если операция не возвращает выходные данные, а *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="ff84e-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="ff84e-130">После такой операции значение *лпбитесретурнед* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="ff84e-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="ff84e-131">Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ff84e-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="ff84e-132">Если этот параметр не равен **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия.</span><span class="sxs-lookup"><span data-stu-id="ff84e-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="ff84e-133">Чтобы получить число возвращаемых байтов, вызовите [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="ff84e-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="ff84e-134">Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных вызовом [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="ff84e-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="ff84e-135">*лповерлаппед* [in]</span><span class="sxs-lookup"><span data-stu-id="ff84e-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="ff84e-136">Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="ff84e-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="ff84e-137">Если *хдевице* был открыт без указания **FILE_FLAG_OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ff84e-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="ff84e-138">Если *хдевице* был открыт с флагом **FILE_FLAG_OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="ff84e-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="ff84e-139">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="ff84e-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="ff84e-140">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="ff84e-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="ff84e-141">Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="ff84e-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="ff84e-142">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="ff84e-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff84e-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff84e-143">Return value</span></span>

<span data-ttu-id="ff84e-144">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ff84e-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="ff84e-145">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ff84e-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="ff84e-146">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ff84e-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff84e-147">Требования</span><span class="sxs-lookup"><span data-stu-id="ff84e-147">Requirements</span></span>

| <span data-ttu-id="ff84e-148">Требование</span><span class="sxs-lookup"><span data-stu-id="ff84e-148">Requirement</span></span> | <span data-ttu-id="ff84e-149">Значение</span><span class="sxs-lookup"><span data-stu-id="ff84e-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff84e-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff84e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ff84e-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff84e-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="ff84e-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff84e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ff84e-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff84e-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="ff84e-154">Header</span><span class="sxs-lookup"><span data-stu-id="ff84e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff84e-155"><dt>Лмдфс. h (включение Лмдфс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff84e-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ff84e-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff84e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff84e-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="ff84e-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="ff84e-158">**нетдфсжетклиентинфо**</span><span class="sxs-lookup"><span data-stu-id="ff84e-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
