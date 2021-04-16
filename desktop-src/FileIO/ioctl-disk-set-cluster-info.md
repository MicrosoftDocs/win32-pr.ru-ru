---
description: Задает сведения о кластере на диске.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: Код элемента управления IOCTL_DISK_SET_CLUSTER_INFO (Нтдддиск. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664426"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a><span data-ttu-id="11ea8-103">\_ \_ \_ \_ Управляющий код для сведений о кластере для набора дисков ioctl</span><span class="sxs-lookup"><span data-stu-id="11ea8-103">IOCTL\_DISK\_SET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="11ea8-104">Задает сведения о кластере на диске.</span><span class="sxs-lookup"><span data-stu-id="11ea8-104">Sets the cluster information on a disk.</span></span>

<span data-ttu-id="11ea8-105">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="11ea8-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="11ea8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11ea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ea8-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="11ea8-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-108">Маркер диска.</span><span class="sxs-lookup"><span data-stu-id="11ea8-108">A handle to the disk.</span></span>

<span data-ttu-id="11ea8-109">Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="11ea8-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-110">*двиоконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="11ea8-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="11ea8-111">The control code for the operation.</span></span>

<span data-ttu-id="11ea8-112">Используйте **ioctl \_ дискового \_ задания \_ \_ сведения о кластере** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="11ea8-112">Use **IOCTL\_DISK\_SET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-113">*лпинбуффер*</span><span class="sxs-lookup"><span data-stu-id="11ea8-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-114">Указатель на структуру данных [**\_ \_ о кластере дисков**](disk-cluster-info.md) , содержащую сведения о кластере для диска.</span><span class="sxs-lookup"><span data-stu-id="11ea8-114">A pointer to a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure that contains cluster information for the disk.</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-115">*нинбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="11ea8-115">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-116">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="11ea8-116">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-117">*лпаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="11ea8-117">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-118">Не используется с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="11ea8-118">Not used with this operation.</span></span> <span data-ttu-id="11ea8-119">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="11ea8-119">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-120">*наутбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="11ea8-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-121">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="11ea8-121">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="11ea8-122">Задайте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="11ea8-122">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-123">*лпбитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="11ea8-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-124">Не используется с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="11ea8-124">Not used with this operation.</span></span> <span data-ttu-id="11ea8-125">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="11ea8-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11ea8-126">*лповерлаппед*</span><span class="sxs-lookup"><span data-stu-id="11ea8-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="11ea8-127">Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="11ea8-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="11ea8-128">Если *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="11ea8-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="11ea8-129">Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="11ea8-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="11ea8-130">В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события.</span><span class="sxs-lookup"><span data-stu-id="11ea8-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="11ea8-131">В противном случае функция завершается ошибкой непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="11ea8-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="11ea8-132">Для операций с перекрытием [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="11ea8-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="11ea8-133">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="11ea8-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ea8-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11ea8-134">Return value</span></span>

<span data-ttu-id="11ea8-135">Если операция завершается успешно, указывая на то, что все тома на диске готовы к использованию, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="11ea8-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="11ea8-136">Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="11ea8-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="11ea8-137">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="11ea8-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="11ea8-138">Требования</span><span class="sxs-lookup"><span data-stu-id="11ea8-138">Requirements</span></span>



| <span data-ttu-id="11ea8-139">Требование</span><span class="sxs-lookup"><span data-stu-id="11ea8-139">Requirement</span></span> | <span data-ttu-id="11ea8-140">Значение</span><span class="sxs-lookup"><span data-stu-id="11ea8-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11ea8-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11ea8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="11ea8-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="11ea8-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="11ea8-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11ea8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="11ea8-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="11ea8-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11ea8-145">Header</span><span class="sxs-lookup"><span data-stu-id="11ea8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="11ea8-146"><dt>Нтдддиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="11ea8-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ea8-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11ea8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ea8-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="11ea8-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="11ea8-149">Управляющие коды управления дисками</span><span class="sxs-lookup"><span data-stu-id="11ea8-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="11ea8-150">**\_сведения о кластере диска \_**</span><span class="sxs-lookup"><span data-stu-id="11ea8-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="11ea8-151">**IOCTL \_ Disk \_ Получение \_ \_ сведений о кластере**</span><span class="sxs-lookup"><span data-stu-id="11ea8-151">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

