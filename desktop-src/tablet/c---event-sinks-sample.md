---
description: Эта программа демонстрирует создание приложения, записывающего события InkCollector с использованием только C++. Эта программа совместно создает объект InkCollector для включения рукописного ввода. При получении события Stroke отображается окно сообщения.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Пример приемников событий C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701304"
---
# <a name="c-event-sinks-sample"></a>Пример приемников событий C++

Эта программа демонстрирует создание приложения, записывающего события InkCollector с использованием только C++. Эта программа совместно создает объект [**InkCollector**](inkcollector-class.md) для включения рукописного ввода. При получении события [**Stroke**](inkcollector-stroke.md) отображается окно сообщения.

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Определение оболочки для событий сборщика рукописных данных

`InkCollectorEvents`Класс обрабатывает передачу событий сборщика рукописных данных от сборщика рукописных данных пользователю этого класса. `AdviseInkCollector`Метод настраивает соединение между объектом [**InkCollector**](inkcollector-class.md) и этим классом. `Invoke`Метод преобразует уведомление о событии [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в вызов виртуальной функции, которую пользователь этого класса может переопределить для обработки определенного события.

> [!Note]  
> Чтобы получить это событие, необходимо выполнить больше, чем переопределить виртуальную функцию для обработчика событий. Для всех, кроме событий по умолчанию, необходимо вызвать метод [**сетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) сборщика рукописных данных, чтобы гарантировать получение события. Во вторых, этот объект маршалирует сами себя, так что все реализованные обработчики событий должны быть также свободны от потоков. Важно использовать API Windows, что может вызвать переключение на другой поток, так как обработчик событий не гарантирует, что он будет выполняться в том же потоке, что и окно, подключенное к сборщику рукописных данных.

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



`Init`Метод вызывает [кокреатефрисреадедмаршалер](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) для настройки свободного потокового маршалером.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



`AdviseInkCollector`Метод настраивает соединение между объектом [**InkCollector**](inkcollector-class.md) и этим классом. Сначала он извлекает точку подключения к сборщику рукописных данных. Затем он получает указатель на, `IInkCollectorEvents` чтобы он мог установить в качестве вспомогательного подключения к элементу управления.


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



`UnadviseInkCollector`Метод освобождает соединения, которые объект имеет к элементу управления.


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Определение обработчика событий сборщика рукописных данных

Класс Кминкевентс переопределяет поведение по умолчанию для обработчика событий [**Stroke**](inkcollector-stroke.md) класса инкколлекторевентс. Метод Stroke отображает окно сообщения, когда [**InkCollector**](inkcollector-class.md) получает событие **Stroke** .


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a>Определение оболочки сборщика рукописных данных

Метод init класса Кминкколлектор объявляет и инициализирует объект Кминкевентс. Затем он создает объект [**InkCollector**](inkcollector-class.md) и связывает сборщик рукописных данных и обработчик событий. Наконец, объект **InkCollector** присоединяется к окну и включается.


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Доступ к интерфейсам планшетных ПК и классам-оболочкам

Сначала включите заголовки для интерфейсов автоматизации планшетных ПК. Они устанавливаются вместе с <entity type="reg"/> <entity type="reg"/> пакетом средств разработки Microsoft Windows XP Tablet PC Edition 1,7.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Затем необходимо включить заголовки для классов-оболочек и обработчика событий [**InkCollector**](inkcollector-class.md) .


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Вызов классов-оболочек

При создании окна процедура окна создает оболочку сборщика рукописных данных и Инициализирует оболочку. При уничтожении окна процедура окна удаляет оболочку сборщика рукописных данных. Оболочка сборщика рукописных данных обрабатывает создание и удаление связанного обработчика событий.


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 
