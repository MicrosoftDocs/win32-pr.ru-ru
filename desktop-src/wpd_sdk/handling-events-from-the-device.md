---
description: Обработка событий с устройства
ms.assetid: 529a8b7a-08b4-47de-8ed3-28e8fff0ede2
title: Обработка событий с устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74692b73e39aa83286604408f3c556f5fbeb3f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703263"
---
# <a name="handling-events-from-the-device"></a>Обработка событий с устройства

Другая операция, выполняемая приложением WPD, — это обработка событий, запускаемых устройством.

Операции обработки событий выполняются с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                      | Описание                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                           | Позволяет приложению регистрироваться для получения асинхронных обратных вызовов. |
| [**Интерфейс Ипортабледевицеевенткаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback) | Содержит обработчик событий приложения.                        |



 

Класс Кпортабледевицеевентскаллбакк в модуле Девицеевентс. cpp примера приложения демонстрирует, как приложение может реализовать [**ипортабледевицеевенткаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback). Реализация метода [**oneven**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) в этом классе записывает параметры для любого события в окно консоли приложения. В дополнение к методу oneven этот класс реализует AddRef и Release, которые используются для поддержания счетчика ссылок объекта.


```C++
class CPortableDeviceEventsCallback : public IPortableDeviceEventCallback
{
public:
    CPortableDeviceEventsCallback() : m_cRef(1)
    {
    }

    ~CPortableDeviceEventsCallback()
    {
    }

    HRESULT __stdcall QueryInterface(
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
            (riid == IID_IPortableDeviceEventCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    ULONG __stdcall AddRef()
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    ULONG __stdcall Release()
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

    HRESULT __stdcall OnEvent(
        IPortableDeviceValues* pEventParameters)
    {
        HRESULT hr = S_OK;

        if (pEventParameters != NULL)
        {
            printf("***************************\n** Device event received **\n***************************\n");
            DisplayStringProperty(pEventParameters, WPD_EVENT_PARAMETER_PNP_DEVICE_ID, L"WPD_EVENT_PARAMETER_PNP_DEVICE_ID");
            DisplayGuidProperty(pEventParameters, WPD_EVENT_PARAMETER_EVENT_ID, L"WPD_EVENT_PARAMETER_EVENT_ID");
        }

        return hr;
    }

    ULONG m_cRef;
};
```



Пример приложения создает экземпляр класса Кпортабледевицеевентскаллбакк в своей вспомогательной функции Регистерфоревентнотификатионс. Эта функция создает экземпляр объекта обратного вызова с помощью оператора New. Затем он вызывает метод [**ипортабледевице:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) для регистрации обратного вызова и начала получения событий.


```C++
void RegisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT                        hr = S_OK;
    LPWSTR                         wszEventCookie = NULL;
    CPortableDeviceEventsCallback* pCallback = NULL;

    if (pDevice == NULL)
    {
        return;
    }

    // Check to see if we already have an event registration cookie.  If so,
    // then avoid registering again.
    // NOTE: An application can register for events as many times as they want.
    //       This sample only keeps a single registration cookie around for
    //       simplicity.
    if (g_strEventRegistrationCookie.GetLength() > 0)
    {
        printf("This application has already registered to receive device events.\n");
        return;
    }

    // Create an instance of the callback object.  This will be called when events
    // are received.
    if (hr == S_OK)
    {
        pCallback = new CPortableDeviceEventsCallback();
        if (pCallback == NULL)
        {
            hr = E_OUTOFMEMORY;
            printf("Failed to allocate memory for IPortableDeviceEventsCallback object, hr = 0x%lx\n",hr);
        }
    }

    // Call Advise to register the callback and receive events.
    if (hr == S_OK)
    {
        hr = pDevice->Advise(0, pCallback, NULL, &wszEventCookie);
        if (FAILED(hr))
        {
            printf("! Failed to register for device events, hr = 0x%lx\n",hr);
        }
    }

    // Save the event registration cookie if event registration was successful.
    if (hr == S_OK)
    {
        g_strEventRegistrationCookie = wszEventCookie;
    }

    // Free the event registration cookie, if one was returned.
    if (wszEventCookie != NULL)
    {
        CoTaskMemFree(wszEventCookie);
        wszEventCookie = NULL;
    }

    if (hr == S_OK)
    {
        printf("This application has registered for device event notifications and was returned the registration cookie '%ws'", g_strEventRegistrationCookie.GetString());
    }

    // If a failure occurs, remember to delete the allocated callback object, if one exists.
    if (pCallback != NULL)
    {
        pCallback->Release();
    }
```



Когда пример приложения выполняет получение событий, он вызывает вспомогательную функцию Унрегистерфоревентнотификатионс. Эта функция, в свою очередь, вызывает метод [**ипортабледевице:: unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) , чтобы отменить регистрацию обратного вызова для получения событий.


```C++
void UnregisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;

    if (pDevice == NULL)
    {
        return;
    }

    hr = pDevice->Unadvise(g_strEventRegistrationCookie);
    if (FAILED(hr))
    {
        printf("! Failed to unregister for device events using registration cookie '%ws', hr = 0x%lx\n",g_strEventRegistrationCookie.GetString(), hr);
    }

    if (hr == S_OK)
    {
        printf("This application used the registration cookie '%ws' to unregister from receiving device event notifications", g_strEventRegistrationCookie.GetString());
    }

    g_strEventRegistrationCookie = L"";
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеевенткаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



