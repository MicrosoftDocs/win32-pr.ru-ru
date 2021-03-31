---
description: В этом разделе описывается запуск и завершение потока обработки заданий печати.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: Как запускать и прекращать поток печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272487"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="04507-103">Как запускать и прекращать поток печати</span><span class="sxs-lookup"><span data-stu-id="04507-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="04507-104">В этом разделе описывается запуск и завершение потока обработки заданий печати.</span><span class="sxs-lookup"><span data-stu-id="04507-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="04507-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="04507-105">Overview</span></span>

<span data-ttu-id="04507-106">Чтобы запретить действиям печати блокировать ответ пользовательского интерфейса, создайте отдельный поток для обработки задания печати.</span><span class="sxs-lookup"><span data-stu-id="04507-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="04507-107">Поток, запускаемый при запуске программы, — это поток, который обрабатывает сообщения окна, являющиеся результатом взаимодействия с пользователем, и, следовательно, поток пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="04507-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="04507-108">Программа должна обрабатывать эти сообщения без задержки, чтобы пользовательский интерфейс своевременно отвечал на вход пользователя и на клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="04507-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="04507-109">Чтобы программа могла быстро реагировать на эти сообщения, объем обработки, который может быть выполнен в рамках одного сообщения, ограничен.</span><span class="sxs-lookup"><span data-stu-id="04507-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="04507-110">Когда для запроса пользователя требуется расширенная обработка, другой поток должен выполнить эту обработку, чтобы обеспечить обработку последующего взаимодействия с пользователем в программе.</span><span class="sxs-lookup"><span data-stu-id="04507-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="04507-111">Обработка данных в отдельном потоке требует, чтобы программа координирует работу потока пользовательского интерфейса и потока обработки.</span><span class="sxs-lookup"><span data-stu-id="04507-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="04507-112">Например, пока поток обработки обрабатывает данные, основной поток не должен изменять эти данные.</span><span class="sxs-lookup"><span data-stu-id="04507-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="04507-113">Одним из способов управления это является поточно-ориентированные объекты синхронизации, такие как семафоры, события и мьютексы.</span><span class="sxs-lookup"><span data-stu-id="04507-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="04507-114">В то же время во время выполнения потока обработки необходимо предотвратить некоторое вмешательство пользователя.</span><span class="sxs-lookup"><span data-stu-id="04507-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="04507-115">В демонстрационной программе данные приложения защищаются, и взаимодействие с пользователем ограничено за счет управления обработкой заданий печати с помощью диалогового окна "модальное выполнение".</span><span class="sxs-lookup"><span data-stu-id="04507-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="04507-116">Модальное диалоговое окно предотвращает взаимодействие пользователя с главным окном программы, что предотвращает изменение пользователем данных программы во время печати данных.</span><span class="sxs-lookup"><span data-stu-id="04507-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="04507-117">Единственным действием, которое может выполнить пользователь во время обработки задания печати, является отмена задания печати.</span><span class="sxs-lookup"><span data-stu-id="04507-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="04507-118">Это ограничение сообщает пользователю по форме курсора.</span><span class="sxs-lookup"><span data-stu-id="04507-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="04507-119">Когда курсор находится над кнопкой **Отмена** , отображается курсор со стрелкой, который указывает, что пользователь может нажать эту кнопку.</span><span class="sxs-lookup"><span data-stu-id="04507-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="04507-120">Когда курсор находится над любой другой частью области окна программы, отображается курсор ожидания, который указывает, что программа занята и не может ответить на ввод данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="04507-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="04507-121">Создание процедуры потока печати</span><span class="sxs-lookup"><span data-stu-id="04507-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="04507-122">Мы рекомендуем включить эти функции во время обработки печати.</span><span class="sxs-lookup"><span data-stu-id="04507-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="04507-123">**Обработка печати делится на этапы**</span><span class="sxs-lookup"><span data-stu-id="04507-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="04507-124">Можно разделить обработку печати на дискретные этапы обработки, которые можно прервать, если пользователь нажмет кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="04507-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="04507-125">Это полезно, поскольку обработка печати может включать ресурсоемкие операции.</span><span class="sxs-lookup"><span data-stu-id="04507-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="04507-126">Разбиение этой обработки на шаги может помешать обработке печати блокировать или откладывать другие потоки или процессы.</span><span class="sxs-lookup"><span data-stu-id="04507-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="04507-127">Разбиение обработки на логические шаги также позволяет четко завершить обработку печати в любой момент, чтобы завершить задание печати до его завершения, не покидая ни одного потерянного ресурса.</span><span class="sxs-lookup"><span data-stu-id="04507-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="04507-128">Это пример списка шагов печати.</span><span class="sxs-lookup"><span data-stu-id="04507-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="04507-129">**Проверка события Cancel между шагами**</span><span class="sxs-lookup"><span data-stu-id="04507-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="04507-130">Когда пользователь нажимает кнопку **Отмена** , поток пользовательского интерфейса сигнализирует о событии Cancel.</span><span class="sxs-lookup"><span data-stu-id="04507-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="04507-131">Поток обработки должен периодически проверять событие Cancel, чтобы узнать, когда пользователь нажмет кнопку **"Отмена** ".</span><span class="sxs-lookup"><span data-stu-id="04507-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="04507-132">Инструкции [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) выполняют эту проверку, а также предоставляют другим программам возможность запуска, чтобы обработка задания печати не блокировала или не задерживает другие потоки или процессы.</span><span class="sxs-lookup"><span data-stu-id="04507-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="04507-133">В следующем примере кода показан один из тестов, позволяющий определить, произошло ли событие Cancel.</span><span class="sxs-lookup"><span data-stu-id="04507-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="04507-134">**Отправка обновлений состояния в поток пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="04507-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="04507-135">Как и каждый шаг обработки печати, поток обработки печати отправляет сообщения обновления в диалоговое окно "ход печати", чтобы оно может обновить индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="04507-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="04507-136">Обратите внимание, что диалоговое окно "ход печати" выполняется в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="04507-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="04507-137">В следующем примере кода показано одно из вызовов сообщения об обновлении.</span><span class="sxs-lookup"><span data-stu-id="04507-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="04507-138">Запуск потока печати</span><span class="sxs-lookup"><span data-stu-id="04507-138">Starting the Printing Thread</span></span>

