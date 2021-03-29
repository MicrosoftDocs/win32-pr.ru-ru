---
description: Класс Камсреад является абстрактным классом для управления рабочими потоками.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Класс Камсреад (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665479"
---
# <a name="camthread-class"></a><span data-ttu-id="ba28d-103">Класс Камсреад</span><span class="sxs-lookup"><span data-stu-id="ba28d-103">CAMThread class</span></span>

<span data-ttu-id="ba28d-104">`CAMThread`Класс является абстрактным классом для управления рабочими потоками.</span><span class="sxs-lookup"><span data-stu-id="ba28d-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="ba28d-105">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="ba28d-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="ba28d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ba28d-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="ba28d-107">**m \_ хсреад**</span><span class="sxs-lookup"><span data-stu-id="ba28d-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="ba28d-108">Обработчик для потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="ba28d-109">Открытые переменные члена</span><span class="sxs-lookup"><span data-stu-id="ba28d-109">Public Member Variables</span></span>                                    | <span data-ttu-id="ba28d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ba28d-110">Description</span></span>                                                                  |
| [<span data-ttu-id="ba28d-111">**m \_ акцесслокк**</span><span class="sxs-lookup"><span data-stu-id="ba28d-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="ba28d-112">Критическая секция, которая блокирует доступ к потоку из других потоков.</span><span class="sxs-lookup"><span data-stu-id="ba28d-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="ba28d-113">**m \_ воркерлокк**</span><span class="sxs-lookup"><span data-stu-id="ba28d-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="ba28d-114">Критическая секция, которая блокирует данные, общие для потоков.</span><span class="sxs-lookup"><span data-stu-id="ba28d-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="ba28d-115">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="ba28d-115">Public Methods</span></span>                                             | <span data-ttu-id="ba28d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ba28d-116">Description</span></span>                                                                  |
| [<span data-ttu-id="ba28d-117">**камсреад**</span><span class="sxs-lookup"><span data-stu-id="ba28d-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="ba28d-118">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="ba28d-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="ba28d-119">**~ Камсреад**</span><span class="sxs-lookup"><span data-stu-id="ba28d-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="ba28d-120">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="ba28d-120">Destructor method.</span></span> <span data-ttu-id="ba28d-121">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="ba28d-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="ba28d-122">**инитиалсреадпрок**</span><span class="sxs-lookup"><span data-stu-id="ba28d-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="ba28d-123">Вызывает метод Среадпрок при создании потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="ba28d-124">**Создать**</span><span class="sxs-lookup"><span data-stu-id="ba28d-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="ba28d-125">Создает поток.</span><span class="sxs-lookup"><span data-stu-id="ba28d-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="ba28d-126">**каллворкер**</span><span class="sxs-lookup"><span data-stu-id="ba28d-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="ba28d-127">Сигнализирует потоку запрос.</span><span class="sxs-lookup"><span data-stu-id="ba28d-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="ba28d-128">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="ba28d-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="ba28d-129">Ожидает завершения работы потока, а затем освобождает его ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ba28d-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="ba28d-130">**среадексистс**</span><span class="sxs-lookup"><span data-stu-id="ba28d-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="ba28d-131">Запрашивает, существует ли поток.</span><span class="sxs-lookup"><span data-stu-id="ba28d-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="ba28d-132">**Запрос на**</span><span class="sxs-lookup"><span data-stu-id="ba28d-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="ba28d-133">Ожидает следующего запроса.</span><span class="sxs-lookup"><span data-stu-id="ba28d-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="ba28d-134">**чеккрекуест**</span><span class="sxs-lookup"><span data-stu-id="ba28d-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="ba28d-135">Проверяет, есть ли запрос, без блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba28d-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="ba28d-136">**Ответить**</span><span class="sxs-lookup"><span data-stu-id="ba28d-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="ba28d-137">Ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="ba28d-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="ba28d-138">**жетрекуессандле**</span><span class="sxs-lookup"><span data-stu-id="ba28d-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="ba28d-139">Извлекает дескриптор события, сигнального методом Каллворкер.</span><span class="sxs-lookup"><span data-stu-id="ba28d-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="ba28d-140">**жетрекуестпарам**</span><span class="sxs-lookup"><span data-stu-id="ba28d-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="ba28d-141">Извлекает последний запрос.</span><span class="sxs-lookup"><span data-stu-id="ba28d-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="ba28d-142">**коинитиализехелпер**</span><span class="sxs-lookup"><span data-stu-id="ba28d-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="ba28d-143">Вызывает CoInitializeEx в начале потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="ba28d-144">Чистые виртуальные методы</span><span class="sxs-lookup"><span data-stu-id="ba28d-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="ba28d-145">Описание</span><span class="sxs-lookup"><span data-stu-id="ba28d-145">Description</span></span>                                                                  |
| [<span data-ttu-id="ba28d-146">**среадпрок**</span><span class="sxs-lookup"><span data-stu-id="ba28d-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="ba28d-147">Потоковая процедура.</span><span class="sxs-lookup"><span data-stu-id="ba28d-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ba28d-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba28d-148">Remarks</span></span>

<span data-ttu-id="ba28d-149">Этот класс предоставляет методы для создания рабочего потока, передачи запросов в поток и ожидания выхода из потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="ba28d-150">Чтобы использовать этот класс, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ba28d-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="ba28d-151">Создайте класс, производный от класса `CAMThread` , и переопределите чистый виртуальный метод [**камсреад:: среадпрок**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="ba28d-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="ba28d-152">Этот метод является процедурой потока, которая вызывается в начале потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="ba28d-153">В приложении создайте экземпляр производного класса.</span><span class="sxs-lookup"><span data-stu-id="ba28d-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="ba28d-154">Создание объекта не приводит к созданию потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="ba28d-155">Чтобы создать поток, вызовите метод [**камсреад:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="ba28d-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="ba28d-156">Чтобы отправить запросы в поток, вызовите метод [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="ba28d-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="ba28d-157">Этот метод принимает параметр DWORD, значение которого определяется вашим классом.</span><span class="sxs-lookup"><span data-stu-id="ba28d-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="ba28d-158">Метод блокируется до тех пор, пока поток не ответит (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="ba28d-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="ba28d-159">В потоковой процедуре отвечайте на запросы, вызывая либо [**камсреад:: WebRequest**](camthread-getrequest.md) , либо [**Камсреад:: чеккрекуест**](camthread-checkrequest.md).</span><span class="sxs-lookup"><span data-stu-id="ba28d-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="ba28d-160">Метод WebRequest блокируется до тех пор, пока другой поток не вызовет Каллворкер.</span><span class="sxs-lookup"><span data-stu-id="ba28d-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="ba28d-161">Метод Чеккрекуест не блокируется, что позволяет потоку проверять наличие новых запросов при асинхронной работе.</span><span class="sxs-lookup"><span data-stu-id="ba28d-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="ba28d-162">Когда поток получает запрос, вызовите [**камсреад:: Reply**](camthread-reply.md) , чтобы разблокировать вызывающий поток.</span><span class="sxs-lookup"><span data-stu-id="ba28d-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="ba28d-163">Метод Reply принимает параметр DWORD, который передается в вызывающий поток в качестве возвращаемого значения для Каллворкер.</span><span class="sxs-lookup"><span data-stu-id="ba28d-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="ba28d-164">Завершив работу с потоком, вызовите метод [**камсреад:: Close**](camthread-close.md) .</span><span class="sxs-lookup"><span data-stu-id="ba28d-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="ba28d-165">Этот метод ожидает выхода из потока, а затем закрывает обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="ba28d-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="ba28d-166">Сообщение Среадпрок должно быть гарантированно закрыто самостоятельно или в ответ на запрос Каллворкер.</span><span class="sxs-lookup"><span data-stu-id="ba28d-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="ba28d-167">Метод деструктора также вызывает Close.</span><span class="sxs-lookup"><span data-stu-id="ba28d-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="ba28d-168">В следующем примере показаны эти действия.</span><span class="sxs-lookup"><span data-stu-id="ba28d-168">The following example illustrates these steps:</span></span>


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



<span data-ttu-id="ba28d-169">В производном классе можно также определить функции элементов, которые проверяют параметры на Каллворкер.</span><span class="sxs-lookup"><span data-stu-id="ba28d-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="ba28d-170">В следующем примере показан типичный способ этого:</span><span class="sxs-lookup"><span data-stu-id="ba28d-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="ba28d-171">`CAMThread`Класс предоставляет два критических раздела в виде общих переменных члена.</span><span class="sxs-lookup"><span data-stu-id="ba28d-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="ba28d-172">Используйте `CAMThread::m_AccessLock` , чтобы заблокировать поток от доступа других потоков.</span><span class="sxs-lookup"><span data-stu-id="ba28d-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="ba28d-173">(Например, методы Create и Каллворкер хранят эту блокировку для сериализации операций в потоке.) Используйте [**камсреад:: m \_ воркерлокк**](camthread-m-workerlock.md) для блокировки данных, которые являются общими для потоков.</span><span class="sxs-lookup"><span data-stu-id="ba28d-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba28d-174">Требования</span><span class="sxs-lookup"><span data-stu-id="ba28d-174">Requirements</span></span>



| <span data-ttu-id="ba28d-175">Требование</span><span class="sxs-lookup"><span data-stu-id="ba28d-175">Requirement</span></span> | <span data-ttu-id="ba28d-176">Значение</span><span class="sxs-lookup"><span data-stu-id="ba28d-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba28d-177">Header</span><span class="sxs-lookup"><span data-stu-id="ba28d-177">Header</span></span><br/>  | <dl> <span data-ttu-id="ba28d-178"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba28d-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ba28d-179">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba28d-179">Library</span></span><br/> | <dl> <span data-ttu-id="ba28d-180"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ba28d-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




