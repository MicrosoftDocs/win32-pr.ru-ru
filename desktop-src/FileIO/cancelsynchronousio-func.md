---
description: Помечает ожидающие операции синхронного ввода-вывода, выданные указанным потоком как отмененные.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Функция Канцелсинчронаусио (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546698"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="71d8d-103">Функция Канцелсинчронаусио</span><span class="sxs-lookup"><span data-stu-id="71d8d-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="71d8d-104">Помечает ожидающие операции синхронного ввода-вывода, выданные указанным потоком как отмененные.</span><span class="sxs-lookup"><span data-stu-id="71d8d-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71d8d-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="71d8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71d8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d8d-107">*хсреад* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71d8d-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d8d-108">Обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="71d8d-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d8d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71d8d-109">Return value</span></span>

<span data-ttu-id="71d8d-110">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="71d8d-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="71d8d-111">Если функция завершается ошибкой, возвращается значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="71d8d-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="71d8d-112">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="71d8d-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="71d8d-113">Если эта функция не может найти запрос на отмену, возвращаемое значение равно 0 (нулю), а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ не \_ удалось**.</span><span class="sxs-lookup"><span data-stu-id="71d8d-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d8d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71d8d-114">Remarks</span></span>

<span data-ttu-id="71d8d-115">Вызывающий объект должен иметь право на [ \_ Завершение доступа потока](/windows/desktop/ProcThread/thread-security-and-access-rights) .</span><span class="sxs-lookup"><span data-stu-id="71d8d-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="71d8d-116">Если для указанного потока выполняются какие-либо ожидающие выполнения операции ввода/вывода, функция **канцелсинчронаусио** помечает их для отмены.</span><span class="sxs-lookup"><span data-stu-id="71d8d-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="71d8d-117">Большинство типов операций могут быть отменены немедленно. другие операции могут продолжать выполнение до того, как они будут фактически отменены, а вызывающий будет уведомлен.</span><span class="sxs-lookup"><span data-stu-id="71d8d-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="71d8d-118">Функция **канцелсинчронаусио** не ждет завершения всех отмененных операций.</span><span class="sxs-lookup"><span data-stu-id="71d8d-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="71d8d-119">Дополнительные сведения см. в разделе [рекомендации по завершению ввода-вывода и отмене](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)работы.</span><span class="sxs-lookup"><span data-stu-id="71d8d-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="71d8d-120">Операция, для которой выполняется отмена, завершена с одним из трех состояний; чтобы определить состояние завершения, необходимо проверить состояние завершения.</span><span class="sxs-lookup"><span data-stu-id="71d8d-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="71d8d-121">Три состояния:</span><span class="sxs-lookup"><span data-stu-id="71d8d-121">The three statuses are:</span></span>

-   <span data-ttu-id="71d8d-122">**Операция выполнена нормально.**</span><span class="sxs-lookup"><span data-stu-id="71d8d-122">**The operation completed normally.**</span></span> <span data-ttu-id="71d8d-123">Это может произойти, даже если операция была отменена, так как запрос отмены мог быть не отправлен вовремя, чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="71d8d-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="71d8d-124">**Операция была отменена.**</span><span class="sxs-lookup"><span data-stu-id="71d8d-124">**The operation was canceled.**</span></span> <span data-ttu-id="71d8d-125">Функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **сообщение об ошибке " \_ операция была \_ прервана**".</span><span class="sxs-lookup"><span data-stu-id="71d8d-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="71d8d-126">**Операция завершилась с другой ошибкой.**</span><span class="sxs-lookup"><span data-stu-id="71d8d-126">**The operation failed with another error.**</span></span> <span data-ttu-id="71d8d-127">Функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="71d8d-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="71d8d-128">В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.</span><span class="sxs-lookup"><span data-stu-id="71d8d-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="71d8d-129">Технология</span><span class="sxs-lookup"><span data-stu-id="71d8d-129">Technology</span></span>                                           | <span data-ttu-id="71d8d-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="71d8d-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="71d8d-131">Протокол SMB 3,0</span><span class="sxs-lookup"><span data-stu-id="71d8d-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="71d8d-132">Да</span><span class="sxs-lookup"><span data-stu-id="71d8d-132">Yes</span></span><br/> |
| <span data-ttu-id="71d8d-133">Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)</span><span class="sxs-lookup"><span data-stu-id="71d8d-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="71d8d-134">Да</span><span class="sxs-lookup"><span data-stu-id="71d8d-134">Yes</span></span><br/> |
| <span data-ttu-id="71d8d-135">SMB 3,0 с масштабируемыми файловыми ресурсами (SO)</span><span class="sxs-lookup"><span data-stu-id="71d8d-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="71d8d-136">Да</span><span class="sxs-lookup"><span data-stu-id="71d8d-136">Yes</span></span><br/> |
| <span data-ttu-id="71d8d-137">Общий том кластераная файловая система (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="71d8d-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="71d8d-138">Да</span><span class="sxs-lookup"><span data-stu-id="71d8d-138">Yes</span></span><br/> |
| <span data-ttu-id="71d8d-139">Восстанавливаемая файловая система (ReFS)</span><span class="sxs-lookup"><span data-stu-id="71d8d-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="71d8d-140">Да</span><span class="sxs-lookup"><span data-stu-id="71d8d-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71d8d-141">Требования</span><span class="sxs-lookup"><span data-stu-id="71d8d-141">Requirements</span></span>



| <span data-ttu-id="71d8d-142">Требование</span><span class="sxs-lookup"><span data-stu-id="71d8d-142">Requirement</span></span> | <span data-ttu-id="71d8d-143">Значение</span><span class="sxs-lookup"><span data-stu-id="71d8d-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d8d-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71d8d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="71d8d-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71d8d-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="71d8d-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71d8d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="71d8d-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71d8d-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="71d8d-148">Header</span><span class="sxs-lookup"><span data-stu-id="71d8d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d8d-149"><dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71d8d-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="71d8d-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71d8d-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="71d8d-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="71d8d-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="71d8d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="71d8d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d8d-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d8d-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="71d8d-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71d8d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d8d-155">**канцелио**</span><span class="sxs-lookup"><span data-stu-id="71d8d-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="71d8d-156">**канцелиоекс**</span><span class="sxs-lookup"><span data-stu-id="71d8d-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="71d8d-157">Функции управления файлами</span><span class="sxs-lookup"><span data-stu-id="71d8d-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="71d8d-158">Синхронный и асинхронный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="71d8d-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

