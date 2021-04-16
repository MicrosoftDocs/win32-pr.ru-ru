---
description: Приложения WMI, написанные на C++, могут выполнять асинхронные вызовы с помощью многих методов интерфейса IWbemServices COM.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Создание асинхронного вызова с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713033"
---
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="81f5d-103">Создание асинхронного вызова с помощью C++</span><span class="sxs-lookup"><span data-stu-id="81f5d-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="81f5d-104">Приложения WMI, написанные на C++, могут выполнять асинхронные вызовы с помощью многих методов интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) com.</span><span class="sxs-lookup"><span data-stu-id="81f5d-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="81f5d-105">Однако Рекомендуемая процедура вызова [*метода WMI*](gloss-w.md) или [*метода поставщика*](gloss-p.md) заключается в использовании вызовов семисинчронаус, так как вызовы семисинчронаус более безопасны, чем асинхронные вызовы.</span><span class="sxs-lookup"><span data-stu-id="81f5d-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="81f5d-106">Дополнительные сведения см. в статьях [выполнение вызова семисинчронаус с помощью C++](making-a-semisynchronous-call-with-c--.md) и [Настройка безопасности для асинхронного вызова](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="81f5d-107">Следующая процедура описывает, как выполнить асинхронный вызов с помощью приемника в процессе.</span><span class="sxs-lookup"><span data-stu-id="81f5d-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="81f5d-108">**Выполнение асинхронного вызова с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="81f5d-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="81f5d-109">Реализуйте интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="81f5d-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="81f5d-110">Все приложения, которые выполняют асинхронные вызовы, должны реализовывать [**ивбемобжектсинк**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="81f5d-111">Для получения уведомлений о событиях временные потребители событий также реализуют **ивбемобжектсинк** .</span><span class="sxs-lookup"><span data-stu-id="81f5d-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="81f5d-112">Войдите в целевое пространство имен WMI.</span><span class="sxs-lookup"><span data-stu-id="81f5d-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="81f5d-113">Приложениям всегда приходится вызывать COM-функцию [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) на этапе инициализации.</span><span class="sxs-lookup"><span data-stu-id="81f5d-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="81f5d-114">Если это не сделано до выполнения асинхронного вызова, WMI освобождает приемник приложения, не завершая асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="81f5d-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="81f5d-115">Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="81f5d-116">Настройте безопасность для приемника.</span><span class="sxs-lookup"><span data-stu-id="81f5d-116">Set the security for your sink.</span></span>

    <span data-ttu-id="81f5d-117">Асинхронные вызовы создают множество проблем безопасности, с которыми может потребоваться работать, например, обеспечивая доступ WMI к приложению.</span><span class="sxs-lookup"><span data-stu-id="81f5d-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="81f5d-118">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="81f5d-119">Выполните асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="81f5d-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="81f5d-120">Метод немедленно возвращает код **\_ ошибки WBEM \_ без \_ ошибок** .</span><span class="sxs-lookup"><span data-stu-id="81f5d-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="81f5d-121">Приложение может продолжить работу с другими задачами, ожидая завершения операции.</span><span class="sxs-lookup"><span data-stu-id="81f5d-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="81f5d-122">Инструментарий WMI сообщает в приложении, вызывая методы в реализации [**ивбемобжектсинк**](iwbemobjectsink.md) приложения.</span><span class="sxs-lookup"><span data-stu-id="81f5d-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="81f5d-123">При необходимости периодически проверяйте свою реализацию на наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="81f5d-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="81f5d-124">Приложения могут получать уведомления о промежуточном состоянии путем установки параметра *лфлагс* в асинхронном вызове **\_ флага WBEM " \_ \_ Состояние отправки**".</span><span class="sxs-lookup"><span data-stu-id="81f5d-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="81f5d-125">Инструментарий WMI сообщает о состоянии вызова, присвоив  параметру лфлагс [**ивбемобжектсинк**](iwbemobjectsink.md) значение **\_ \_ Progress Status**.</span><span class="sxs-lookup"><span data-stu-id="81f5d-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="81f5d-126">При необходимости можно отменить вызов до завершения обработки WMI, вызвав метод [**IWbemServices:: канцелкалласинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="81f5d-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="81f5d-127">Метод [**канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) отменяет асинхронную обработку, немедленно освобождая указатель на интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) и гарантирует, что указатель освобождается перед возвратом **канцеласинккалл** .</span><span class="sxs-lookup"><span data-stu-id="81f5d-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="81f5d-128">Если вы используете объект-оболочку, реализующий интерфейс **иунсекуред** для размещения [**ивбемобжектсинк**](iwbemobjectsink.md), может оказаться, что некоторые дополнительные сложности.</span><span class="sxs-lookup"><span data-stu-id="81f5d-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="81f5d-129">Так как приложение должно передавать тот же указатель на [**канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) , который был передан в исходном асинхронном вызове, приложение должно храниться на объекте-оболочке до тех пор, пока не станет ясно, что отмена не требуется.</span><span class="sxs-lookup"><span data-stu-id="81f5d-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="81f5d-130">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="81f5d-131">По завершении очистите указатели и завершите работу приложения.</span><span class="sxs-lookup"><span data-stu-id="81f5d-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="81f5d-132">Инструментарий WMI предоставляет окончательный вызов состояния с помощью метода [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="81f5d-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="81f5d-133">После отправки окончательного обновления состояния WMI освобождает приемник объекта, вызывая метод **Release** для класса, реализующего интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="81f5d-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="81f5d-134">В предыдущем примере это метод **куерисинк:: Release** .</span><span class="sxs-lookup"><span data-stu-id="81f5d-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="81f5d-135">Если вы хотите контролировать время существования объекта приемника, можно реализовать приемник с начальным счетчиком ссылок, равным единице (1).</span><span class="sxs-lookup"><span data-stu-id="81f5d-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="81f5d-136">Если клиентское приложение передает один и тот же интерфейс приемника в два разных перекрывающихся асинхронных вызова, WMI не гарантирует порядок обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="81f5d-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="81f5d-137">Клиентское приложение, выполняющее перекрывающиеся асинхронные вызовы, должно либо передавать разные объекты-приемники, либо выполнять сериализацию вызовов.</span><span class="sxs-lookup"><span data-stu-id="81f5d-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="81f5d-138">В следующем примере требуются следующие инструкции Reference и \# include.</span><span class="sxs-lookup"><span data-stu-id="81f5d-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="81f5d-139">В следующем примере показано, как выполнить асинхронный запрос с помощью метода [**ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , но не создать параметры безопасности или освободить объект [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="81f5d-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="81f5d-140">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> <span data-ttu-id="81f5d-141">Приведенный выше код не компилируется без ошибок, так как класс **куерисинк** не определен.</span><span class="sxs-lookup"><span data-stu-id="81f5d-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="81f5d-142">Дополнительные сведения о **куерисинк** см. в разделе [**ивбемобжектсинк**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="81f5d-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="81f5d-143">См. также</span><span class="sxs-lookup"><span data-stu-id="81f5d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81f5d-144">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="81f5d-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
