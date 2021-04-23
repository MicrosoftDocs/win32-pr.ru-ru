---
title: Регистрация обратного вызова COM
description: Вместо опроса изменений в состоянии задания можно выполнить регистрацию, чтобы получить уведомление при изменении состояния задания.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- БИТЫ задания передачи, уведомление о событии
- Регистрация для получения битов уведомления о событиях
- БИТЫ уведомлений о событиях
- БИТЫ уведомлений о событиях, обратные вызовы
- БИТЫ событий уведомления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338220"
---
# <a name="registering-a-com-callback"></a><span data-ttu-id="78636-108">Регистрация обратного вызова COM</span><span class="sxs-lookup"><span data-stu-id="78636-108">Registering a COM Callback</span></span>

<span data-ttu-id="78636-109">Вместо [опроса](polling-for-the-status-of-the-job.md) изменений в состоянии задания можно выполнить регистрацию, чтобы получить уведомление при изменении состояния задания.</span><span class="sxs-lookup"><span data-stu-id="78636-109">Instead of [polling](polling-for-the-status-of-the-job.md) for changes in the status of a job, you can register to receive notification when the job's status changes.</span></span> <span data-ttu-id="78636-110">Чтобы получить уведомление, необходимо реализовать интерфейс [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) .</span><span class="sxs-lookup"><span data-stu-id="78636-110">To receive notification, you must implement the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface.</span></span> <span data-ttu-id="78636-111">Интерфейс содержит следующие методы, которые вызываются BITS в зависимости от регистрации:</span><span class="sxs-lookup"><span data-stu-id="78636-111">The interface contains the following methods that BITS calls, depending on your registration:</span></span>

