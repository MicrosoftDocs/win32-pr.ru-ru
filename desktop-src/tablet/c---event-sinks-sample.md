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
# <a name="c-event-sinks-sample"></a><span data-ttu-id="312d2-105">Пример приемников событий C++</span><span class="sxs-lookup"><span data-stu-id="312d2-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="312d2-106">Эта программа демонстрирует создание приложения, записывающего события InkCollector с использованием только C++.</span><span class="sxs-lookup"><span data-stu-id="312d2-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="312d2-107">Эта программа совместно создает объект [**InkCollector**](inkcollector-class.md) для включения рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="312d2-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="312d2-108">При получении события [**Stroke**](inkcollector-stroke.md) отображается окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="312d2-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="312d2-109">Определение оболочки для событий сборщика рукописных данных</span><span class="sxs-lookup"><span data-stu-id="312d2-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="312d2-110">`InkCollectorEvents`Класс обрабатывает передачу событий сборщика рукописных данных от сборщика рукописных данных пользователю этого класса.</span><span class="sxs-lookup"><span data-stu-id="312d2-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="312d2-111">`AdviseInkCollector`Метод настраивает соединение между объектом [**InkCollector**](inkcollector-class.md) и этим классом.</span><span class="sxs-lookup"><span data-stu-id="312d2-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="312d2-112">`Invoke`Метод преобразует уведомление о событии [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в вызов виртуальной функции, которую пользователь этого класса может переопределить для обработки определенного события.</span><span class="sxs-lookup"><span data-stu-id="312d2-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="312d2-113">Чтобы получить это событие, необходимо выполнить больше, чем переопределить виртуальную функцию для обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="312d2-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="312d2-114">Для всех, кроме событий по умолчанию, необходимо вызвать метод [**сетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) сборщика рукописных данных, чтобы гарантировать получение события.</span><span class="sxs-lookup"><span data-stu-id="312d2-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="312d2-115">Во вторых, этот объект маршалирует сами себя, так что все реализованные обработчики событий должны быть также свободны от потоков.</span><span class="sxs-lookup"><span data-stu-id="312d2-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="312d2-116">Важно использовать API Windows, что может вызвать переключение на другой поток, так как обработчик событий не гарантирует, что он будет выполняться в том же потоке, что и окно, подключенное к сборщику рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="312d2-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


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



<span data-ttu-id="312d2-117">`Init`Метод вызывает [кокреатефрисреадедмаршалер](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) для настройки свободного потокового маршалером.</span><span class="sxs-lookup"><span data-stu-id="312d2-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="312d2-118">`AdviseInkCollector`Метод настраивает соединение между объектом [**InkCollector**](inkcollector-class.md) и этим классом.</span><span class="sxs-lookup"><span data-stu-id="312d2-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="312d2-119">Сначала он извлекает точку подключения к сборщику рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="312d2-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="312d2-120">Затем он получает указатель на, `IInkCollectorEvents` чтобы он мог установить в качестве вспомогательного подключения к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="312d2-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


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



<span data-ttu-id="312d2-121">`UnadviseInkCollector`Метод освобождает соединения, которые объект имеет к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="312d2-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="312d2-122">Определение обработчика событий сборщика рукописных данных</span><span class="sxs-lookup"><span data-stu-id="312d2-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="312d2-123">Класс Кминкевентс переопределяет поведение по умолчанию для обработчика событий [**Stroke**](inkcollector-stroke.md) класса инкколлекторевентс.</span><span class="sxs-lookup"><span data-stu-id="312d2-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="312d2-124">Метод Stroke отображает окно сообщения, когда [**InkCollector**](inkcollector-class.md) получает событие **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="312d2-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


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



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="312d2-125">Определение оболочки сборщика рукописных данных</span><span class="sxs-lookup"><span data-stu-id="312d2-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="312d2-126">Метод init класса Кминкколлектор объявляет и инициализирует объект Кминкевентс.</span><span class="sxs-lookup"><span data-stu-id="312d2-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="312d2-127">Затем он создает объект [**InkCollector**](inkcollector-class.md) и связывает сборщик рукописных данных и обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="312d2-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="312d2-128">Наконец, объект **InkCollector** присоединяется к окну и включается.</span><span class="sxs-lookup"><span data-stu-id="312d2-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="312d2-129">Доступ к интерфейсам планшетных ПК и классам-оболочкам</span><span class="sxs-lookup"><span data-stu-id="312d2-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="312d2-130">Сначала включите заголовки для интерфейсов автоматизации планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="312d2-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="312d2-131">Они устанавливаются вместе с <entity type="reg"/> <entity type="reg"/> пакетом средств разработки Microsoft Windows XP Tablet PC Edition 1,7.</span><span class="sxs-lookup"><span data-stu-id="312d2-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="312d2-132">Затем необходимо включить заголовки для классов-оболочек и обработчика событий [**InkCollector**](inkcollector-class.md) .</span><span class="sxs-lookup"><span data-stu-id="312d2-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="312d2-133">Вызов классов-оболочек</span><span class="sxs-lookup"><span data-stu-id="312d2-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="312d2-134">При создании окна процедура окна создает оболочку сборщика рукописных данных и Инициализирует оболочку.</span><span class="sxs-lookup"><span data-stu-id="312d2-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="312d2-135">При уничтожении окна процедура окна удаляет оболочку сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="312d2-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="312d2-136">Оболочка сборщика рукописных данных обрабатывает создание и удаление связанного обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="312d2-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


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



 

 