<span data-ttu-id="04507-139">Поток обработки печати выполняется до тех пор, пока функция Принтсреадпрок не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="04507-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="04507-140">Чтобы запустить поток печати, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="04507-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="04507-141">**Подготовьте данные и элементы пользовательского интерфейса для печати.**</span><span class="sxs-lookup"><span data-stu-id="04507-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="04507-142">Перед запуском потока обработки печати необходимо инициализировать элементы данных, которые описывают задание печати и элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="04507-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="04507-143">Эти элементы включают состояние курсора, поэтому курсор ожидания будет отображаться соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="04507-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="04507-144">Также необходимо настроить индикатор выполнения, чтобы он отражал размер задания печати.</span><span class="sxs-lookup"><span data-stu-id="04507-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="04507-145">Эти подготовительные действия подробно описаны в статье [как получить сведения о задании печати от пользователя](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="04507-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="04507-146">В следующем примере кода показано, как настроить индикатор выполнения, чтобы отразить размер задания печати, запрошенного пользователем.</span><span class="sxs-lookup"><span data-stu-id="04507-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  <span data-ttu-id="04507-147">**Запустите поток обработки печати.**</span><span class="sxs-lookup"><span data-stu-id="04507-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="04507-148">Вызовите функцию [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , чтобы запустить поток обработки.</span><span class="sxs-lookup"><span data-stu-id="04507-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="04507-149">В следующем примере кода запускается поток обработки.</span><span class="sxs-lookup"><span data-stu-id="04507-149">The following code example starts the processing thread.</span></span>

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  <span data-ttu-id="04507-150">**Проверьте, не завершилась ли обработка печати при запуске.**</span><span class="sxs-lookup"><span data-stu-id="04507-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="04507-151">Функция [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) возвращает маркер созданному потоку, если поток был успешно создан.</span><span class="sxs-lookup"><span data-stu-id="04507-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="04507-152">Функция Принтсреадпрок, которая была запущена в новом потоке, проверяет некоторые условия до того, как начнется фактическая обработка задания печати.</span><span class="sxs-lookup"><span data-stu-id="04507-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="04507-153">Если обнаруживаются ошибки в этих проверках, Принтсреадпрок может вернуть данные без обработки каких бы то ни было данных задания печати.</span><span class="sxs-lookup"><span data-stu-id="04507-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="04507-154">Поток пользовательского интерфейса может проверить, успешно ли запущен поток обработки, ожидая обработки в течение определенного периода времени, превышающего время, необходимое для выполнения начальных тестов, но больше не нужно.</span><span class="sxs-lookup"><span data-stu-id="04507-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="04507-155">Когда поток завершает работу, дескриптор потока получает сигнал.</span><span class="sxs-lookup"><span data-stu-id="04507-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="04507-156">Код проверяет состояние потока на короткий период времени после запуска потока обработки.</span><span class="sxs-lookup"><span data-stu-id="04507-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="04507-157">Функция [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) возвращает значение, если истекло время ожидания или когда дескриптор потока получает сигнал.</span><span class="sxs-lookup"><span data-stu-id="04507-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="04507-158">Если функция **WaitForSingleObject** возвращает состояние **ожидания \_ объекта \_ 0** , поток завершился раньше, поэтому следует закрыть диалоговое окно хода выполнения, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="04507-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="04507-159">Остановка потока печати</span><span class="sxs-lookup"><span data-stu-id="04507-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="04507-160">Когда пользователь нажимает кнопку **"Отмена** " в диалоговом окне "ход печати", поток печати получает уведомления, чтобы он мог прекратить обработку задания печати упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="04507-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="04507-161">Хотя кнопка **Cancel** и событие **куитевент** являются важными аспектами этой обработки, необходимо спроектировать всю последовательность обработки для успешного прерывания.</span><span class="sxs-lookup"><span data-stu-id="04507-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="04507-162">Это означает, что шаги последовательности не должны оставлять выделенные ресурсы, которые не освобождаются, если пользователь отменит последовательность до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="04507-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="04507-163">В следующем примере кода показано, как образец программы проверяет **куитевент** перед обработкой каждой страницы печатаемого документа.</span><span class="sxs-lookup"><span data-stu-id="04507-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="04507-164">Если **куитевент** получает сигнал или обнаружена ошибка, обработка печати останавливается.</span><span class="sxs-lookup"><span data-stu-id="04507-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
