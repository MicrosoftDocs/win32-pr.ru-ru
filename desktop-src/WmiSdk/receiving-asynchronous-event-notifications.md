---
description: Асинхронное уведомление о событиях — это метод, позволяющий приложению постоянно отслеживать события без монопольного применения системных ресурсов.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Получение уведомлений о асинхронных событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647476"
---
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="96dac-103">Получение уведомлений о асинхронных событиях</span><span class="sxs-lookup"><span data-stu-id="96dac-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="96dac-104">Асинхронное уведомление о событиях — это метод, позволяющий приложению постоянно отслеживать события без монопольного применения системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96dac-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="96dac-105">Асинхронные уведомления о событиях имеют те же ограничения безопасности, что и другие асинхронные вызовы.</span><span class="sxs-lookup"><span data-stu-id="96dac-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="96dac-106">Вместо этого можно выполнять вызовы семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="96dac-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="96dac-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="96dac-108">Очередь асинхронных событий, направляемых клиенту, имеет потенциал для увеличения исключительно большого объема.</span><span class="sxs-lookup"><span data-stu-id="96dac-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="96dac-109">Поэтому Инструментарий WMI реализует политику на уровне системы, чтобы избежать нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="96dac-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="96dac-110">WMI либо замедляет события, либо начинает удалять события из очереди, когда очередь растет до определенного размера.</span><span class="sxs-lookup"><span data-stu-id="96dac-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="96dac-111">Инструментарий WMI использует свойства [**ловсрешолдоневентс**](/windows/desktop/CIMWin32Prov/win32-wmisetting) и [**хигхсрешолдоневентс**](/windows/desktop/CIMWin32Prov/win32-wmisetting) класса [**Win32 \_ вмисеттинг**](/windows/desktop/CIMWin32Prov/win32-wmisetting) , чтобы задать ограничения для предотвращения нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="96dac-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="96dac-112">Минимальное значение указывает, когда инструментарий WMI должен запустить задолгое уведомление о событии, а максимальное значение указывает, когда следует запускать удаление событий.</span><span class="sxs-lookup"><span data-stu-id="96dac-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="96dac-113">Значения по умолчанию для нижнего и верхнего пороговых значений — 1000000 (10 МБ) и 2000000 (20 МБ).</span><span class="sxs-lookup"><span data-stu-id="96dac-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="96dac-114">Кроме того, можно задать свойство [**максваитоневентс**](/windows/desktop/CIMWin32Prov/win32-wmisetting) , чтобы описать период времени, в течение которого WMI должен ожидать перед удалением событий.</span><span class="sxs-lookup"><span data-stu-id="96dac-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="96dac-115">Значение по умолчанию для **максваитоневентс** — 2000, или 2 секунды.</span><span class="sxs-lookup"><span data-stu-id="96dac-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="96dac-116">Получение асинхронных уведомлений о событиях в VBScript</span><span class="sxs-lookup"><span data-stu-id="96dac-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="96dac-117">Вызовы сценариев для получения уведомлений о событиях, по сути, одинаковы для всех асинхронных вызовов с теми же проблемами безопасности.</span><span class="sxs-lookup"><span data-stu-id="96dac-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="96dac-118">Дополнительные сведения см. в разделе [выполнение асинхронного вызова с помощью VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="96dac-119">**Получение асинхронных уведомлений о событиях в VBScript**</span><span class="sxs-lookup"><span data-stu-id="96dac-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="96dac-120">Создайте объект приемника, вызвав [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) и указав ProgID "вбемскриптинг" и тип объекта [**свбемсинк**](swbemsink.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="96dac-121">Объект приемника получает уведомления.</span><span class="sxs-lookup"><span data-stu-id="96dac-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="96dac-122">Напишите подпрограммы для каждого события, которое необходимо обменять.</span><span class="sxs-lookup"><span data-stu-id="96dac-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="96dac-123">В следующей таблице перечислены события [**свбемсинк**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="96dac-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="96dac-124">Событие</span><span class="sxs-lookup"><span data-stu-id="96dac-124">Event</span></span>                                            | <span data-ttu-id="96dac-125">Значение</span><span class="sxs-lookup"><span data-stu-id="96dac-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="96dac-126">**онобжектреади**</span><span class="sxs-lookup"><span data-stu-id="96dac-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="96dac-127">Сообщает о возвратах объекта в приемник.</span><span class="sxs-lookup"><span data-stu-id="96dac-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="96dac-128">Использование этого вызова возвращает один объект каждый раз, пока операция не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="96dac-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="96dac-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="96dac-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="96dac-130">Сообщает о завершении асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="96dac-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="96dac-131">Это событие никогда не происходит, если операция является неопределенной.</span><span class="sxs-lookup"><span data-stu-id="96dac-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="96dac-132">**онобжектпут**</span><span class="sxs-lookup"><span data-stu-id="96dac-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="96dac-133">Сообщает о завершении асинхронной операции размещения.</span><span class="sxs-lookup"><span data-stu-id="96dac-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="96dac-134">Это событие возвращает путь к объекту экземпляра или сохраненного класса.</span><span class="sxs-lookup"><span data-stu-id="96dac-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="96dac-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="96dac-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="96dac-136">Сообщает состояние выполняемого асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="96dac-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="96dac-137">Не все поставщики поддерживают промежуточные отчеты о состоянии.</span><span class="sxs-lookup"><span data-stu-id="96dac-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="96dac-138">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="96dac-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="96dac-139">Отменяет все необработанные асинхронные операции, связанные с этим приемником объектов.</span><span class="sxs-lookup"><span data-stu-id="96dac-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="96dac-140">Следующий пример кода VBScript уведомляет об удалении процессов с интервалом опроса 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="96dac-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="96dac-141">В этом скрипте онобжектреади ПРИЕМНИКа подпрограммы \_ обрабатывает экземпляр события.</span><span class="sxs-lookup"><span data-stu-id="96dac-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="96dac-142">В этом примере объект приемника называется "Sink", однако этот объект можно назвать по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="96dac-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="96dac-143">Получение уведомлений о асинхронных событиях в C++</span><span class="sxs-lookup"><span data-stu-id="96dac-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="96dac-144">Для выполнения асинхронного уведомления создается отдельный поток только для отслеживания и получения событий от инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="96dac-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="96dac-145">Когда этот поток получает сообщение, поток уведомляет ваше основное приложение.</span><span class="sxs-lookup"><span data-stu-id="96dac-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="96dac-146">Нажимая отдельный поток, вы разрешаете основному процессу выполнять другие действия, ожидая прибытия события.</span><span class="sxs-lookup"><span data-stu-id="96dac-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="96dac-147">Асинхронная доставка уведомлений повышает производительность, но может обеспечить меньшую безопасность, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="96dac-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="96dac-148">В C++ имеется возможность использовать интерфейс [**ивбемунсекуредапартмент**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) или выполнять проверки доступа в дескрипторах безопасности.</span><span class="sxs-lookup"><span data-stu-id="96dac-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="96dac-149">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="96dac-150">**Настройка уведомлений о асинхронных событиях**</span><span class="sxs-lookup"><span data-stu-id="96dac-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="96dac-151">Перед инициализацией каких-либо асинхронных уведомлений убедитесь, что параметры предотвращения нехватки памяти правильно заданы в [**Win32 \_ вмисеттинг**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span><span class="sxs-lookup"><span data-stu-id="96dac-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="96dac-152">Определите тип событий, которые вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="96dac-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="96dac-153">Инструментарий WMI поддерживает внутренние и внешние события.</span><span class="sxs-lookup"><span data-stu-id="96dac-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="96dac-154">Внутреннее событие — это событие, предопределенное WMI, в то время как внешнее событие является событием, определенным сторонним поставщиком.</span><span class="sxs-lookup"><span data-stu-id="96dac-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="96dac-155">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="96dac-156">В следующей процедуре описывается получение асинхронных уведомлений о событиях в C++.</span><span class="sxs-lookup"><span data-stu-id="96dac-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="96dac-157">**Получение асинхронных уведомлений о событиях в C++**</span><span class="sxs-lookup"><span data-stu-id="96dac-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="96dac-158">Настройте приложение с помощью вызовов функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="96dac-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="96dac-159">Вызов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) инициализирует COM, а [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) предоставляет WMI разрешение на вызов процесса потребителя.</span><span class="sxs-lookup"><span data-stu-id="96dac-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="96dac-160">Функция **CoInitializeEx** также предоставляет возможность программировать многопоточное приложение, необходимое для асинхронного уведомления.</span><span class="sxs-lookup"><span data-stu-id="96dac-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="96dac-161">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="96dac-162">Для правильной компиляции кода в этом разделе необходимы следующие ссылки и \# операторы include.</span><span class="sxs-lookup"><span data-stu-id="96dac-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="96dac-163">В следующем примере кода показано, как настроить временный потребитель событий с помощью вызовов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="96dac-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  <span data-ttu-id="96dac-164">Создайте объект приемника с помощью интерфейса [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="96dac-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="96dac-165">Инструментарий WMI использует [**ивбемобжектсинк**](iwbemobjectsink.md) для отправки уведомлений о событиях и для сообщения о состоянии асинхронной операции или уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="96dac-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="96dac-166">Зарегистрируйте потребителя событий с помощью вызова метода [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="96dac-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="96dac-167">Убедитесь, что параметр *преспонсехандлер* указывает на объект приемника, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="96dac-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="96dac-168">Назначение регистрации — получение только необходимых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="96dac-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="96dac-169">Получение избыточных уведомлений тратит время на обработку и доставку; и не использует возможности фильтрации WMI с максимальной вероятностью.</span><span class="sxs-lookup"><span data-stu-id="96dac-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="96dac-170">Однако временный потребитель может получить более одного типа события.</span><span class="sxs-lookup"><span data-stu-id="96dac-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="96dac-171">В этом случае временный потребитель должен выполнить отдельные вызовы [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) для каждого типа событий.</span><span class="sxs-lookup"><span data-stu-id="96dac-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="96dac-172">Например, потребителю может требоваться уведомление при создании новых процессов (событие создания экземпляра или [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)), а также об изменениях в некоторых разделах реестра (событие реестра, например [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span><span class="sxs-lookup"><span data-stu-id="96dac-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="96dac-173">Таким образом, потребитель выполняет один вызов [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) для регистрации событий создания экземпляра и другой вызов **ExecNotificationQueryAsync** для регистрации событий реестра.</span><span class="sxs-lookup"><span data-stu-id="96dac-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="96dac-174">Если вы решили создать потребитель событий, регистрирующий несколько событий, следует избегать регистрации нескольких классов с одним и тем же приемником.</span><span class="sxs-lookup"><span data-stu-id="96dac-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="96dac-175">Вместо этого используйте отдельный приемник для каждого класса зарегистрированного события.</span><span class="sxs-lookup"><span data-stu-id="96dac-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="96dac-176">Наличие выделенного приемника упрощает обработку и помогает в обслуживании, позволяя отменить одну регистрацию, не затрагивая другие.</span><span class="sxs-lookup"><span data-stu-id="96dac-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="96dac-177">Выполните все необходимые действия в потребителе события.</span><span class="sxs-lookup"><span data-stu-id="96dac-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="96dac-178">Этот шаг должен содержать большую часть кода и включать такие действия, как отображение событий в пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="96dac-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="96dac-179">По завершении отмените регистрацию временного потребителя событий, вызвав событие [**IWbemServices:: канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="96dac-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="96dac-180">Независимо от того, завершился ли вызов [**канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) успешно или нет, не удаляйте объект приемника до тех пор, пока значение счетчика ссылок на объект не достигнет нуля.</span><span class="sxs-lookup"><span data-stu-id="96dac-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="96dac-181">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="96dac-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
