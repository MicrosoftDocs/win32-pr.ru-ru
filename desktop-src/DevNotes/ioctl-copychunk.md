---
description: '\_Управляющий код COPYCHUNK ioctl инициирует копию диапазона данных на стороне сервера, называемую также фрагментом.'
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Код элемента управления IOCTL_COPYCHUNK
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662067"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="64676-103">\_Управляющий код COPYCHUNK ioctl</span><span class="sxs-lookup"><span data-stu-id="64676-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="64676-104">Управляющий код **\_ COPYCHUNK ioctl** инициирует копию диапазона данных на стороне сервера, называемую также фрагментом.</span><span class="sxs-lookup"><span data-stu-id="64676-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="64676-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="64676-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="64676-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64676-107">*хдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64676-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-108">Описатель файла, который является целевым объектом операции копирования на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="64676-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="64676-109">Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="64676-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="64676-110">*двиоконтролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64676-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="64676-111">The control code for the operation.</span></span> <span data-ttu-id="64676-112">Для этой операции используйте **ioctl \_ COPYCHUNK** .</span><span class="sxs-lookup"><span data-stu-id="64676-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="64676-113">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="64676-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="64676-114">Указатель на входной буфер — структуру **копирования SRV- \_ COPYCHUNK \_** .</span><span class="sxs-lookup"><span data-stu-id="64676-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="64676-115">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="64676-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="64676-116">*нинбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64676-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="64676-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="64676-118">*лпаутбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="64676-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-119">Указатель на выходной буфер, структура **\_ \_ ответа SRV COPYCHUNK** .</span><span class="sxs-lookup"><span data-stu-id="64676-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="64676-120">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="64676-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="64676-121">*наутбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64676-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-122">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="64676-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="64676-123">*лпбитесретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="64676-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-124">Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="64676-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="64676-125">Если выходной буфер слишком мал, вызов завершается ошибкой, функция [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ недостаточно \_ буфера**, а *лпбитесретурнед* равно нулю.</span><span class="sxs-lookup"><span data-stu-id="64676-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="64676-126">Если параметр *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="64676-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="64676-127">Даже если операция не возвращает выходные данные и параметр *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="64676-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="64676-128">После такой операции значение *лпбитесретурнед* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="64676-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="64676-129">Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="64676-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="64676-130">Если *лповерлаппед* не равно **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия.</span><span class="sxs-lookup"><span data-stu-id="64676-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="64676-131">Чтобы получить число возвращаемых байтов, вызовите функцию [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="64676-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="64676-132">Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных путем вызова функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="64676-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="64676-133">*лповерлаппед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64676-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64676-134">Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="64676-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="64676-135">Если параметр *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="64676-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="64676-136">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="64676-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="64676-137">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="64676-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="64676-138">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="64676-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="64676-139">Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="64676-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="64676-140">В противном случае функция не возвращает значение до завершения операции или до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="64676-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64676-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64676-141">Return value</span></span>

<span data-ttu-id="64676-142">Если операция завершается успешно, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="64676-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="64676-143">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="64676-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="64676-144">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="64676-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="64676-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64676-145">Remarks</span></span>

<span data-ttu-id="64676-146">Этот управляющий код не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="64676-146">This control code has no associated header file.</span></span> <span data-ttu-id="64676-147">Необходимо определить управляющий код и структуры данных следующим образом.</span><span class="sxs-lookup"><span data-stu-id="64676-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="64676-148">Эти члены можно описать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="64676-148">These members can be described as follows.</span></span>



| <span data-ttu-id="64676-149">Член</span><span class="sxs-lookup"><span data-stu-id="64676-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="64676-150">Описание</span><span class="sxs-lookup"><span data-stu-id="64676-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64676-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**саурцеоффсет**</span><span class="sxs-lookup"><span data-stu-id="64676-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="64676-152">Смещение в байтах от начала исходного файла до копируемого фрагмента.</span><span class="sxs-lookup"><span data-stu-id="64676-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="64676-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**дестинатионоффсет**</span><span class="sxs-lookup"><span data-stu-id="64676-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="64676-154">Смещение (в байтах) от начала целевого файла до места копирования фрагмента.</span><span class="sxs-lookup"><span data-stu-id="64676-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="64676-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Недопустим**</span><span class="sxs-lookup"><span data-stu-id="64676-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="64676-156">Число байтов данных в копируемом фрагменте.</span><span class="sxs-lookup"><span data-stu-id="64676-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="64676-157">Должно быть больше нуля и меньше или равно 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="64676-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="64676-158">**Длина** \* **Чунккаунт** должно быть меньше или равно 16 МБ.</span><span class="sxs-lookup"><span data-stu-id="64676-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="64676-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="64676-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="64676-160">Ключ, представляющий исходный файл с копируемыми данными.</span><span class="sxs-lookup"><span data-stu-id="64676-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="64676-161">Этот ключ получен с помощью [**\_ \_ \_ \_ ключа возобновления запроса фсктл SRV**](fsctl-srv-request-resume-key.md).</span><span class="sxs-lookup"><span data-stu-id="64676-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="64676-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**чунккаунт**</span><span class="sxs-lookup"><span data-stu-id="64676-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="64676-163">Число копируемых фрагментов.</span><span class="sxs-lookup"><span data-stu-id="64676-163">The number of chunks to be copied.</span></span> <span data-ttu-id="64676-164">Должно быть больше нуля и меньше или равно 256.</span><span class="sxs-lookup"><span data-stu-id="64676-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="64676-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Процессу**</span><span class="sxs-lookup"><span data-stu-id="64676-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="64676-166">Этот член зарезервирован для системного использования; не используйте.</span><span class="sxs-lookup"><span data-stu-id="64676-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="64676-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Фрагмент**</span><span class="sxs-lookup"><span data-stu-id="64676-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="64676-168">Массив структур COPYCHUNK **чунккаунт** **SRV \_** , по одному для каждого копируемого фрагмента.</span><span class="sxs-lookup"><span data-stu-id="64676-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="64676-169">Длина этого массива в байтах должна быть **чунккаунт** \* sizeof (**SRV \_ COPYCHUNK**).</span><span class="sxs-lookup"><span data-stu-id="64676-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="64676-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**чунксвриттен**</span><span class="sxs-lookup"><span data-stu-id="64676-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="64676-171">Если операция завершилась ошибкой **с \_ недопустимым \_ параметром**, это значение указывает максимальное количество фрагментов, которые сервер будет принимать в одном запросе, то есть 256.</span><span class="sxs-lookup"><span data-stu-id="64676-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="64676-172">В противном случае это значение указывает количество успешно записанных блоков.</span><span class="sxs-lookup"><span data-stu-id="64676-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="64676-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**чункбитесвриттен**</span><span class="sxs-lookup"><span data-stu-id="64676-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="64676-174">Если операция завершилась ошибкой **с \_ недопустимым \_ параметром**, это значение указывает максимальное число байтов, которое сервер будет разрешать записывать в один блок, который равен 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="64676-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="64676-175">В противном случае это значение указывает число байтов, успешно записанных в последний фрагмент, который не был успешно обработан (если произошла частичная запись).</span><span class="sxs-lookup"><span data-stu-id="64676-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="64676-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**тоталбитесвриттен**</span><span class="sxs-lookup"><span data-stu-id="64676-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="64676-177">Если операция завершилась ошибкой **с \_ недопустимым \_ параметром**, это значение указывает максимальное число байтов, которое будет скопировано сервером в одном запросе, что составляет 16 МБ.</span><span class="sxs-lookup"><span data-stu-id="64676-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="64676-178">В противном случае это значение указывает число успешно записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="64676-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="64676-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64676-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64676-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="64676-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="64676-181">**\_ \_ \_ ключ возобновления запроса SRV фсктл \_**</span><span class="sxs-lookup"><span data-stu-id="64676-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
