---
description: Помечает все необработанные операции ввода-вывода для указанного маркера файла. Функция отменяет только операции ввода-вывода в текущем процессе, независимо от того, какой поток создал операцию ввода-вывода.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Функция Канцелиоекс (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683311"
---
# <a name="cancelioex-function"></a><span data-ttu-id="f1806-104">Функция Канцелиоекс</span><span class="sxs-lookup"><span data-stu-id="f1806-104">CancelIoEx function</span></span>

<span data-ttu-id="f1806-105">Помечает все необработанные операции ввода-вывода для указанного маркера файла.</span><span class="sxs-lookup"><span data-stu-id="f1806-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="f1806-106">Функция отменяет только операции ввода-вывода в текущем процессе, независимо от того, какой поток создал операцию ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f1806-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1806-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1806-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="f1806-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1806-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1806-109">*hFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1806-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1806-110">Маркер файла.</span><span class="sxs-lookup"><span data-stu-id="f1806-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="f1806-111">*лповерлаппед* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f1806-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1806-112">Указатель на структуру данных с [**ПЕРЕкрытием**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , содержащую данные, используемые для асинхронного ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f1806-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="f1806-113">Если этот параметр имеет **значение NULL**, все запросы ввода-вывода для параметра *hFile* отменяются.</span><span class="sxs-lookup"><span data-stu-id="f1806-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="f1806-114">Если этот параметр не равен **null**, только определенные запросы ввода-вывода, выданные для файла с указанной структурой *лповерлаппед* OVERLAPPED, помечаются как отмененные. Это означает, что можно отменить один или несколько запросов, а функция [**канцелио**](cancelio.md) отменяет все необработанные запросы к файлу.</span><span class="sxs-lookup"><span data-stu-id="f1806-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1806-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1806-115">Return value</span></span>

<span data-ttu-id="f1806-116">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f1806-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="f1806-117">Запрошена операция отмены для всех ожидающих операций ввода-вывода, выданных вызывающим процессом для указанного маркера файла.</span><span class="sxs-lookup"><span data-stu-id="f1806-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="f1806-118">Приложение не должно освобождать или повторно использовать структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , связанную с отмененными операциями ввода-вывода, пока они не будут завершены.</span><span class="sxs-lookup"><span data-stu-id="f1806-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="f1806-119">Поток может использовать функцию [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) , чтобы определить, когда завершаются операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f1806-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="f1806-120">Если функция завершается ошибкой, возвращается значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f1806-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="f1806-121">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f1806-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="f1806-122">Если эта функция не может найти запрос на отмену, возвращаемое значение равно 0 (нулю), а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ не \_ удалось**.</span><span class="sxs-lookup"><span data-stu-id="f1806-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1806-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1806-123">Remarks</span></span>

<span data-ttu-id="f1806-124">Функция **канцелиоекс** позволяет отменять запросы в потоках, отличных от вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="f1806-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="f1806-125">Функция [**канцелио**](cancelio.md) отменяет запросы только в том же потоке, который вызвал функцию **канцелио** .</span><span class="sxs-lookup"><span data-stu-id="f1806-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="f1806-126">**Канцелиоекс** отменяет только что необработанные операции ввода-вывода для маркера, он не изменяет состояние маркера. Это означает, что вы не можете полагаться на состояние маркера, так как вы не можете определить, завершилась ли операция успешно или отменена.</span><span class="sxs-lookup"><span data-stu-id="f1806-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="f1806-127">Если для указанного маркера файла выполняются ожидающие операции ввода-вывода, функция **канцелиоекс** помечает их для отмены.</span><span class="sxs-lookup"><span data-stu-id="f1806-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="f1806-128">Большинство типов операций могут быть отменены немедленно. другие операции могут продолжать выполнение до того, как они будут фактически отменены, а вызывающий будет уведомлен.</span><span class="sxs-lookup"><span data-stu-id="f1806-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="f1806-129">Функция **канцелиоекс** не ждет завершения всех отмененных операций.</span><span class="sxs-lookup"><span data-stu-id="f1806-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="f1806-130">Если этот файл связан с портом завершения, пакет завершения ввода-вывода не помещается в очередь порта, если синхронная операция была успешно отменена.</span><span class="sxs-lookup"><span data-stu-id="f1806-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="f1806-131">Для асинхронных операций, которые все еще ожидают, операция отмены будет ставить в очередь пакет завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f1806-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="f1806-132">Операция, для которой выполняется отмена, завершена с одним из трех состояний; чтобы определить состояние завершения, необходимо проверить состояние завершения.</span><span class="sxs-lookup"><span data-stu-id="f1806-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="f1806-133">Три состояния:</span><span class="sxs-lookup"><span data-stu-id="f1806-133">The three statuses are:</span></span>

-   <span data-ttu-id="f1806-134">Операция выполнена нормально.</span><span class="sxs-lookup"><span data-stu-id="f1806-134">The operation completed normally.</span></span> <span data-ttu-id="f1806-135">Это может произойти, даже если операция была отменена, так как запрос отмены мог быть не отправлен вовремя, чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="f1806-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="f1806-136">Операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="f1806-136">The operation was canceled.</span></span> <span data-ttu-id="f1806-137">Функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **сообщение об ошибке " \_ операция была \_ прервана**".</span><span class="sxs-lookup"><span data-stu-id="f1806-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="f1806-138">Операция завершилась с другой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f1806-138">The operation failed with another error.</span></span> <span data-ttu-id="f1806-139">Функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f1806-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="f1806-140">В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.</span><span class="sxs-lookup"><span data-stu-id="f1806-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="f1806-141">Технология</span><span class="sxs-lookup"><span data-stu-id="f1806-141">Technology</span></span>                                           | <span data-ttu-id="f1806-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f1806-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="f1806-143">Протокол SMB 3,0</span><span class="sxs-lookup"><span data-stu-id="f1806-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="f1806-144">Да</span><span class="sxs-lookup"><span data-stu-id="f1806-144">Yes</span></span><br/> |
| <span data-ttu-id="f1806-145">Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)</span><span class="sxs-lookup"><span data-stu-id="f1806-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="f1806-146">Да</span><span class="sxs-lookup"><span data-stu-id="f1806-146">Yes</span></span><br/> |
| <span data-ttu-id="f1806-147">SMB 3,0 с масштабируемыми файловыми ресурсами (SO)</span><span class="sxs-lookup"><span data-stu-id="f1806-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="f1806-148">Да</span><span class="sxs-lookup"><span data-stu-id="f1806-148">Yes</span></span><br/> |
| <span data-ttu-id="f1806-149">Общий том кластераная файловая система (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="f1806-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="f1806-150">Да</span><span class="sxs-lookup"><span data-stu-id="f1806-150">Yes</span></span><br/> |
| <span data-ttu-id="f1806-151">Восстанавливаемая файловая система (ReFS)</span><span class="sxs-lookup"><span data-stu-id="f1806-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="f1806-152">Да</span><span class="sxs-lookup"><span data-stu-id="f1806-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1806-153">Требования</span><span class="sxs-lookup"><span data-stu-id="f1806-153">Requirements</span></span>



| <span data-ttu-id="f1806-154">Требование</span><span class="sxs-lookup"><span data-stu-id="f1806-154">Requirement</span></span> | <span data-ttu-id="f1806-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f1806-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1806-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1806-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f1806-157">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f1806-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="f1806-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1806-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f1806-159">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f1806-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="f1806-160">Header</span><span class="sxs-lookup"><span data-stu-id="f1806-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1806-161"><dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1806-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f1806-162">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1806-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1806-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1806-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="f1806-164">DLL</span><span class="sxs-lookup"><span data-stu-id="f1806-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1806-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1806-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="f1806-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1806-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1806-167">**канцелио**</span><span class="sxs-lookup"><span data-stu-id="f1806-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="f1806-168">**канцелсинчронаусио**</span><span class="sxs-lookup"><span data-stu-id="f1806-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="f1806-169">Отмена ожидающих операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="f1806-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="f1806-170">Функции управления файлами</span><span class="sxs-lookup"><span data-stu-id="f1806-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="f1806-171">Синхронный и асинхронный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="f1806-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

