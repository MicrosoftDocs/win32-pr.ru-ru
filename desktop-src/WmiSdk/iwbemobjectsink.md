---
description: Интерфейс Ивбемобжектсинк создает интерфейс приемника, который может получать все типы уведомлений в модели программирования WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Интерфейс Ивбемобжектсинк (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683217"
---
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="4b061-103">Интерфейс Ивбемобжектсинк</span><span class="sxs-lookup"><span data-stu-id="4b061-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="4b061-104">Интерфейс **ивбемобжектсинк** создает интерфейс приемника, который может получать все типы уведомлений в модели программирования WMI.</span><span class="sxs-lookup"><span data-stu-id="4b061-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="4b061-105">Клиенты должны реализовать этот интерфейс для получения результатов [асинхронных методов](making-an-asynchronous-call-with-c--.md) [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)и конкретных типов уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="4b061-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="4b061-106">Поставщики используют, но не реализуют этот интерфейс для предоставления событий и объектов WMI.</span><span class="sxs-lookup"><span data-stu-id="4b061-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="4b061-107">Как правило, поставщики вызывают реализацию, предоставляемую WMI.</span><span class="sxs-lookup"><span data-stu-id="4b061-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="4b061-108">В этих случаях вызовите метод [**указания**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) для предоставления объектов службе WMI.</span><span class="sxs-lookup"><span data-stu-id="4b061-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="4b061-109">После этого вызовите [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , чтобы обозначить конец последовательности уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4b061-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="4b061-110">Кроме того, можно вызвать **SetStatus** , чтобы указать ошибки, когда у приемника нет объектов.</span><span class="sxs-lookup"><span data-stu-id="4b061-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="4b061-111">При программировании асинхронных клиентов WMI пользователь предоставляет реализацию.</span><span class="sxs-lookup"><span data-stu-id="4b061-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="4b061-112">Инструментарий WMI вызывает методы для доставки объектов и установки состояния результата.</span><span class="sxs-lookup"><span data-stu-id="4b061-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="4b061-113">Если клиентское приложение передает один и тот же интерфейс приемника в два разных перекрывающихся асинхронных вызова, WMI не гарантирует порядок обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4b061-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="4b061-114">Клиентские приложения, которые делают перекрывающиеся асинхронные вызовы, должны либо передавать разные объекты-приемник, либо выполнять сериализацию своих вызовов.</span><span class="sxs-lookup"><span data-stu-id="4b061-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b061-115">Поскольку обратный вызов к приемнику может быть не возвращен на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="4b061-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="4b061-116">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4b061-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="4b061-117">Элементы</span><span class="sxs-lookup"><span data-stu-id="4b061-117">Members</span></span>

<span data-ttu-id="4b061-118">Интерфейс **ивбемобжектсинк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b061-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="4b061-119">Методы</span><span class="sxs-lookup"><span data-stu-id="4b061-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b061-120">Методы</span><span class="sxs-lookup"><span data-stu-id="4b061-120">Methods</span></span>

<span data-ttu-id="4b061-121">Интерфейс **ивбемобжектсинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4b061-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="4b061-122">Метод</span><span class="sxs-lookup"><span data-stu-id="4b061-122">Method</span></span>                                         | <span data-ttu-id="4b061-123">Описание</span><span class="sxs-lookup"><span data-stu-id="4b061-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b061-124">**Казывая**</span><span class="sxs-lookup"><span data-stu-id="4b061-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="4b061-125">Получает объекты уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4b061-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="4b061-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="4b061-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="4b061-127">Вызывается источниками для обозначения конца последовательности уведомлений или для отправки приемнику других кодов состояния.</span><span class="sxs-lookup"><span data-stu-id="4b061-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b061-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b061-128">Remarks</span></span>

<span data-ttu-id="4b061-129">При реализации приемника подписки на события (**ивбемобжектсинк** или [**ивбемевентсинк**](iwbemeventsink.md)) не следует вызывать WMI из методов [**указания**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) или [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="4b061-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="4b061-130">Например, вызов [**IWbemServices:: канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) для отмены приемника из реализации [**индикации**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) может повлиять на состояние WMI.</span><span class="sxs-lookup"><span data-stu-id="4b061-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="4b061-131">Чтобы отменить подписку на события, установите флаг и вызовите **IWbemServices:: канцеласинккалл** из другого потока или объекта.</span><span class="sxs-lookup"><span data-stu-id="4b061-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="4b061-132">Для реализаций, которые не связаны с приемником событий, например объектом, перечислением и получением запросов, можно выполнить обратный вызов к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="4b061-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="4b061-133">Реализации приемника должны обрабатывать уведомление о событии в течение 100 мс, поскольку поток WMI, доставляющий уведомление о событии, не может выполнить другие действия, пока объект приемника не завершит обработку.</span><span class="sxs-lookup"><span data-stu-id="4b061-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="4b061-134">Если для уведомления требуется большой объем обработки, приемник может использовать внутреннюю очередь для другого потока, чтобы обработать обработку.</span><span class="sxs-lookup"><span data-stu-id="4b061-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="4b061-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="4b061-135">Examples</span></span>

<span data-ttu-id="4b061-136">Следующий пример кода является простой реализацией приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="4b061-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="4b061-137">Этот пример можно использовать с [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) для получения возвращенных экземпляров:</span><span class="sxs-lookup"><span data-stu-id="4b061-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a><span data-ttu-id="4b061-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4b061-138">Requirements</span></span>



| <span data-ttu-id="4b061-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4b061-139">Requirement</span></span> | <span data-ttu-id="4b061-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4b061-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b061-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b061-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4b061-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b061-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="4b061-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b061-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4b061-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b061-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="4b061-145">Header</span><span class="sxs-lookup"><span data-stu-id="4b061-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b061-146"><dt>Вбемкли. h (включение Вбемидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b061-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="4b061-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b061-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b061-148"><dt>Вбемууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b061-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="4b061-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4b061-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b061-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b061-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="4b061-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b061-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b061-152">COM API для WMI</span><span class="sxs-lookup"><span data-stu-id="4b061-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="4b061-153">Создание асинхронного вызова с помощью C++</span><span class="sxs-lookup"><span data-stu-id="4b061-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="4b061-154">Настройка безопасности при асинхронном вызове</span><span class="sxs-lookup"><span data-stu-id="4b061-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="4b061-155">Получение событий для длительности вашего приложения</span><span class="sxs-lookup"><span data-stu-id="4b061-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




