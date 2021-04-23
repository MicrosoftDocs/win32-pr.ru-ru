---
description: Возвращает несколько записей портов завершения одновременно.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Функция Жеткуеуедкомплетионстатусекс (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664433"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="44762-103">Функция Жеткуеуедкомплетионстатусекс</span><span class="sxs-lookup"><span data-stu-id="44762-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="44762-104">Возвращает несколько записей портов завершения одновременно.</span><span class="sxs-lookup"><span data-stu-id="44762-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="44762-105">Он ожидает завершения ожидающих операций ввода-вывода, связанных с указанным портом завершения.</span><span class="sxs-lookup"><span data-stu-id="44762-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="44762-106">Чтобы отменять постановку пакетов завершения ввода-вывода по одному, используйте функцию [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="44762-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="44762-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44762-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="44762-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="44762-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44762-109">*Комплетионпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44762-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44762-110">Маркер порта завершения.</span><span class="sxs-lookup"><span data-stu-id="44762-110">A handle to the completion port.</span></span> <span data-ttu-id="44762-111">Чтобы создать порт завершения, используйте функцию [**CreateIoCompletionPort**](createiocompletionport.md) .</span><span class="sxs-lookup"><span data-stu-id="44762-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="44762-112">*лпкомплетионпортентриес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44762-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44762-113">На входе указывает на предварительно выделенный массив [**перекрывающихся структур \_ записи**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .</span><span class="sxs-lookup"><span data-stu-id="44762-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="44762-114">На выходе получает массив [**перекрывающихся структур \_ записи**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) , содержащих записи.</span><span class="sxs-lookup"><span data-stu-id="44762-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="44762-115">Число элементов массива предоставляется *улнументриесремовед*.</span><span class="sxs-lookup"><span data-stu-id="44762-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="44762-116">Число байтов, передаваемых при каждом вводе-выводе, ключ завершения, указывающий, какой файл выполняется каждый ввод-вывод, и адрес перекрывающейся структуры, используемый в каждом исходном вводе-выводе, возвращается в массиве *лпкомплетионпортентриес* .</span><span class="sxs-lookup"><span data-stu-id="44762-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="44762-117">*улкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44762-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44762-118">Максимальное число удаляемых записей.</span><span class="sxs-lookup"><span data-stu-id="44762-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="44762-119">*улнументриесремовед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44762-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44762-120">Указатель на переменную, которая получает число фактически удаленных записей.</span><span class="sxs-lookup"><span data-stu-id="44762-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="44762-121">*dwMilliseconds* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44762-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44762-122">Время в миллисекундах, в течение которого вызывающая сторона ожидает отображения пакета завершения в порте завершения.</span><span class="sxs-lookup"><span data-stu-id="44762-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="44762-123">Если пакет завершения не отображается в течение заданного времени, функция истечет время ожидания и возвратит **значение false**.</span><span class="sxs-lookup"><span data-stu-id="44762-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="44762-124">Если *dwMilliseconds* имеет **бесконечное** значение (0xFFFFFFFF), функция никогда не будет исключаться. Если *dwMilliseconds* равен нулю, а операция ввода-вывода для выхода из очереди отсутствует, функция будет немедленно истечет.</span><span class="sxs-lookup"><span data-stu-id="44762-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="44762-125">*фалертабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44762-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44762-126">Если этот параметр имеет **значение false**, функция не возвращает результат, пока не истечет время ожидания или не будет получена запись.</span><span class="sxs-lookup"><span data-stu-id="44762-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="44762-127">Если параметр имеет **значение true** и отсутствуют доступные записи, функция выполняет предупреждение.</span><span class="sxs-lookup"><span data-stu-id="44762-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="44762-128">Поток возвращается, когда система помещает в очередь подпрограммы завершения ввода-вывода или APC в поток, а поток выполняет функцию.</span><span class="sxs-lookup"><span data-stu-id="44762-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="44762-129">Подпрограммы завершения помещаются в очередь, когда функция [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) или [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) , в которой она была указана, была завершена, а вызывающий поток — это поток, который инициировал операцию.</span><span class="sxs-lookup"><span data-stu-id="44762-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="44762-130">Компания APC помещается в очередь при вызове [**куеуеусерапк**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span><span class="sxs-lookup"><span data-stu-id="44762-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44762-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44762-131">Return value</span></span>

<span data-ttu-id="44762-132">Возвращает ненулевое **значение (true**) в случае успешного или нулевого значения (**false**) в противном случае.</span><span class="sxs-lookup"><span data-stu-id="44762-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="44762-133">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="44762-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="44762-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44762-134">Remarks</span></span>

<span data-ttu-id="44762-135">Эта функция связывает поток с указанным портом завершения.</span><span class="sxs-lookup"><span data-stu-id="44762-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="44762-136">Поток может быть связан не более чем с одним портом завершения.</span><span class="sxs-lookup"><span data-stu-id="44762-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="44762-137">Эта функция возвращает **значение true** , если по крайней мере один ожидающий ввод-вывод завершен, но возможно, что произошел сбой одной или нескольких операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="44762-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="44762-138">Обратите внимание, что пользователь этой функции может проверить список возвращенных записей в параметре *лпкомплетионпортентриес* , чтобы определить, какие из них соответствуют любым возможным операциям ввода-вывода, просмотрев состояние, содержащееся в элементе **лповерлаппед** в каждой [**перекрывающейся \_ записи**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="44762-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="44762-139">Эта функция возвращает **значение false** , если ни одна операция ввода-вывода не была выведена из очереди.</span><span class="sxs-lookup"><span data-stu-id="44762-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="44762-140">Обычно это означает, что при обработке параметров для этого вызова произошла ошибка или маркер *комплетионпорт* был закрыт или в противном случае является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="44762-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="44762-141">Функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) предоставляет расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="44762-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="44762-142">Если вызов [**жеткуеуедкомплетионстатусекс**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) завершается сбоем из-за закрытия связанного с ним маркера, функция возвращает **значение false** , а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвратит **ошибку No \_ \_ Wait \_ 0**.</span><span class="sxs-lookup"><span data-stu-id="44762-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="44762-143">Серверные приложения могут иметь несколько потоков, вызывающих функцию **жеткуеуедкомплетионстатусекс** для одного и того же порта завершения.</span><span class="sxs-lookup"><span data-stu-id="44762-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="44762-144">По мере завершения операций ввода-вывода они помещаются в очередь на этот порт в порядке "первым пов первом выходе".</span><span class="sxs-lookup"><span data-stu-id="44762-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="44762-145">Если поток активно ожидает этого вызова, один или несколько запросов, помещенных в очередь, завершают вызов только для этого потока.</span><span class="sxs-lookup"><span data-stu-id="44762-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="44762-146">Дополнительные сведения о теории портов завершения ввода-вывода, использовании и связанных функциях см. в разделе [порты завершения ввода-вывода](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="44762-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="44762-147">В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.</span><span class="sxs-lookup"><span data-stu-id="44762-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="44762-148">Технология</span><span class="sxs-lookup"><span data-stu-id="44762-148">Technology</span></span>                                           | <span data-ttu-id="44762-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="44762-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="44762-150">Протокол SMB 3,0</span><span class="sxs-lookup"><span data-stu-id="44762-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="44762-151">Да</span><span class="sxs-lookup"><span data-stu-id="44762-151">Yes</span></span><br/> |
| <span data-ttu-id="44762-152">Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)</span><span class="sxs-lookup"><span data-stu-id="44762-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="44762-153">Да</span><span class="sxs-lookup"><span data-stu-id="44762-153">Yes</span></span><br/> |
| <span data-ttu-id="44762-154">SMB 3,0 с масштабируемыми файловыми ресурсами (SO)</span><span class="sxs-lookup"><span data-stu-id="44762-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="44762-155">Да</span><span class="sxs-lookup"><span data-stu-id="44762-155">Yes</span></span><br/> |
| <span data-ttu-id="44762-156">Общий том кластераная файловая система (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="44762-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="44762-157">Да</span><span class="sxs-lookup"><span data-stu-id="44762-157">Yes</span></span><br/> |
| <span data-ttu-id="44762-158">Восстанавливаемая файловая система (ReFS)</span><span class="sxs-lookup"><span data-stu-id="44762-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="44762-159">Да</span><span class="sxs-lookup"><span data-stu-id="44762-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="44762-160">Требования</span><span class="sxs-lookup"><span data-stu-id="44762-160">Requirements</span></span>



| <span data-ttu-id="44762-161">Требование</span><span class="sxs-lookup"><span data-stu-id="44762-161">Requirement</span></span> | <span data-ttu-id="44762-162">Значение</span><span class="sxs-lookup"><span data-stu-id="44762-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44762-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44762-163">Minimum supported client</span></span><br/> | <span data-ttu-id="44762-164">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="44762-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="44762-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44762-165">Minimum supported server</span></span><br/> | <span data-ttu-id="44762-166">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="44762-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="44762-167">Header</span><span class="sxs-lookup"><span data-stu-id="44762-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="44762-168"><dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44762-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="44762-169">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44762-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="44762-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="44762-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="44762-171">DLL</span><span class="sxs-lookup"><span data-stu-id="44762-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44762-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44762-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="44762-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44762-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="44762-174">**Обзорные разделы**</span><span class="sxs-lookup"><span data-stu-id="44762-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="44762-175">Функции управления файлами</span><span class="sxs-lookup"><span data-stu-id="44762-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="44762-176">Порты завершения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="44762-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="44762-177">Использование заголовков Windows</span><span class="sxs-lookup"><span data-stu-id="44762-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="44762-178">**Функции**</span><span class="sxs-lookup"><span data-stu-id="44762-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="44762-179">**коннектнамедпипе**</span><span class="sxs-lookup"><span data-stu-id="44762-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="44762-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="44762-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="44762-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="44762-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="44762-182">**жеткуеуедкомплетионстатусекс**</span><span class="sxs-lookup"><span data-stu-id="44762-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="44762-183">**локкфиликс**</span><span class="sxs-lookup"><span data-stu-id="44762-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="44762-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="44762-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="44762-185">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="44762-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="44762-186">**трансактнамедпипе**</span><span class="sxs-lookup"><span data-stu-id="44762-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="44762-187">**ваиткоммевент**</span><span class="sxs-lookup"><span data-stu-id="44762-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="44762-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="44762-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

