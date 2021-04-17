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
# <a name="canceling-pending-io-operations"></a>Отмена ожидающих операций ввода-вывода

Предоставление пользователям возможности отменять запросы ввода-вывода, которые замедляют или блокируется, может повысить удобство использования и надежность приложения. Например, если вызов функции [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) заблокирован, так как вызов выполняется на очень низком устройстве, отмена этого параметра позволяет снова выполнить вызов с новыми параметрами без завершения работы приложения.

Windows Vista расширяет возможности отмены, а также поддерживает отмену синхронных операций.

**Примечание**  .  Вызов функции [**канцелиоекс**](cancelioex-func.md) не гарантирует, что операция ввода-вывода будет отменена. драйвер, обрабатывающий операцию, должен поддерживать отмену, и операция должна находиться в состоянии, которое может быть отменено.

## <a name="cancellation-considerations"></a>Рекомендации по отмене

При программировании вызовов отмены следует учитывать следующие моменты.

-   Нет никакой гарантии, что базовые драйверы правильно поддерживают отмену.
-   При отмене асинхронного ввода-вывода при отсутствии перекрытой структуры функции [**канцелиоекс**](cancelioex-func.md) функция пытается отменить все необработанные операции ввода-вывода для файла во всех потоках процесса. Каждый поток обрабатывается по отдельности, поэтому после обработки потока он может запустить другой ввод-вывод для файла, прежде чем все остальные потоки настроили операции ввода-вывода для файла, что приведет к проблемам синхронизации.
-   При отмене асинхронного ввода-вывода не следует повторно использовать перекрывающиеся структуры с целевой отменой. После завершения операции ввода-вывода (либо успешно, либо с отмененным состоянием) перекрывающаяся структура больше не используется системой и может быть использована повторно.
-   При отмене синхронного ввода-вывода вызов функции [**канцелсинчронаусио**](cancelsynchronousio-func.md) пытается отменить любой текущий синхронный вызов в потоке. Необходимо следить, чтобы обеспечить правильную синхронизацию вызовов. Недопустимый вызов в последовательности вызовов может быть отменен. Например, если функция **канцелсинчронаусио** вызывается для синхронной операции, x, операция Y начинается только после завершения операции x (обычно или с ошибкой). Если поток, вызвавший операцию X, запускает еще один синхронный вызов к X, вызов отмены может привести к прерыванию нового запроса ввода-вывода.
-   При отмене синхронного ввода-вывода имейте в виду, что состояние гонки может существовать всякий раз, когда поток совместно используется различными частями приложения, например с потоком пула потоков.

## <a name="operations-that-cannot-be-canceled"></a>Операции, которые не могут быть отменены

Некоторые функции не могут быть отменены с помощью функции [**канцелио**](cancelio.md), [**канцелиоекс**](cancelioex-func.md)или [**канцелсинчронаусио**](cancelsynchronousio-func.md) . Некоторые из этих функций были расширены для разрешения отмены (например, функции [**копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ), и вместо них следует использовать. Помимо поддержки отмены, эти функции также имеют встроенные обратные вызовы для поддержки при отслеживании хода выполнения операции. Следующие функции не поддерживают отмену:

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)— использование [ **копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)— используйте [ **мовефилевиспрогресс**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**Мовефиликс**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)— используйте [ **мовефилевиспрогресс**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**реплацефиле**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Дополнительные сведения см. в разделе [рекомендации по завершению ввода-вывода и отмене](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)работы.

## <a name="canceling-asynchronous-io"></a>Отмена асинхронного ввода-вывода

Асинхронный ввод-вывод можно отменить из любого потока в процессе, который выдал операцию ввода-вывода. Необходимо указать маркер, который операция ввода-вывода была выполнена, и, при необходимости, структуру OVERLAPPED, которая использовалась для выполнения операций ввода-вывода. Можно определить, произошло ли отмена, изучив состояние, возвращенное в структуре OVERLAPPED, или в обратном вызове завершения. Состояние операции " **Ошибка \_ \_ прервано** " означает, что операция была отменена.

В следующем примере показана подпрограммы, которая принимает время ожидания и пытается выполнить операцию чтения, отменяя ее с помощью функции [**канцелиоекс**](cancelioex-func.md) , если истекло время ожидания.


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



## <a name="canceling-synchronous-io"></a>Отмена синхронного ввода-вывода

Вы можете отменить синхронный ввод-вывод из любого потока процесса, который выдал операцию ввода-вывода. Необходимо указать обработчик для потока, который в данный момент выполняет операцию ввода-вывода.

В следующем примере показаны две подпрограммы:

-   Функция **синчронаусиоворкер** — это рабочий поток, который реализует некоторый синхронный файловый ввод-вывод, начиная с вызова функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Если подпрограммы выполняются успешно, за подпрограммы могут следовать дополнительные операции, которые не включены здесь. Глобальную переменную *гкомплетионстатус* можно использовать для определения успешности всех операций, а также от того, завершилась ли операция ошибкой или отменена. Глобальная переменная *двоператионинпрогресс* указывает, выполняется ли файловый ввод-вывод.

    **Примечание**  .  В этом примере поток пользовательского интерфейса также может проверить существование рабочего потока.

    Дополнительные ручные проверки, которые здесь не включены, необходимы в функции **синчронаусиоворкер** , чтобы гарантировать, что если отмена была запрошена в течение короткого периода между вызовами файлового ввода-вывода, остальные операции будут отменены.

-   Функция **маинуисреадмессажехандлер** имитирует обработчик сообщений в оконной процедуре потока пользовательского интерфейса. Пользователь запрашивает набор синхронных операций с файлами, щелкая элемент управления, который создает определяемое пользователем сообщение окна (в разделе, помеченном **WM \_ мисинкопс**). При этом создается новый поток с помощью функции **креатефилесреад** , которая затем запускает функцию **синчронаусиоворкер** . Поток пользовательского интерфейса по-прежнему обрабатывает сообщения, пока рабочий поток выполняет запрошенные операции ввода-вывода. Если пользователь решает отменить незавершенные операции (обычно путем нажатия кнопки "Отмена"), подпрограммы (в разделе, помеченном **WM \_ миканцел**) вызывают функцию [**канцелсинчронаусио**](cancelsynchronousio-func.md) с помощью обработчика потока, возвращенного функцией **креатефилесреад** . Функция **канцелсинчронаусио** возвращает сразу после попытки отмены. Наконец, пользователь или приложение могут позже запросить некоторую другую операцию, которая зависит от того, завершились ли файловые операции. В этом случае подпрограммы (в разделе, помеченном **WM \_ PROCESSDATA**) сначала проверяют, завершены ли операции, а затем выполняют операции очистки.

    **Примечание**  .  В этом примере, поскольку отмена могла произойти в любой точке последовательности операций, перед продолжением может потребоваться убедиться, что состояние является целостным или как минимум понятным.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Синхронный и асинхронный ввод-вывод](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



