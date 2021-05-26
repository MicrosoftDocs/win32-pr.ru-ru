---
description: Асинхронный вызов методов службы
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Асинхронный вызов методов службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423854"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="1442b-103">Асинхронный вызов методов службы</span><span class="sxs-lookup"><span data-stu-id="1442b-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="1442b-104">Приложение Впдсервицеаписампле содержит код, демонстрирующий, как приложение может асинхронно вызывать методы службы.</span><span class="sxs-lookup"><span data-stu-id="1442b-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="1442b-105">В этом образце используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1442b-105">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="1442b-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1442b-106">Interface</span></span>    | <span data-ttu-id="1442b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1442b-107">Description</span></span>          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1442b-108">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="1442b-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="1442b-109">Используется для получения интерфейса **ипортабледевицесервицемесодс** для вызова методов в заданной службе.</span><span class="sxs-lookup"><span data-stu-id="1442b-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="1442b-110">**ипортабледевицесервицемесодс**</span><span class="sxs-lookup"><span data-stu-id="1442b-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="1442b-111">Используется для вызова метода службы.</span><span class="sxs-lookup"><span data-stu-id="1442b-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="1442b-112">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="1442b-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="1442b-113">Используется для хранения параметров исходящего метода и результатов входящего метода.</span><span class="sxs-lookup"><span data-stu-id="1442b-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="1442b-114">Может иметь **значение NULL** , если метод не требует никаких параметров или не возвращает никаких результатов.</span><span class="sxs-lookup"><span data-stu-id="1442b-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="1442b-115">**ипортабледевицесервицемесодкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1442b-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="1442b-116">Реализуется приложением для получения результатов метода после завершения метода.</span><span class="sxs-lookup"><span data-stu-id="1442b-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="1442b-117">Когда пользователь выбирает в командной строке параметр "10", приложение вызывает метод **инвокемесодсасинк** , который находится в модуле сервицемесодс. cpp.</span><span class="sxs-lookup"><span data-stu-id="1442b-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="1442b-118">Обратите внимание, что до вызова методов пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="1442b-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="1442b-119">Методы службы инкапсулируют функциональные возможности, определяемые и реализуемые каждой службой.</span><span class="sxs-lookup"><span data-stu-id="1442b-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="1442b-120">Они уникальны для каждого типа службы и представлены идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="1442b-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="1442b-121">Например, служба Contacts определяет метод **бегинсинк** , который вызывается приложениями для подготовки устройства к синхронизации объектов Contact, и метод **ендсинк** для уведомления устройства о завершении синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1442b-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="1442b-122">Приложения выполняют метод службы переносимых устройств путем вызова [**ипортабледевицесервицемесодс:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="1442b-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="1442b-123">Методы службы не следует путать с командами WPD.</span><span class="sxs-lookup"><span data-stu-id="1442b-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="1442b-124">Команды WPD являются частью стандартного интерфейса драйвера устройства WPD (DDI) и являются механизмом обмена данными между приложением WPD и драйвером.</span><span class="sxs-lookup"><span data-stu-id="1442b-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="1442b-125">Команды являются предопределенными, сгруппированные по категориям (например, **\_ категории WPD \_ Common**), и представляются структурой **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="1442b-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="1442b-126">Приложение отправляет команды драйверу устройства, вызывая [**ипортабледевицесервице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="1442b-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="1442b-127">Дополнительные сведения см. в разделе команды.</span><span class="sxs-lookup"><span data-stu-id="1442b-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="1442b-128">Метод **инвокемесодсасинк** вызывает [**методы ипортабледевицесервице::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="1442b-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="1442b-129">С помощью этого интерфейса он вызывает вспомогательную функцию **инвокемесодасинк** дважды; один раз для метода **бегинсинк** и один раз для метода **ендсинк** .</span><span class="sxs-lookup"><span data-stu-id="1442b-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="1442b-130">В этом примере **инвокемесодасинк** ожидает, пока глобальное событие не будет сигнальным при вызове [**ипортабледевицесервицемесодкаллбакк:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) .</span><span class="sxs-lookup"><span data-stu-id="1442b-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="1442b-131">В следующем коде используется метод **инвокемесодсасинк** .</span><span class="sxs-lookup"><span data-stu-id="1442b-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



<span data-ttu-id="1442b-132">Вспомогательная функция **инвокемесодасинк** выполняет следующие действия для каждого вызванного метода:</span><span class="sxs-lookup"><span data-stu-id="1442b-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="1442b-133">Создает глобальный обработчик событий, который отслеживается для определения завершения метода.</span><span class="sxs-lookup"><span data-stu-id="1442b-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="1442b-134">Создает объект **кмесодкаллбакк** , который предоставляется в качестве аргумента для [**ипортабледевицесервицемесодс: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span><span class="sxs-lookup"><span data-stu-id="1442b-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="1442b-135">Вызывает метод **ипортабледевицесервицемесодс:: InvokeAsync** для вызова данного метода.</span><span class="sxs-lookup"><span data-stu-id="1442b-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="1442b-136">Отслеживает глобальный обработчик событий для завершения.</span><span class="sxs-lookup"><span data-stu-id="1442b-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="1442b-137">Выполняет очистку.</span><span class="sxs-lookup"><span data-stu-id="1442b-137">Performs cleanup.</span></span>

<span data-ttu-id="1442b-138">Класс **кмесодкаллбакк** демонстрирует, как приложение может реализовать [**ипортабледевицесервицемесодкаллбакк**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span><span class="sxs-lookup"><span data-stu-id="1442b-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="1442b-139">Реализация **OnComplete** в этом классе сообщает о событии, чтобы уведомить приложение о завершении метода службы.</span><span class="sxs-lookup"><span data-stu-id="1442b-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="1442b-140">В дополнение к методу **OnComplete** этот класс реализует **AddRef**, **QueryInterface** и **Release**, которые используются для поддержания счетчика ссылок объекта и интерфейсов, которые он реализует.</span><span class="sxs-lookup"><span data-stu-id="1442b-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a><span data-ttu-id="1442b-141">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1442b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1442b-142">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="1442b-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="1442b-143">**ипортабледевицесервицемесодкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1442b-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="1442b-144">**ипортабледевицесервицемесодс**</span><span class="sxs-lookup"><span data-stu-id="1442b-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="1442b-145">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="1442b-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
