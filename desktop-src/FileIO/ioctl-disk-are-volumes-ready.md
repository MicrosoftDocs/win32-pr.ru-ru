---
description: Ожидает, пока все тома на указанном диске будут готовы к использованию.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: Код элемента управления IOCTL_DISK_ARE_VOLUMES_READY (Нтдддиск. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684366"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="f59af-103">\_Диск ioctl \_ — \_ это \_ готовые к использованию тома контрольные коды</span><span class="sxs-lookup"><span data-stu-id="f59af-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="f59af-104">Ожидает, пока все тома на указанном диске будут готовы к использованию.</span><span class="sxs-lookup"><span data-stu-id="f59af-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="f59af-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="f59af-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="f59af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f59af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f59af-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="f59af-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-108">Маркер диска.</span><span class="sxs-lookup"><span data-stu-id="f59af-108">A handle to the disk.</span></span>

<span data-ttu-id="f59af-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="f59af-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="f59af-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="f59af-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="f59af-111">The control code for the operation.</span></span>

<span data-ttu-id="f59af-112">Использование **\_ диска ioctl \_ — это \_ тома, \_ Готовые** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="f59af-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f59af-113">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="f59af-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-114">Не используется с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f59af-114">Not used with this operation.</span></span> <span data-ttu-id="f59af-115">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f59af-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f59af-116">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="f59af-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="f59af-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="f59af-118">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f59af-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="f59af-119">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="f59af-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-120">Не используется с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f59af-120">Not used with this operation.</span></span> <span data-ttu-id="f59af-121">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f59af-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f59af-122">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="f59af-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-123">Не используется с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f59af-123">Not used with this operation.</span></span> <span data-ttu-id="f59af-124">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f59af-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="f59af-125">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="f59af-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-126">Не используется с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="f59af-126">Not used with this operation.</span></span> <span data-ttu-id="f59af-127">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f59af-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f59af-128">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="f59af-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="f59af-129">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="f59af-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="f59af-130">Если *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f59af-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="f59af-131">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="f59af-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="f59af-132">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="f59af-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="f59af-133">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="f59af-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="f59af-134">Для операций с перекрытием [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="f59af-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="f59af-135">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="f59af-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f59af-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f59af-136">Return value</span></span>

<span data-ttu-id="f59af-137">Если операция завершается успешно, указывая на то, что все тома на диске готовы к использованию, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f59af-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="f59af-138">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f59af-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="f59af-139">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="f59af-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="f59af-140">Требования</span><span class="sxs-lookup"><span data-stu-id="f59af-140">Requirements</span></span>



| <span data-ttu-id="f59af-141">Требование</span><span class="sxs-lookup"><span data-stu-id="f59af-141">Requirement</span></span> | <span data-ttu-id="f59af-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f59af-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f59af-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f59af-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f59af-144">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f59af-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f59af-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f59af-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f59af-146">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f59af-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f59af-147">Header</span><span class="sxs-lookup"><span data-stu-id="f59af-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f59af-148"><dt>Нтдддиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="f59af-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59af-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f59af-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59af-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="f59af-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="f59af-151">Управляющие коды управления дисками</span><span class="sxs-lookup"><span data-stu-id="f59af-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

