---
description: Отменяет все ожидающие операции ввода и вывода (I/O), выданные вызывающим потоком для указанного файла.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Функция Канцелио (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662872"
---
# <a name="cancelio-function"></a><span data-ttu-id="9fa36-103">Функция Канцелио</span><span class="sxs-lookup"><span data-stu-id="9fa36-103">CancelIo function</span></span>

<span data-ttu-id="9fa36-104">Отменяет все ожидающие операции ввода и вывода (I/O), выданные вызывающим потоком для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="9fa36-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="9fa36-105">Функция не отменяет операции ввода-вывода, которые другие потоки выдают для маркера файла.</span><span class="sxs-lookup"><span data-stu-id="9fa36-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="9fa36-106">Чтобы отменить операции ввода-вывода из другого потока, используйте функцию [**канцелиоекс**](cancelioex-func.md) .</span><span class="sxs-lookup"><span data-stu-id="9fa36-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa36-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fa36-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="9fa36-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fa36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa36-109">*hFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fa36-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa36-110">Маркер файла.</span><span class="sxs-lookup"><span data-stu-id="9fa36-110">A handle to the file.</span></span>

<span data-ttu-id="9fa36-111">Функция отменяет все ожидающие операции ввода-вывода для этого обработчика файлов.</span><span class="sxs-lookup"><span data-stu-id="9fa36-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa36-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fa36-112">Return value</span></span>

<span data-ttu-id="9fa36-113">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9fa36-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="9fa36-114">Успешно запрошена операция отмены для всех ожидающих операций ввода-вывода, выданных вызывающим потоком для указанного маркера файла.</span><span class="sxs-lookup"><span data-stu-id="9fa36-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="9fa36-115">Поток может использовать функцию [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) , чтобы определить, когда завершаются операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9fa36-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="9fa36-116">Если функция завершается ошибкой, возвращаемое значение равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="9fa36-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="9fa36-117">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="9fa36-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa36-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fa36-118">Remarks</span></span>

<span data-ttu-id="9fa36-119">Если для указанного маркера файла выполняются ожидающие выполнения операции ввода-вывода и они выдаются вызывающим потоком, функция **канцелио** отменяет их.</span><span class="sxs-lookup"><span data-stu-id="9fa36-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="9fa36-120">**Канцелио** отменяет только что необработанные операции ввода-вывода для маркера, он не изменяет состояние маркера. Это означает, что вы не можете полагаться на состояние маркера, так как вы не можете определить, завершилась ли операция успешно или отменена.</span><span class="sxs-lookup"><span data-stu-id="9fa36-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="9fa36-121">Операции ввода-вывода должны выдаваться как перекрывающиеся операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9fa36-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="9fa36-122">Если это не так, операции ввода-вывода не возвращают, чтобы разрешить потоку вызывать функцию **канцелио** .</span><span class="sxs-lookup"><span data-stu-id="9fa36-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="9fa36-123">Вызов функции **канцелио** с маркером файла, который не открыт с **\_ \_ перекрытием флага файла** , не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="9fa36-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="9fa36-124">Все операции ввода-вывода, отмененные с ошибкой, **\_ \_ прерываются**, и все уведомления о завершении операций ввода-вывода выполняются обычным образом.</span><span class="sxs-lookup"><span data-stu-id="9fa36-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="9fa36-125">В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.</span><span class="sxs-lookup"><span data-stu-id="9fa36-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="9fa36-126">Технология</span><span class="sxs-lookup"><span data-stu-id="9fa36-126">Technology</span></span>                                           | <span data-ttu-id="9fa36-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9fa36-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="9fa36-128">Протокол SMB 3,0</span><span class="sxs-lookup"><span data-stu-id="9fa36-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="9fa36-129">Да</span><span class="sxs-lookup"><span data-stu-id="9fa36-129">Yes</span></span><br/> |
| <span data-ttu-id="9fa36-130">Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)</span><span class="sxs-lookup"><span data-stu-id="9fa36-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="9fa36-131">Да</span><span class="sxs-lookup"><span data-stu-id="9fa36-131">Yes</span></span><br/> |
| <span data-ttu-id="9fa36-132">SMB 3,0 с масштабируемыми файловыми ресурсами (SO)</span><span class="sxs-lookup"><span data-stu-id="9fa36-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="9fa36-133">Да</span><span class="sxs-lookup"><span data-stu-id="9fa36-133">Yes</span></span><br/> |
| <span data-ttu-id="9fa36-134">Общий том кластераная файловая система (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="9fa36-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="9fa36-135">Да</span><span class="sxs-lookup"><span data-stu-id="9fa36-135">Yes</span></span><br/> |
| <span data-ttu-id="9fa36-136">Восстанавливаемая файловая система (ReFS)</span><span class="sxs-lookup"><span data-stu-id="9fa36-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="9fa36-137">Да</span><span class="sxs-lookup"><span data-stu-id="9fa36-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9fa36-138">Требования</span><span class="sxs-lookup"><span data-stu-id="9fa36-138">Requirements</span></span>



| <span data-ttu-id="9fa36-139">Требование</span><span class="sxs-lookup"><span data-stu-id="9fa36-139">Requirement</span></span> | <span data-ttu-id="9fa36-140">Значение</span><span class="sxs-lookup"><span data-stu-id="9fa36-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa36-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fa36-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa36-142">\[Приложения UWP для классических приложений Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="9fa36-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9fa36-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fa36-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa36-144">\[Приложения UWP для классических приложений Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="9fa36-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9fa36-145">Header</span><span class="sxs-lookup"><span data-stu-id="9fa36-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fa36-146"><dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fa36-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9fa36-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9fa36-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fa36-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fa36-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="9fa36-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9fa36-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fa36-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fa36-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="9fa36-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fa36-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa36-152">**канцелиоекс**</span><span class="sxs-lookup"><span data-stu-id="9fa36-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="9fa36-153">**канцелсинчронаусио**</span><span class="sxs-lookup"><span data-stu-id="9fa36-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="9fa36-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="9fa36-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="9fa36-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="9fa36-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="9fa36-156">Функции управления файлами</span><span class="sxs-lookup"><span data-stu-id="9fa36-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="9fa36-157">**локкфиликс**</span><span class="sxs-lookup"><span data-stu-id="9fa36-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="9fa36-158">**реаддиректоричанжесв**</span><span class="sxs-lookup"><span data-stu-id="9fa36-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="9fa36-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="9fa36-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="9fa36-160">**реадфиликс**</span><span class="sxs-lookup"><span data-stu-id="9fa36-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="9fa36-161">Синхронный и асинхронный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="9fa36-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="9fa36-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="9fa36-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="9fa36-163">**вритефиликс**</span><span class="sxs-lookup"><span data-stu-id="9fa36-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

