---
description: Асинхронный вызов методов службы
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Асинхронный вызов методов службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265435"
---
# <a name="invoking-service-methods-asynchronously"></a>Асинхронный вызов методов службы

Приложение Впдсервицеаписампле содержит код, демонстрирующий, как приложение может асинхронно вызывать методы службы. В этом образце используются следующие интерфейсы.



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейс                                                                               | Описание                                                                                                                                                             |
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Используется для получения интерфейса **ипортабледевицесервицемесодс** для вызова методов в заданной службе.                                                                  |
| [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Используется для вызова метода службы.                                                                                                                                        |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)                                  | Используется для хранения параметров исходящего метода и результатов входящего метода. Может иметь **значение NULL** , если метод не требует никаких параметров или не возвращает никаких результатов. |
| [**ипортабледевицесервицемесодкаллбакк**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Реализуется приложением для получения результатов метода после завершения метода.                                                                               |



 

Когда пользователь выбирает в командной строке параметр "10", приложение вызывает метод **инвокемесодсасинк** , который находится в модуле сервицемесодс. cpp. Обратите внимание, что до вызова методов пример приложения открывает службу контактов на подключенном устройстве.

Методы службы инкапсулируют функциональные возможности, определяемые и реализуемые каждой службой. Они уникальны для каждого типа службы и представлены идентификатором GUID. Например, служба Contacts определяет метод **бегинсинк** , который вызывается приложениями для подготовки устройства к синхронизации объектов Contact, и метод **ендсинк** для уведомления устройства о завершении синхронизации. Приложения выполняют метод службы переносимых устройств путем вызова [**ипортабледевицесервицемесодс:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Методы службы не следует путать с командами WPD. Команды WPD являются частью стандартного интерфейса драйвера устройства WPD (DDI) и являются механизмом обмена данными между приложением WPD и драйвером. Команды являются предопределенными, сгруппированные по категориям (например, **\_ категории WPD \_ Common**), и представляются структурой **PROPERTYKEY** . Приложение отправляет команды драйверу устройства, вызывая [**ипортабледевицесервице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Дополнительные сведения см. в разделе команды.

Метод **инвокемесодсасинк** вызывает [**методы ипортабледевицесервице::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) для получения интерфейса [**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . С помощью этого интерфейса он вызывает вспомогательную функцию **инвокемесодасинк** дважды; один раз для метода **бегинсинк** и один раз для метода **ендсинк** . В этом примере **инвокемесодасинк** ожидает, пока глобальное событие не будет сигнальным при вызове [**ипортабледевицесервицемесодкаллбакк:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) .

В следующем коде используется метод **инвокемесодсасинк** .


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



Вспомогательная функция **инвокемесодасинк** выполняет следующие действия для каждого вызванного метода:

-   Создает глобальный обработчик событий, который отслеживается для определения завершения метода.
-   Создает объект **кмесодкаллбакк** , который предоставляется в качестве аргумента для [**ипортабледевицесервицемесодс: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).
-   Вызывает метод **ипортабледевицесервицемесодс:: InvokeAsync** для вызова данного метода.
-   Отслеживает глобальный обработчик событий для завершения.
-   Выполняет очистку.

Класс **кмесодкаллбакк** демонстрирует, как приложение может реализовать [**ипортабледевицесервицемесодкаллбакк**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback). Реализация **OnComplete** в этом классе сообщает о событии, чтобы уведомить приложение о завершении метода службы. В дополнение к методу **OnComplete** этот класс реализует **AddRef**, **QueryInterface** и **Release**, которые используются для поддержания счетчика ссылок объекта и интерфейсов, которые он реализует.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**ипортабледевицесервицемесодкаллбакк**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**ипортабледевицесервицемесодс**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
