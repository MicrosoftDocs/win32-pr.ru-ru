---
description: Предоставление пользователям возможности отменять запросы ввода-вывода, которые замедляют или блокируется, может повысить удобство использования и надежность приложения.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Отмена ожидающих операций ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684382"
---
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="16a1a-103">Отмена ожидающих операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="16a1a-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="16a1a-104">Предоставление пользователям возможности отменять запросы ввода-вывода, которые замедляют или блокируется, может повысить удобство использования и надежность приложения.</span><span class="sxs-lookup"><span data-stu-id="16a1a-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="16a1a-105">Например, если вызов функции [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) заблокирован, так как вызов выполняется на очень низком устройстве, отмена этого параметра позволяет снова выполнить вызов с новыми параметрами без завершения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="16a1a-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="16a1a-106">Windows Vista расширяет возможности отмены, а также поддерживает отмену синхронных операций.</span><span class="sxs-lookup"><span data-stu-id="16a1a-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="16a1a-107">**Примечание**  .  Вызов функции [**канцелиоекс**](cancelioex-func.md) не гарантирует, что операция ввода-вывода будет отменена. драйвер, обрабатывающий операцию, должен поддерживать отмену, и операция должна находиться в состоянии, которое может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="16a1a-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="16a1a-108">Рекомендации по отмене</span><span class="sxs-lookup"><span data-stu-id="16a1a-108">Cancellation Considerations</span></span>

