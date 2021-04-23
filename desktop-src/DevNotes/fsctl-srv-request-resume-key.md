---
description: '\_ \_ \_ \_ Управляющий код ключа возобновления фсктл SRV-запроса используется для получения ссылки на непрозрачный файл для использования с \_ управляющим кодом ioctl COPYCHUNK.'
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Код элемента управления FSCTL_SRV_REQUEST_RESUME_KEY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895429"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="6f811-103">\_ \_ \_ \_ Код управления ключами возобновления ключа для запроса SRV фсктл</span><span class="sxs-lookup"><span data-stu-id="6f811-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="6f811-104">Управляющий код **\_ \_ \_ \_ ключа возобновления фсктл SRV-запроса** используется для получения ссылки на непрозрачный файл для использования с управляющим кодом [**ioctl \_ COPYCHUNK**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="6f811-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="6f811-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="6f811-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="6f811-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f811-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f811-107">*хдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f811-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-108">Описатель файла, для которого запрашивается ключ исходного файла.</span><span class="sxs-lookup"><span data-stu-id="6f811-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="6f811-109">Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="6f811-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-110">*двиоконтролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f811-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="6f811-111">The control code for the operation.</span></span> <span data-ttu-id="6f811-112">Используйте **\_ \_ \_ \_ ключ возобновления запроса SRV фсктл** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="6f811-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-113">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="6f811-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6f811-114">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6f811-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-115">*нинбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f811-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-116">Не используется в этой операции; присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="6f811-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-117">*лпаутбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f811-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-118">Указатель на выходной буфер, структура **\_ \_ \_ ключа возобновления SRV-запроса** .</span><span class="sxs-lookup"><span data-stu-id="6f811-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="6f811-119">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="6f811-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-120">*наутбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f811-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-121">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="6f811-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-122">*лпбитесретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f811-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-123">Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="6f811-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="6f811-124">Если выходной буфер слишком мал, вызов завершается ошибкой, функция [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ недостаточно \_ буфера**, а *лпбитесретурнед* равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6f811-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="6f811-125">Если параметр *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6f811-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="6f811-126">Даже если операция не возвращает выходные данные и параметр *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="6f811-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="6f811-127">После такой операции значение *лпбитесретурнед* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="6f811-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="6f811-128">Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6f811-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="6f811-129">Если *лповерлаппед* не равно **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия.</span><span class="sxs-lookup"><span data-stu-id="6f811-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="6f811-130">Чтобы получить число возвращаемых байтов, вызовите функцию [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="6f811-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="6f811-131">Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных путем вызова функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="6f811-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="6f811-132">*лповерлаппед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f811-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f811-133">Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="6f811-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="6f811-134">Если параметр *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6f811-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="6f811-135">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="6f811-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="6f811-136">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="6f811-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="6f811-137">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="6f811-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="6f811-138">Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="6f811-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="6f811-139">В противном случае функция не возвращает значение до завершения операции или до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="6f811-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f811-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f811-140">Return value</span></span>

<span data-ttu-id="6f811-141">Если операция завершается успешно, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6f811-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="6f811-142">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="6f811-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="6f811-143">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="6f811-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f811-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f811-144">Remarks</span></span>

<span data-ttu-id="6f811-145">Этот управляющий код не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="6f811-145">This control code has no associated header file.</span></span> <span data-ttu-id="6f811-146">Необходимо определить управляющий код и структуры данных следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6f811-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="6f811-147">Эти члены можно описать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6f811-147">These members can be described as follows.</span></span>



| <span data-ttu-id="6f811-148">Член</span><span class="sxs-lookup"><span data-stu-id="6f811-148">Member</span></span>                                                                                                                       | <span data-ttu-id="6f811-149">Описание</span><span class="sxs-lookup"><span data-stu-id="6f811-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f811-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ресумекэй**</span><span class="sxs-lookup"><span data-stu-id="6f811-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="6f811-151">Непрозрачное значение, идентифицирующее исходный файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="6f811-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="6f811-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="6f811-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="6f811-153">Непрозрачное значение, определяющее время открытия файла.</span><span class="sxs-lookup"><span data-stu-id="6f811-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="6f811-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**PID**</span><span class="sxs-lookup"><span data-stu-id="6f811-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="6f811-155">Непрозрачное значение, идентифицирующее процесс, открывший файл.</span><span class="sxs-lookup"><span data-stu-id="6f811-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="6f811-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Раздел**</span><span class="sxs-lookup"><span data-stu-id="6f811-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="6f811-157">Структура **\_ \_ ключа возобновления SRV** .</span><span class="sxs-lookup"><span data-stu-id="6f811-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="6f811-158">Для выполнения операции копирования на стороне сервера используйте эту структуру с управляющим кодом [**ioctl \_ COPYCHUNK**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="6f811-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="6f811-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**контекстленгс**</span><span class="sxs-lookup"><span data-stu-id="6f811-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="6f811-160">Этот член зарезервирован для системного использования; не используйте.</span><span class="sxs-lookup"><span data-stu-id="6f811-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="6f811-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Локального**</span><span class="sxs-lookup"><span data-stu-id="6f811-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="6f811-162">Этот член зарезервирован для системного использования; не используйте.</span><span class="sxs-lookup"><span data-stu-id="6f811-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="6f811-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f811-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f811-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="6f811-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="6f811-165">**\_COPYCHUNK ioctl**</span><span class="sxs-lookup"><span data-stu-id="6f811-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
