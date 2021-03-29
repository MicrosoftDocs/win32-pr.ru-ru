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
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="ad270-103">Получение событий из сетевого источника</span><span class="sxs-lookup"><span data-stu-id="ad270-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="ad270-104">Сопоставитель источников позволяет приложению создать сетевой источник и открыть подключение к определенному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="ad270-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="ad270-105">Сетевой источник создает события, помечающие начало и конец асинхронной операции открытия соединения.</span><span class="sxs-lookup"><span data-stu-id="ad270-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="ad270-106">Приложение может зарегистрировать эти события с помощью интерфейса [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="ad270-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="ad270-107">Этот интерфейс предоставляет метод [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) , который сетевой источник вызывает напрямую при асинхронном открытии URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="ad270-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="ad270-108">Сетевой источник уведомляет приложение, когда оно начинает открывать URL-адрес, вызывая событие [меконнектстарт](meconnectstart.md) .</span><span class="sxs-lookup"><span data-stu-id="ad270-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="ad270-109">Затем сетевой источник вызывает событие [меконнектенд](meconnectend.md) при завершении операции открытия.</span><span class="sxs-lookup"><span data-stu-id="ad270-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="ad270-110">Чтобы отправить эти события в приложение, сетевой источник не использует интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , так как эти события вызываются до создания источника сети.</span><span class="sxs-lookup"><span data-stu-id="ad270-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="ad270-111">Приложение может получать все остальные события источника сети с помощью интерфейса **Имфмедиаевентженератор** сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ad270-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="ad270-112">Получение событий из сетевого источника</span><span class="sxs-lookup"><span data-stu-id="ad270-112">To get events from the network source</span></span>

1.  <span data-ttu-id="ad270-113">Реализуйте интерфейс [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="ad270-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="ad270-114">В реализации метода [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ad270-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="ad270-115">Получите состояние события, вызвав [**имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span><span class="sxs-lookup"><span data-stu-id="ad270-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="ad270-116">Этот метод указывает, завершилась ли операция, вызвавшая событие, например вызов метода сопоставителя источника.</span><span class="sxs-lookup"><span data-stu-id="ad270-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="ad270-117">Если операция не выполнена успешно, состояние — код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad270-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="ad270-118">Обработайте событие на основе типа события: [меконнектстарт](meconnectstart.md) или [меконнектенд](meconnectend.md), который приложение может получить, вызвав [**имфмедиаевент:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span><span class="sxs-lookup"><span data-stu-id="ad270-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="ad270-119">Настройте пару "ключ-значение" в объекте хранилища свойств, чтобы сохранить указатель на реализацию [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) , описанную в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="ad270-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="ad270-120">Создайте объект хранилища свойств, вызвав функцию **пскреатемеморипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="ad270-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="ad270-121">Задайте свойство [**мфпкэй \_ саурцеопенмонитор**](mfpkey-sourceopenmonitor-property.md) в структуре **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="ad270-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="ad270-122">Укажите \_ значение данных неизвестного типа VT в структуре **пропвариант** , установив указатель **IUnknown** в реализацию приложения интерфейса [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="ad270-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="ad270-123">Задайте пару "ключ-значение" в хранилище свойств, вызвав метод **ипропертисторе:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="ad270-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="ad270-124">Передайте указатель хранилища свойств в методы сопоставителя источника, которые используются приложением для создания сетевого источника, например [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) и другие.</span><span class="sxs-lookup"><span data-stu-id="ad270-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="ad270-125">Пример</span><span class="sxs-lookup"><span data-stu-id="ad270-125">Example</span></span>

<span data-ttu-id="ad270-126">В следующем примере показано, как реализовать интерфейс [**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) для получения событий из сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="ad270-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


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



<span data-ttu-id="ad270-127">В следующем примере показано, как задать свойство [**мфпкэй \_ саурцеопенмонитор**](mfpkey-sourceopenmonitor-property.md) в сетевом источнике при открытии URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="ad270-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ad270-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ad270-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad270-129">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad270-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