<span data-ttu-id="16a1a-109">При программировании вызовов отмены следует учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="16a1a-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="16a1a-110">Нет никакой гарантии, что базовые драйверы правильно поддерживают отмену.</span><span class="sxs-lookup"><span data-stu-id="16a1a-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="16a1a-111">При отмене асинхронного ввода-вывода при отсутствии перекрытой структуры функции [**канцелиоекс**](cancelioex-func.md) функция пытается отменить все необработанные операции ввода-вывода для файла во всех потоках процесса.</span><span class="sxs-lookup"><span data-stu-id="16a1a-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="16a1a-112">Каждый поток обрабатывается по отдельности, поэтому после обработки потока он может запустить другой ввод-вывод для файла, прежде чем все остальные потоки настроили операции ввода-вывода для файла, что приведет к проблемам синхронизации.</span><span class="sxs-lookup"><span data-stu-id="16a1a-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="16a1a-113">При отмене асинхронного ввода-вывода не следует повторно использовать перекрывающиеся структуры с целевой отменой.</span><span class="sxs-lookup"><span data-stu-id="16a1a-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="16a1a-114">После завершения операции ввода-вывода (либо успешно, либо с отмененным состоянием) перекрывающаяся структура больше не используется системой и может быть использована повторно.</span><span class="sxs-lookup"><span data-stu-id="16a1a-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="16a1a-115">При отмене синхронного ввода-вывода вызов функции [**канцелсинчронаусио**](cancelsynchronousio-func.md) пытается отменить любой текущий синхронный вызов в потоке.</span><span class="sxs-lookup"><span data-stu-id="16a1a-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="16a1a-116">Необходимо следить, чтобы обеспечить правильную синхронизацию вызовов. Недопустимый вызов в последовательности вызовов может быть отменен.</span><span class="sxs-lookup"><span data-stu-id="16a1a-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="16a1a-117">Например, если функция **канцелсинчронаусио** вызывается для синхронной операции, x, операция Y начинается только после завершения операции x (обычно или с ошибкой).</span><span class="sxs-lookup"><span data-stu-id="16a1a-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="16a1a-118">Если поток, вызвавший операцию X, запускает еще один синхронный вызов к X, вызов отмены может привести к прерыванию нового запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="16a1a-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="16a1a-119">При отмене синхронного ввода-вывода имейте в виду, что состояние гонки может существовать всякий раз, когда поток совместно используется различными частями приложения, например с потоком пула потоков.</span><span class="sxs-lookup"><span data-stu-id="16a1a-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="16a1a-120">Операции, которые не могут быть отменены</span><span class="sxs-lookup"><span data-stu-id="16a1a-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="16a1a-121">Некоторые функции не могут быть отменены с помощью функции [**канцелио**](cancelio.md), [**канцелиоекс**](cancelioex-func.md)или [**канцелсинчронаусио**](cancelsynchronousio-func.md) .</span><span class="sxs-lookup"><span data-stu-id="16a1a-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="16a1a-122">Некоторые из этих функций были расширены для разрешения отмены (например, функции [**копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ), и вместо них следует использовать.</span><span class="sxs-lookup"><span data-stu-id="16a1a-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="16a1a-123">Помимо поддержки отмены, эти функции также имеют встроенные обратные вызовы для поддержки при отслеживании хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="16a1a-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="16a1a-124">Следующие функции не поддерживают отмену:</span><span class="sxs-lookup"><span data-stu-id="16a1a-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="16a1a-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)— использование [ **копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="16a1a-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="16a1a-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)— используйте [ **мовефилевиспрогресс**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="16a1a-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="16a1a-127">[**Мовефиликс**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)— используйте [ **мовефилевиспрогресс**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="16a1a-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="16a1a-128">**реплацефиле**</span><span class="sxs-lookup"><span data-stu-id="16a1a-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="16a1a-129">Дополнительные сведения см. в разделе [рекомендации по завершению ввода-вывода и отмене](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)работы.</span><span class="sxs-lookup"><span data-stu-id="16a1a-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="16a1a-130">Отмена асинхронного ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="16a1a-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="16a1a-131">Асинхронный ввод-вывод можно отменить из любого потока в процессе, который выдал операцию ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="16a1a-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="16a1a-132">Необходимо указать маркер, который операция ввода-вывода была выполнена, и, при необходимости, структуру OVERLAPPED, которая использовалась для выполнения операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="16a1a-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="16a1a-133">Можно определить, произошло ли отмена, изучив состояние, возвращенное в структуре OVERLAPPED, или в обратном вызове завершения.</span><span class="sxs-lookup"><span data-stu-id="16a1a-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="16a1a-134">Состояние операции " **Ошибка \_ \_ прервано** " означает, что операция была отменена.</span><span class="sxs-lookup"><span data-stu-id="16a1a-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="16a1a-135">В следующем примере показана подпрограммы, которая принимает время ожидания и пытается выполнить операцию чтения, отменяя ее с помощью функции [**канцелиоекс**](cancelioex-func.md) , если истекло время ожидания.</span><span class="sxs-lookup"><span data-stu-id="16a1a-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a><span data-ttu-id="16a1a-136">Отмена синхронного ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="16a1a-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="16a1a-137">Вы можете отменить синхронный ввод-вывод из любого потока процесса, который выдал операцию ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="16a1a-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="16a1a-138">Необходимо указать обработчик для потока, который в данный момент выполняет операцию ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="16a1a-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="16a1a-139">В следующем примере показаны две подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="16a1a-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="16a1a-140">Функция **синчронаусиоворкер** — это рабочий поток, который реализует некоторый синхронный файловый ввод-вывод, начиная с вызова функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="16a1a-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="16a1a-141">Если подпрограммы выполняются успешно, за подпрограммы могут следовать дополнительные операции, которые не включены здесь.</span><span class="sxs-lookup"><span data-stu-id="16a1a-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="16a1a-142">Глобальную переменную *гкомплетионстатус* можно использовать для определения успешности всех операций, а также от того, завершилась ли операция ошибкой или отменена.</span><span class="sxs-lookup"><span data-stu-id="16a1a-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="16a1a-143">Глобальная переменная *двоператионинпрогресс* указывает, выполняется ли файловый ввод-вывод.</span><span class="sxs-lookup"><span data-stu-id="16a1a-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="16a1a-144">**Примечание**  .  В этом примере поток пользовательского интерфейса также может проверить существование рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="16a1a-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="16a1a-145">Дополнительные ручные проверки, которые здесь не включены, необходимы в функции **синчронаусиоворкер** , чтобы гарантировать, что если отмена была запрошена в течение короткого периода между вызовами файлового ввода-вывода, остальные операции будут отменены.</span><span class="sxs-lookup"><span data-stu-id="16a1a-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="16a1a-146">Функция **маинуисреадмессажехандлер** имитирует обработчик сообщений в оконной процедуре потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="16a1a-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="16a1a-147">Пользователь запрашивает набор синхронных операций с файлами, щелкая элемент управления, который создает определяемое пользователем сообщение окна (в разделе, помеченном **WM \_ мисинкопс**).</span><span class="sxs-lookup"><span data-stu-id="16a1a-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="16a1a-148">При этом создается новый поток с помощью функции **креатефилесреад** , которая затем запускает функцию **синчронаусиоворкер** .</span><span class="sxs-lookup"><span data-stu-id="16a1a-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="16a1a-149">Поток пользовательского интерфейса по-прежнему обрабатывает сообщения, пока рабочий поток выполняет запрошенные операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="16a1a-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="16a1a-150">Если пользователь решает отменить незавершенные операции (обычно путем нажатия кнопки "Отмена"), подпрограммы (в разделе, помеченном **WM \_ миканцел**) вызывают функцию [**канцелсинчронаусио**](cancelsynchronousio-func.md) с помощью обработчика потока, возвращенного функцией **креатефилесреад** .</span><span class="sxs-lookup"><span data-stu-id="16a1a-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="16a1a-151">Функция **канцелсинчронаусио** возвращает сразу после попытки отмены.</span><span class="sxs-lookup"><span data-stu-id="16a1a-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="16a1a-152">Наконец, пользователь или приложение могут позже запросить некоторую другую операцию, которая зависит от того, завершились ли файловые операции.</span><span class="sxs-lookup"><span data-stu-id="16a1a-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="16a1a-153">В этом случае подпрограммы (в разделе, помеченном **WM \_ PROCESSDATA**) сначала проверяют, завершены ли операции, а затем выполняют операции очистки.</span><span class="sxs-lookup"><span data-stu-id="16a1a-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="16a1a-154">**Примечание**  .  В этом примере, поскольку отмена могла произойти в любой точке последовательности операций, перед продолжением может потребоваться убедиться, что состояние является целостным или как минимум понятным.</span><span class="sxs-lookup"><span data-stu-id="16a1a-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="16a1a-155">См. также</span><span class="sxs-lookup"><span data-stu-id="16a1a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16a1a-156">Синхронный и асинхронный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="16a1a-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