-   [<span data-ttu-id="78636-112">**жобтрансферред**</span><span class="sxs-lookup"><span data-stu-id="78636-112">**JobTransferred**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [<span data-ttu-id="78636-113">**жоберрор**</span><span class="sxs-lookup"><span data-stu-id="78636-113">**JobError**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [<span data-ttu-id="78636-114">**жобмодификатион**</span><span class="sxs-lookup"><span data-stu-id="78636-114">**JobModification**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [<span data-ttu-id="78636-115">**филетрансферред**</span><span class="sxs-lookup"><span data-stu-id="78636-115">**FileTransferred**</span></span>](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

<span data-ttu-id="78636-116">Пример, в котором реализован интерфейс [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , см. в примере кода в разделе интерфейс [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="78636-116">For an example that implements the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface, see the example code in the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface topic.</span></span>

<span data-ttu-id="78636-117">Интерфейс [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) предоставляет уведомление при передаче файла.</span><span class="sxs-lookup"><span data-stu-id="78636-117">The [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface provides notification when a file is transferred.</span></span> <span data-ttu-id="78636-118">Как правило, этот метод используется для проверки файла, чтобы файл был доступен для загрузки одноранговыми узлами. в противном случае файл недоступен для одноранговых узлов, пока не будет вызван метод [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="78636-118">Typically, you use this method to validate the file, so that the file is available for peers to download; otherwise, the file is not available to peers until you call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="78636-119">Чтобы проверить файл, вызовите метод [**IBackgroundCopyFile3:: сетвалидатионстате**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .</span><span class="sxs-lookup"><span data-stu-id="78636-119">To validate the file, call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method.</span></span>

<span data-ttu-id="78636-120">Существует два метода регистрации обратного вызова COM: регистрация объекта обратного вызова или Регистрация идентификатора класса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="78636-120">There are two methods for registering a COM callback: registering a callback object, or registering a callback class ID.</span></span> <span data-ttu-id="78636-121">Использование объекта обратного вызова упрощается и снижает издержки; Использование CLSID обратного вызова является более надежным, но более сложным.</span><span class="sxs-lookup"><span data-stu-id="78636-121">Using a callback object is simpler and lower overhead; using a callback CLSID is more reliable, but more complicated.</span></span> <span data-ttu-id="78636-122">Вы можете зарегистрировать либо оба, либо ни одного из них, если он существует и по-прежнему будет вызываться, и будет возвращаться к созданию нового объекта на основе указанного идентификатора класса, если это не удается.</span><span class="sxs-lookup"><span data-stu-id="78636-122">You can register either, both, or neither – BITS will use a callback object if one exists and can still be called, and will fall back to instantiating a new object based on a provided class ID if that fails.</span></span>

### <a name="registering-a-callback-object"></a><span data-ttu-id="78636-123">Регистрация объекта обратного вызова</span><span class="sxs-lookup"><span data-stu-id="78636-123">Registering a Callback Object</span></span>

<span data-ttu-id="78636-124">Чтобы зарегистрировать свою реализацию в БИТАХ, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) .</span><span class="sxs-lookup"><span data-stu-id="78636-124">To register your implementation with BITS, call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method.</span></span> <span data-ttu-id="78636-125">Чтобы указать, какие методы BITS вызывают, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).</span><span class="sxs-lookup"><span data-stu-id="78636-125">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)method.</span></span>

<span data-ttu-id="78636-126">Интерфейс уведомления станет недействительным после завершения работы приложения. Служба BITS не сохраняет интерфейс уведомления.</span><span class="sxs-lookup"><span data-stu-id="78636-126">The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface.</span></span> <span data-ttu-id="78636-127">В результате процесс инициализации приложения должен зарегистрировать существующие задания, для которых вы хотите получить уведомление.</span><span class="sxs-lookup"><span data-stu-id="78636-127">As a result, your application's initialization process should register existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="78636-128">Если необходимо собрать сведения о состоянии и ходе выполнения, произошедшие с момента последнего запуска приложения, следует опросить сведения о состоянии и ходе выполнения во время инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="78636-128">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="78636-129">Перед выходом приложение должно очистить указатель интерфейса обратного вызова (**сетнотифинтерфаце (null)**).</span><span class="sxs-lookup"><span data-stu-id="78636-129">Before exiting, your application should clear the callback interface pointer (**SetNotifyInterface(NULL)**).</span></span> <span data-ttu-id="78636-130">Более эффективным является очистка указателя обратного вызова, что позволяет службе BITS обнаружить, что она больше не действительна.</span><span class="sxs-lookup"><span data-stu-id="78636-130">It is more efficient to clear the callback pointer than to let BITS discover that it is no longer valid.</span></span>

<span data-ttu-id="78636-131">Обратите внимание, что если несколько приложений вызывают метод [**сетнотифинтерфаце**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) для установки интерфейса уведомления для задания, Последнее приложение вызывает метод **сетнотифинтерфаце** , который будет получать уведомления — другие приложения не будут получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="78636-131">Note that if more than one application calls the [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to set the notification interface for the job, the last application to call the **SetNotifyInterface** method is the one that will receive notifications—the other applications will not receive notifications.</span></span>

<span data-ttu-id="78636-132">В следующем примере показано, как зарегистрироваться для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="78636-132">The following example shows how to register for notifications.</span></span> <span data-ttu-id="78636-133">В примере предполагается, что указатель интерфейса [**использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) является допустимым.</span><span class="sxs-lookup"><span data-stu-id="78636-133">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span> <span data-ttu-id="78636-134">Дополнительные сведения о классе примера Кнотифинтерфаце, используемом в следующем примере, см. в разделе интерфейс [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="78636-134">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a><span data-ttu-id="78636-135">Регистрация CLSID обратного вызова</span><span class="sxs-lookup"><span data-stu-id="78636-135">Registering a Callback CLSID</span></span>

<span data-ttu-id="78636-136">Чтобы зарегистрировать CLSID обратного вызова с помощью битов, вызовите метод [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) со **\_ \_ свойством \_ \_ задания BITS** PropertyId.</span><span class="sxs-lookup"><span data-stu-id="78636-136">To register a callback CLSID with BITS, call the [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) method with the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** PropertyId.</span></span> <span data-ttu-id="78636-137">Чтобы указать, какие методы BITS вызывают, вызовите метод [**использованием метода ibackgroundcopyjob:: сетнотифифлагс**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .</span><span class="sxs-lookup"><span data-stu-id="78636-137">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method.</span></span>

<span data-ttu-id="78636-138">Перед регистрацией идентификатора CLSID в задании BITS необходимо убедиться, что идентификатор CLSID уведомления зарегистрирован на сервере вне процесса COM.</span><span class="sxs-lookup"><span data-stu-id="78636-138">You must ensure that the notification CLSID is registered to an out-of-process COM server prior to registering the CLSID with a BITS job.</span></span> <span data-ttu-id="78636-139">Реализация [сервера COM](/windows/desktop/com/com-server-responsibilities) значительно сложнее, чем определение и передача объекта обратного вызова, но предлагает несколько важных преимуществ.</span><span class="sxs-lookup"><span data-stu-id="78636-139">Implementing a [COM server](/windows/desktop/com/com-server-responsibilities) is significantly more complicated than defining and passing a callback object, but offers several important advantages.</span></span> <span data-ttu-id="78636-140">Сервер COM позволяет службе BITS поддерживать связь между заданием BITS и кодом приложения при перезагрузке системы, а также для больших или длительных заданий.</span><span class="sxs-lookup"><span data-stu-id="78636-140">A COM server allows BITS to maintain the association between a BITS job and your application’s code across system reboots, and for large or long-lived jobs.</span></span> <span data-ttu-id="78636-141">Сервер COM также позволяет приложению полностью завершить работу, пока служба BITS продолжит выполнять передачи в фоновом режиме, что может улучшить использование аккумулятора, ЦП и памяти системы.</span><span class="sxs-lookup"><span data-stu-id="78636-141">A COM server also allows your application to shut down completely while BITS continues executing transfers in the background, which can improve battery, CPU, and memory usage of the system.</span></span>

<span data-ttu-id="78636-142">Чтобы предоставить уведомление, которое вы зарегистрировали для получения, служба BITS сначала пытается вызвать соответствующий метод существующего объекта обратного вызова, который вы могли присоединить.</span><span class="sxs-lookup"><span data-stu-id="78636-142">To provide a notification you have registered to receive, BITS first attempts to call the corresponding method of any existing callback object you may have attached.</span></span> <span data-ttu-id="78636-143">Если существующего объекта нет или этот существующий объект был отключен (как правило, в результате завершения работы приложения), служба BITS вызовет CoCreateInstance, используя CLSID уведомлений для создания экземпляра нового объекта обратного вызова, и будет использовать этот объект для последующих обратных вызовов до тех пор, пока он не будет отключен или не будет заменен новым вызовом [**использованием метода ibackgroundcopyjob:: сетнотифинтерфаце**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span><span class="sxs-lookup"><span data-stu-id="78636-143">If there is no existing object, or if that existing object has become disconnected (typically as a result of your application terminating), BITS will call CoCreateInstance using the notification CLSID to instantiate a new callback object, and will use that object for any further callbacks until it becomes disconnected or it is replaced by a new call to [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span></span>

<span data-ttu-id="78636-144">В отличие от объектов обратного вызова, CLSID обратного вызова сохраняется вместе с соответствующими заданиями BITS, если служба BITS или система остановлены и перезапущены.</span><span class="sxs-lookup"><span data-stu-id="78636-144">Unlike callback objects, callback CLSID are persisted alongside their corresponding BITS job(s) if the BITS service or the system are shut down and restarted.</span></span> <span data-ttu-id="78636-145">Приложение может очистить любой ранее установленный идентификатор CLSID уведомления перед выходом (или в любой другой момент), передав новый CLSID уведомления GUID \_ null, но ваше приложение может предпочесть оставить идентификатор CLSID уведомления зарегистрированным, если приложение зарегистрировано для запуска com в ответ на запросы CoCreateInstance для идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="78636-145">Your application may clear any previously-set notification CLSID before exiting (or at any other time) by passing a new notification CLSID of GUID\_NULL, but your application may prefer to leave the notification CLSID registered if your application has registered to have COM start it in response to CoCreateInstance requests for your CLSID.</span></span> <span data-ttu-id="78636-146">Обратите внимание, что если в нескольких приложениях задано **свойство \_ \_ \_ \_ CLSID уведомления свойства задания BITS** , то последним задается последний CLSID, который будет использоваться BITS для создания экземпляров объектов обратного вызова — экземпляры других идентификаторов CLSID создаваться не будут.</span><span class="sxs-lookup"><span data-stu-id="78636-146">Note that if more than one application sets the calls the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** property, the last CLSID to be set is the one that BITS will use to instantiate callback objects – the other CLSIDs will not be instantiated.</span></span> <span data-ttu-id="78636-147">Аналогично, если одно приложение регистрирует CLSID и другой регистрирует объект обратного вызова, применяются обычные правила для объекта обратного вызова, которые применяют приоритет, и CLSID не будет использоваться, если объект обратного вызова не был сброшен или отключен.</span><span class="sxs-lookup"><span data-stu-id="78636-147">Similarly, if one application registers a CLSID and another registers a callback object, the usual rules for the callback object taking precedence apply, and the CLSID will not be used unless the callback object is cleared or becomes disconnected.</span></span>

<span data-ttu-id="78636-148">В следующем примере показано, как зарегистрировать уведомления CLSID.</span><span class="sxs-lookup"><span data-stu-id="78636-148">The following example shows how to register for CLSID notifications.</span></span> <span data-ttu-id="78636-149">В примере предполагается, что указатель интерфейса [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) является допустимым и что приложение уже зарегистрировано как внутрипроцессный COM-сервер, реализующий класс кнотифинтерфаце.</span><span class="sxs-lookup"><span data-stu-id="78636-149">The example assumes the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface pointer is valid, and that your application has already registered as an out-of-process COM Server which implements the CNotifyInterface class.</span></span> <span data-ttu-id="78636-150">Дополнительные сведения о классе примера Кнотифинтерфаце, используемом в следующем примере, см. в разделе интерфейс [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="78636-150">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 