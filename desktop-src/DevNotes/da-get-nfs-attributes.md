---
description: '\_ \_ \_ Код управления атрибутами Da Get NFS запрашивает дополнительные сведения о ресурсе NFS.'
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Код элемента управления DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538681"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="c45dd-103">\_ \_ \_ Код элемента управления для получения атрибутов NFS</span><span class="sxs-lookup"><span data-stu-id="c45dd-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="c45dd-104">Код **управления \_ \_ \_ атрибутами Da Get NFS** запрашивает дополнительные сведения о ресурсе NFS.</span><span class="sxs-lookup"><span data-stu-id="c45dd-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="c45dd-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c45dd-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="c45dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c45dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45dd-107">*хдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-108">Маркер файла в общей папке NFS.</span><span class="sxs-lookup"><span data-stu-id="c45dd-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="c45dd-109">Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="c45dd-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-110">*двиоконтролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="c45dd-111">The control code for the operation.</span></span> <span data-ttu-id="c45dd-112">Для этой операции используйте **\_ \_ \_ атрибут Da Get NFS** .</span><span class="sxs-lookup"><span data-stu-id="c45dd-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-113">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="c45dd-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c45dd-114">Не используется в этой операции; Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c45dd-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-115">*нинбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-116">Не используется в этой операции; присвойте ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="c45dd-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-117">*лпаутбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-118">Указатель на выходной буфер, который содержит структуру **\_ \_ атрибутов файла NFS** .</span><span class="sxs-lookup"><span data-stu-id="c45dd-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="c45dd-119">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="c45dd-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-120">*наутбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-121">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="c45dd-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-122">*лпбитесретурнед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-123">Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.</span><span class="sxs-lookup"><span data-stu-id="c45dd-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="c45dd-124">Если выходной буфер слишком мал, вызов завершается ошибкой, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ недостаточно \_ буфера**, а *лпбитесретурнед* — ноль.</span><span class="sxs-lookup"><span data-stu-id="c45dd-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="c45dd-125">Если *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c45dd-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="c45dd-126">Даже если операция не возвращает выходные данные, а *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*.</span><span class="sxs-lookup"><span data-stu-id="c45dd-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="c45dd-127">После такой операции значение *лпбитесретурнед* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="c45dd-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="c45dd-128">Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c45dd-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="c45dd-129">Если этот параметр не равен **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия.</span><span class="sxs-lookup"><span data-stu-id="c45dd-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="c45dd-130">Чтобы получить число возвращаемых байтов, вызовите [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="c45dd-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="c45dd-131">Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных вызовом [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="c45dd-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-132">*лповерлаппед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c45dd-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-133">Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="c45dd-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="c45dd-134">Если *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c45dd-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="c45dd-135">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="c45dd-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="c45dd-136">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="c45dd-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="c45dd-137">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="c45dd-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="c45dd-138">Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="c45dd-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="c45dd-139">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c45dd-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45dd-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c45dd-140">Return value</span></span>

<span data-ttu-id="c45dd-141">Если операция завершается успешно, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c45dd-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="c45dd-142">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c45dd-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="c45dd-143">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c45dd-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c45dd-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c45dd-144">Remarks</span></span>

<span data-ttu-id="c45dd-145">Этот управляющий код не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="c45dd-145">This control code has no associated header file.</span></span> <span data-ttu-id="c45dd-146">Необходимо определить управляющий код и структуры данных следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c45dd-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="c45dd-147">Члены структуры можно описать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c45dd-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="c45dd-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="c45dd-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-149">Непрозрачное значение, используемое для специальных типов файлов, таких как файлы специального блока, специального символьного типа и FIFO.</span><span class="sxs-lookup"><span data-stu-id="c45dd-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="c45dd-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-151">Непрозрачное значение, используемое для специальных типов файлов, таких как файлы специального блока, специального символьного типа и FIFO.</span><span class="sxs-lookup"><span data-stu-id="c45dd-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Несколько**</span><span class="sxs-lookup"><span data-stu-id="c45dd-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-153">64-разрядное значение, представляющее секунды с 1 января 1970 (UTC).</span><span class="sxs-lookup"><span data-stu-id="c45dd-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**нсекондс**</span><span class="sxs-lookup"><span data-stu-id="c45dd-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-155">Число наносекунд, добавляемых к элементу **секунд** .</span><span class="sxs-lookup"><span data-stu-id="c45dd-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span><span class="sxs-lookup"><span data-stu-id="c45dd-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-157">Тип файла NFS для общей папки.</span><span class="sxs-lookup"><span data-stu-id="c45dd-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="c45dd-158">Тип файла NFS</span><span class="sxs-lookup"><span data-stu-id="c45dd-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="c45dd-159">Описание</span><span class="sxs-lookup"><span data-stu-id="c45dd-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="c45dd-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>\_тип NFS \_ reg</span><span class="sxs-lookup"><span data-stu-id="c45dd-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="c45dd-161">Обычный файл.</span><span class="sxs-lookup"><span data-stu-id="c45dd-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="c45dd-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>\_dir тип \_ NFS</span><span class="sxs-lookup"><span data-stu-id="c45dd-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="c45dd-163">Каталог.</span><span class="sxs-lookup"><span data-stu-id="c45dd-163">A directory.</span></span><br/>              |
| <span data-ttu-id="c45dd-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_тип NFS \_ BLK</span><span class="sxs-lookup"><span data-stu-id="c45dd-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="c45dd-165">Специальный блочный файл.</span><span class="sxs-lookup"><span data-stu-id="c45dd-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="c45dd-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>\_тип NFS типа \_ Chr</span><span class="sxs-lookup"><span data-stu-id="c45dd-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="c45dd-167">Специальный символьный файл.</span><span class="sxs-lookup"><span data-stu-id="c45dd-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="c45dd-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>\_тип NFS \_ LNK</span><span class="sxs-lookup"><span data-stu-id="c45dd-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="c45dd-169">Символьная ссылка.</span><span class="sxs-lookup"><span data-stu-id="c45dd-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="c45dd-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>\_тип NFS \_ Сокк</span><span class="sxs-lookup"><span data-stu-id="c45dd-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="c45dd-171">Сокет Windows.</span><span class="sxs-lookup"><span data-stu-id="c45dd-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="c45dd-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>\_тип NFS \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="c45dd-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="c45dd-173">Файл FIFO.</span><span class="sxs-lookup"><span data-stu-id="c45dd-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="c45dd-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Режима**</span><span class="sxs-lookup"><span data-stu-id="c45dd-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-175">Режим файла.</span><span class="sxs-lookup"><span data-stu-id="c45dd-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**нлинк**</span><span class="sxs-lookup"><span data-stu-id="c45dd-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-177">Число ссылок на общую папку.</span><span class="sxs-lookup"><span data-stu-id="c45dd-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Такой**</span><span class="sxs-lookup"><span data-stu-id="c45dd-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-179">Идентификатор пользователя UNIX (UID).</span><span class="sxs-lookup"><span data-stu-id="c45dd-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Операционной**</span><span class="sxs-lookup"><span data-stu-id="c45dd-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-181">Идентификатор группы UNIX (GID).</span><span class="sxs-lookup"><span data-stu-id="c45dd-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Изменять**</span><span class="sxs-lookup"><span data-stu-id="c45dd-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-183">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="c45dd-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Используется**</span><span class="sxs-lookup"><span data-stu-id="c45dd-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-185">Используемый размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="c45dd-185">The file size used, in bytes.</span></span> <span data-ttu-id="c45dd-186">Это то же самое, что и размер файла.</span><span class="sxs-lookup"><span data-stu-id="c45dd-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**рдев**</span><span class="sxs-lookup"><span data-stu-id="c45dd-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-188">Идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="c45dd-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**фсид**</span><span class="sxs-lookup"><span data-stu-id="c45dd-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-190">Идентификатор файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c45dd-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**ИД**</span><span class="sxs-lookup"><span data-stu-id="c45dd-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-192">Идентификатор файла.</span><span class="sxs-lookup"><span data-stu-id="c45dd-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**акцесстиме**</span><span class="sxs-lookup"><span data-stu-id="c45dd-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-194">Время последнего доступа.</span><span class="sxs-lookup"><span data-stu-id="c45dd-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**модифитиме**</span><span class="sxs-lookup"><span data-stu-id="c45dd-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-196">Время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="c45dd-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**чанжетиме**</span><span class="sxs-lookup"><span data-stu-id="c45dd-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-198">Время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="c45dd-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="c45dd-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="c45dd-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-200">Структура **\_ \_ атрибутов файла NFS** .</span><span class="sxs-lookup"><span data-stu-id="c45dd-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="c45dd-201">Более подробное описание членов этой структуры см. в описании структуры **fattr3** в спецификации протокола NFS версии 3 (как определено в [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span><span class="sxs-lookup"><span data-stu-id="c45dd-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="c45dd-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Версия**</span><span class="sxs-lookup"><span data-stu-id="c45dd-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="c45dd-203">Указывает, является ли подключение, для которого был создан маркер, для общего ресурса NFS по протоколу NFS версии 2 или NFS версии 3.</span><span class="sxs-lookup"><span data-stu-id="c45dd-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="c45dd-204">Значение</span><span class="sxs-lookup"><span data-stu-id="c45dd-204">Value</span></span>                            | <span data-ttu-id="c45dd-205">Описание</span><span class="sxs-lookup"><span data-stu-id="c45dd-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="c45dd-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="c45dd-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="c45dd-207">NFS версии 2</span><span class="sxs-lookup"><span data-stu-id="c45dd-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="c45dd-208"><span id="3"></span>3-5</span><span class="sxs-lookup"><span data-stu-id="c45dd-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="c45dd-209">NFS версии 3</span><span class="sxs-lookup"><span data-stu-id="c45dd-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c45dd-210">Требования</span><span class="sxs-lookup"><span data-stu-id="c45dd-210">Requirements</span></span>



| <span data-ttu-id="c45dd-211">Требование</span><span class="sxs-lookup"><span data-stu-id="c45dd-211">Requirement</span></span> | <span data-ttu-id="c45dd-212">Значение</span><span class="sxs-lookup"><span data-stu-id="c45dd-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="c45dd-213">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c45dd-213">Minimum supported client</span></span><br/> | <span data-ttu-id="c45dd-214">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c45dd-214">None supported</span></span><br/>         |
| <span data-ttu-id="c45dd-215">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c45dd-215">Minimum supported server</span></span><br/> | <span data-ttu-id="c45dd-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c45dd-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="c45dd-217">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c45dd-217">End of client support</span></span><br/>    | <span data-ttu-id="c45dd-218">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c45dd-218">None supported</span></span><br/>         |
| <span data-ttu-id="c45dd-219">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c45dd-219">End of server support</span></span><br/>    | <span data-ttu-id="c45dd-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c45dd-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c45dd-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c45dd-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45dd-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="c45dd-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
