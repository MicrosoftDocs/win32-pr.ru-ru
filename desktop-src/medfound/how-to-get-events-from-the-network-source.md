---
description: Получение событий из сетевого источника
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Получение событий из сетевого источника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811338"
---
# <a name="how-to-get-events-from-the-network-source"></a>Получение событий из сетевого источника

Сопоставитель источников позволяет приложению создать сетевой источник и открыть подключение к определенному URL-адресу. Сетевой источник создает события, помечающие начало и конец асинхронной операции открытия соединения. Приложение может зарегистрировать эти события с помощью интерфейса [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .

Этот интерфейс предоставляет метод [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) , который сетевой источник вызывает напрямую при асинхронном открытии URL-адреса. Сетевой источник уведомляет приложение, когда оно начинает открывать URL-адрес, вызывая событие [меконнектстарт](meconnectstart.md) . Затем сетевой источник вызывает событие [меконнектенд](meconnectend.md) при завершении операции открытия.

> [!Note]  
> Чтобы отправить эти события в приложение, сетевой источник не использует интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , так как эти события вызываются до создания источника сети. Приложение может получать все остальные события источника сети с помощью интерфейса **Имфмедиаевентженератор** сеанса мультимедиа.

 

## <a name="to-get-events-from-the-network-source"></a>Получение событий из сетевого источника

1.  Реализуйте интерфейс [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) . В реализации метода [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) выполните следующие действия.
    1.  Получите состояние события, вызвав [**имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus). Этот метод указывает, завершилась ли операция, вызвавшая событие, например вызов метода сопоставителя источника. Если операция не выполнена успешно, состояние — код ошибки.
    2.  Обработайте событие на основе типа события: [меконнектстарт](meconnectstart.md) или [меконнектенд](meconnectend.md), который приложение может получить, вызвав [**имфмедиаевент:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).
2.  Настройте пару "ключ-значение" в объекте хранилища свойств, чтобы сохранить указатель на реализацию [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) , описанную в шаге 1.
    1.  Создайте объект хранилища свойств, вызвав функцию **пскреатемеморипропертисторе** .
    2.  Задайте свойство [**мфпкэй \_ саурцеопенмонитор**](mfpkey-sourceopenmonitor-property.md) в структуре **PROPERTYKEY** .
    3.  Укажите \_ значение данных неизвестного типа VT в структуре **пропвариант** , установив указатель **IUnknown** в реализацию приложения интерфейса [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .
    4.  Задайте пару "ключ-значение" в хранилище свойств, вызвав метод **ипропертисторе:: SetValue**.
3.  Передайте указатель хранилища свойств в методы сопоставителя источника, которые используются приложением для создания сетевого источника, например [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) и другие.

## <a name="example"></a>Пример

В следующем примере показано, как реализовать интерфейс [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) для получения событий из сетевого источника.


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



В следующем примере показано, как задать свойство [**мфпкэй \_ саурцеопенмонитор**](mfpkey-sourceopenmonitor-property.md) в сетевом источнике при открытии URL-адреса:


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сетевые подключения в Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



