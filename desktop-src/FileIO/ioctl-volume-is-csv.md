---
description: Определяет, является ли том томом CSV.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: Код элемента управления IOCTL_VOLUME_IS_CSV (Нтддвол. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348542"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="3451b-103">\_Том ioctl \_ — это \_ управляющий код CSV</span><span class="sxs-lookup"><span data-stu-id="3451b-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="3451b-104">Определяет, является ли том томом CSV.</span><span class="sxs-lookup"><span data-stu-id="3451b-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="3451b-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3451b-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="3451b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3451b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3451b-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="3451b-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-108">Маркер для тома.</span><span class="sxs-lookup"><span data-stu-id="3451b-108">A handle to the volume.</span></span> <span data-ttu-id="3451b-109">Чтобы получить маркер тома, вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="3451b-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="3451b-110">Только администраторы могут открывать дескрипторы томов.</span><span class="sxs-lookup"><span data-stu-id="3451b-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="3451b-111">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="3451b-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-112">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="3451b-112">The control code for the operation.</span></span> <span data-ttu-id="3451b-113">Для этой операции используется **параметр "том ioctl" \_ \_ — \_ CSV** .</span><span class="sxs-lookup"><span data-stu-id="3451b-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3451b-114">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="3451b-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-115">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3451b-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3451b-116">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="3451b-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-117">Не используется в этой операции; установите нулевое значение (0).</span><span class="sxs-lookup"><span data-stu-id="3451b-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="3451b-118">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="3451b-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-119">Указатель на **значение true** , если том является томом CSV; в противном случае вызов функции завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3451b-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="3451b-120">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="3451b-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-121">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="3451b-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3451b-122">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="3451b-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-123">Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="3451b-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="3451b-124">Если *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3451b-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="3451b-125">Даже если операция не возвращает выходные данные, а *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="3451b-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="3451b-126">После такой операции значение *лпбитесретурнед* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="3451b-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="3451b-127">Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3451b-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="3451b-128">Если этот параметр не равен **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия.</span><span class="sxs-lookup"><span data-stu-id="3451b-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="3451b-129">Чтобы получить число возвращаемых байтов, вызовите [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="3451b-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="3451b-130">Если *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных вызовом [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="3451b-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="3451b-131">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="3451b-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="3451b-132">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="3451b-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="3451b-133">Если *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3451b-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="3451b-134">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="3451b-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="3451b-135">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="3451b-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="3451b-136">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="3451b-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="3451b-137">Для операций с перекрытием [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="3451b-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="3451b-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3451b-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3451b-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3451b-139">Return value</span></span>

<span data-ttu-id="3451b-140">Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3451b-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="3451b-141">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="3451b-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="3451b-142">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3451b-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="3451b-143">Требования</span><span class="sxs-lookup"><span data-stu-id="3451b-143">Requirements</span></span>



| <span data-ttu-id="3451b-144">Требование</span><span class="sxs-lookup"><span data-stu-id="3451b-144">Requirement</span></span> | <span data-ttu-id="3451b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="3451b-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3451b-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3451b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3451b-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3451b-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="3451b-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3451b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3451b-149">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3451b-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3451b-150">Header</span><span class="sxs-lookup"><span data-stu-id="3451b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3451b-151"><dt>Нтддвол. h</dt></span><span class="sxs-lookup"><span data-stu-id="3451b-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3451b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3451b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3451b-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="3451b-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="3451b-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="3451b-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="3451b-155">Управляющие коды для управления томами</span><span class="sxs-lookup"><span data-stu-id="3451b-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

