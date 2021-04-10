---
title: Добавление поддержки манипуляции в неуправляемый код
description: В этом разделе объясняется, как добавить поддержку манипуляции в неуправляемый код путем реализации приемника событий для \_ интерфейса иманипулатионевентс.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Касание Windows, манипуляции
- Windows Touch, _IManipulationEvents интерфейс
- Windows Touch, интерфейс IManipulationProcessor
- манипуляции, Добавление поддержки в неуправляемом коде
- манипуляции, поддержка неуправляемого кода
- манипуляции, поддержка в неуправляемом коде
- манипуляции, интерфейс _IManipulationEvents
- манипуляции, интерфейс IManipulationProcessor
- Интерфейс _IManipulationEvents, поддержка манипуляции в неуправляемом коде
- Интерфейс IManipulationProcessor, поддержка манипуляции в неуправляемом коде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134303"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a><span data-ttu-id="bc44d-113">Добавление поддержки манипуляции в неуправляемый код</span><span class="sxs-lookup"><span data-stu-id="bc44d-113">Adding Manipulation Support in Unmanaged Code</span></span>

<span data-ttu-id="bc44d-114">В этом разделе объясняется, как добавить поддержку манипуляции в неуправляемый код путем реализации приемника событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="bc44d-114">This section explains how to add manipulation support to unmanaged code by implementing an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

<span data-ttu-id="bc44d-115">На следующем рисунке изображена архитектура манипуляции.</span><span class="sxs-lookup"><span data-stu-id="bc44d-115">The following image outlines the manipulation architecture.</span></span>

![Иллюстрация, показывающая сообщения касания Windows, которые передаются в обработчик манипуляции объекта, который обрабатывает события с помощью \- интерфейса иманипулатионевентс](images/manipulation-arch.png)

<span data-ttu-id="bc44d-117">Сенсорные данные, полученные от сообщений [**WM \_ Touch**](wm-touchdown.md) , передаются в [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) вместе с идентификатором контакта из сообщения Touch.</span><span class="sxs-lookup"><span data-stu-id="bc44d-117">Touch data that is received from [**WM\_TOUCH**](wm-touchdown.md) messages is passed to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) together with the contact ID from the touch message.</span></span> <span data-ttu-id="bc44d-118">На основе последовательности сообщений интерфейс **IManipulationProcessor** вычисляет тип выполняемого преобразования и значения, связанные с этим преобразованием.</span><span class="sxs-lookup"><span data-stu-id="bc44d-118">Based on the message sequence, the **IManipulationProcessor** interface will calculate what kind of transformation is being performed and what the values associated with this transformation are.</span></span> <span data-ttu-id="bc44d-119">Затем **IManipulationProcessor** создаст [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) , которые обрабатываются приемником событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-119">The **IManipulationProcessor** will then generate [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) which are handled by an event sink.</span></span> <span data-ttu-id="bc44d-120">Затем приемник событий может использовать эти значения для выполнения пользовательских операций с объектом, для которого выполняется преобразование.</span><span class="sxs-lookup"><span data-stu-id="bc44d-120">The event sink can then use these values to perform custom operations on the object being transformed.</span></span>

<span data-ttu-id="bc44d-121">Чтобы добавить в приложение поддержку манипуляций, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bc44d-121">To add manipulation support to your application, you must follow these steps:</span></span>

1.  <span data-ttu-id="bc44d-122">Реализуйте приемник событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="bc44d-122">Implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>
2.  <span data-ttu-id="bc44d-123">Создайте экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="bc44d-123">Create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>
3.  <span data-ttu-id="bc44d-124">Создайте экземпляр приемника событий и настройте события касания.</span><span class="sxs-lookup"><span data-stu-id="bc44d-124">Create an instance of your event sink and set up touch events.</span></span>
4.  <span data-ttu-id="bc44d-125">Отправка данных о событиях касания обработчику манипуляции.</span><span class="sxs-lookup"><span data-stu-id="bc44d-125">Send touch event data to the manipulation processor.</span></span>

<span data-ttu-id="bc44d-126">В этом разделе описаны шаги, которые необходимо выполнить для добавления поддержки манипуляции в приложение.</span><span class="sxs-lookup"><span data-stu-id="bc44d-126">This section explains the steps that you must follow to add manipulation support to your application.</span></span> <span data-ttu-id="bc44d-127">Код предоставляется на каждом шаге, чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="bc44d-127">Code is provided at each step to get you started.</span></span>

> [!Note]  
> <span data-ttu-id="bc44d-128">Нельзя одновременно использовать манипуляции и жесты, так как жесты и сенсорные сообщения являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="bc44d-128">You cannot use manipulations and gestures at the same time because gesture and touch messages are mutually exclusive.</span></span>

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a><span data-ttu-id="bc44d-129">Реализация приемника событий для \_ интерфейса иманипуалтионевентс</span><span class="sxs-lookup"><span data-stu-id="bc44d-129">Implement an Event Sink for \_IManipualtionEvents Interface</span></span>

<span data-ttu-id="bc44d-130">Прежде чем можно будет создать экземпляр приемника событий, необходимо создать класс, реализующий интерфейс [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) для событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-130">Before you can create an instance of your event sink, you must create a class that implements the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface for eventing.</span></span> <span data-ttu-id="bc44d-131">Это ваш приемник событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-131">This is your event sink.</span></span> <span data-ttu-id="bc44d-132">События, создаваемые интерфейсом [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) , обрабатываются приемником событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-132">Events generated by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface are handled by your event sink.</span></span> <span data-ttu-id="bc44d-133">В следующем примере кода показан заголовок для класса, который наследует интерфейс **\_ иманипулатионевентс** .</span><span class="sxs-lookup"><span data-stu-id="bc44d-133">The following code shows an example header for a class that inherits the **\_IManipulationEvents** interface.</span></span>

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT translationDeltaX,
        /* [in] */ FLOAT translationDeltaY,
        /* [in] */ FLOAT scaleDelta,
        /* [in] */ FLOAT expansionDelta,
        /* [in] */ FLOAT rotationDelta,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

<span data-ttu-id="bc44d-134">При наличии заголовка необходимо создать реализацию интерфейса событий, чтобы ваш класс выполнял действия, которые должен выполнять обработчик манипуляции.</span><span class="sxs-lookup"><span data-stu-id="bc44d-134">Given the header, you must create an implementation of the events interface so that your class performs the actions that you want the manipulation processor to perform.</span></span> <span data-ttu-id="bc44d-135">Следующий код представляет собой шаблон, который реализует минимальную функциональность приемника событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="bc44d-135">The following code is a template that implements the minimum functionality of an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
    
    RECT rect;
        
    GetWindowRect(m_hWnd, &rect);
    
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

<span data-ttu-id="bc44d-136">Обратите особое внимание на реализации методов [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)и [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) в классе.</span><span class="sxs-lookup"><span data-stu-id="bc44d-136">Pay extra attention to implementations of [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) methods in the class.</span></span> <span data-ttu-id="bc44d-137">Это наиболее вероятные методы в интерфейсе, которые потребует выполнения операций на основе данных манипуляции, передаваемых в событии.</span><span class="sxs-lookup"><span data-stu-id="bc44d-137">These are the most likely methods in the interface that will require you to perform operations based on the manipulation information that is passed around in the event.</span></span> <span data-ttu-id="bc44d-138">Обратите внимание, что второй параметр в конструкторе является объектом, используемым в манипуляциях событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-138">Note also that the second parameter in the constructor is the object that is used in the event manipulations.</span></span> <span data-ttu-id="bc44d-139">В коде, используемом для создания образца, hWnd приложения отправляется в конструктор, чтобы его можно было перемещать и изменять его размер.</span><span class="sxs-lookup"><span data-stu-id="bc44d-139">In the code used for producing the sample, the hWnd for the application is sent to the constructor so that it can be repositioned and resized.</span></span>

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a><span data-ttu-id="bc44d-140">Создание экземпляра интерфейса IManipulationProcessor</span><span class="sxs-lookup"><span data-stu-id="bc44d-140">Create an instance of an IManipulationProcessor Interface</span></span>

<span data-ttu-id="bc44d-141">В коде, где будут использоваться манипуляции, необходимо создать экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="bc44d-141">In the code where you will use manipulations, you must create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="bc44d-142">Сначала необходимо добавить поддержку для класса манипуляций.</span><span class="sxs-lookup"><span data-stu-id="bc44d-142">First you must add support for the manipulations class.</span></span> <span data-ttu-id="bc44d-143">В следующем коде показано, как это можно сделать в классе.</span><span class="sxs-lookup"><span data-stu-id="bc44d-143">The following code shows how you can do this in your class.</span></span>

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

<span data-ttu-id="bc44d-144">После создания переменной для обработчика манипуляции и включения заголовков для манипуляций необходимо создать экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="bc44d-144">After you have your variable for the manipulation processor and you have included the headers for manipulations, you have to create an instance of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="bc44d-145">Это COM-объект.</span><span class="sxs-lookup"><span data-stu-id="bc44d-145">This is a COM object.</span></span> <span data-ttu-id="bc44d-146">Поэтому необходимо вызвать [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), а затем создать экземпляр ссылки на **IManipulationProcessor**.</span><span class="sxs-lookup"><span data-stu-id="bc44d-146">Therefore, you must call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), and then create an instance of your reference to the **IManipulationProcessor**.</span></span> <span data-ttu-id="bc44d-147">В следующем коде показано, как можно создать экземпляр этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bc44d-147">The following code shows how you can create an instance of this interface.</span></span>

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a><span data-ttu-id="bc44d-148">Создание экземпляра приемника событий и настройка событий касания</span><span class="sxs-lookup"><span data-stu-id="bc44d-148">Create an instance of your Event Sink and set up Touch Events</span></span>

<span data-ttu-id="bc44d-149">Включите определение класса приемника событий в код, а затем добавьте переменную для класса приемника событий манипуляции.</span><span class="sxs-lookup"><span data-stu-id="bc44d-149">Include the definition for your event sink class to your code and then add a variable for the manipulation event sink class.</span></span> <span data-ttu-id="bc44d-150">Следующий пример кода включает заголовок для реализации класса и настраивает глобальную переменную для хранения приемника событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-150">The following code example includes the header for the class implementation and sets up a global variable to store the event sink.</span></span>

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

<span data-ttu-id="bc44d-151">После того как вы добавили переменную и включили определение для нового класса приемника событий, можно создать класс с помощью обработчика манипуляций, настроенного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="bc44d-151">After you have the variable and have included your definition for the new event sink class, you can construct the class by using the manipulation processor that you have set up in the previous step.</span></span> <span data-ttu-id="bc44d-152">В следующем коде показано, как экземпляр этого класса будет создан из **онинитдиалог**.</span><span class="sxs-lookup"><span data-stu-id="bc44d-152">The following code shows how an instance of this class would be created from **OnInitDialog**.</span></span>

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> <span data-ttu-id="bc44d-153">Способ создания экземпляра приемника событий зависит от того, что вы делаете с данными манипуляции.</span><span class="sxs-lookup"><span data-stu-id="bc44d-153">The way that you create an instance of your event sink depends on what you are doing with the manipulation data.</span></span> <span data-ttu-id="bc44d-154">В большинстве случаев создается приемник событий обработчика манипуляций, который не имеет того же конструктора, что и этот пример.</span><span class="sxs-lookup"><span data-stu-id="bc44d-154">In most cases, you will create a manipulation processor event sink that does not have the same constructor as this example.</span></span>

### <a name="send-touch-event-data-to-the-manipulation-processor"></a><span data-ttu-id="bc44d-155">Отправка данных о событиях касания обработчику манипуляции</span><span class="sxs-lookup"><span data-stu-id="bc44d-155">Send Touch Event Data to the Manipulation Processor</span></span>

<span data-ttu-id="bc44d-156">Теперь, когда у вас установлен обработчик манипуляции и приемник событий, необходимо передать данные касания обработчику манипуляции, чтобы активировать события манипуляции.</span><span class="sxs-lookup"><span data-stu-id="bc44d-156">Now that you have your manipulation processor and event sink set up, you must feed touch data to the manipulation processor to trigger manipulation events.</span></span>

> [!Note]  
> <span data-ttu-id="bc44d-157">Эта процедура описана в разделе [Начало работы с сообщениями Windows Touch](getting-started-with-multi-touch-messages.md).</span><span class="sxs-lookup"><span data-stu-id="bc44d-157">This is the same procedure as discussed in [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md).</span></span>

<span data-ttu-id="bc44d-158">Во первых, вы создадите код для декодирования сообщений [**WM \_ Touch**](wm-touchdown.md) и их отправки в интерфейс [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) для вызова событий.</span><span class="sxs-lookup"><span data-stu-id="bc44d-158">First, you will create some code to decode the [**WM\_TOUCH**](wm-touchdown.md) messages and send them to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface to raise events.</span></span> <span data-ttu-id="bc44d-159">В следующем коде показан пример реализации, которая вызывается из метода **WndProc** и возвращает **lResult** для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bc44d-159">The following code shows an example implementation that is called from the **WndProc** method and return an **LRESULT** for messaging.</span></span>

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

<span data-ttu-id="bc44d-160">Теперь, когда у вас есть служебный метод для декодирования сообщения [**WM \_ Touch**](wm-touchdown.md) , необходимо передать сообщения **WM \_ Touch** функции служебной программы из метода **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="bc44d-160">Now that you have a utility method for decoding the [**WM\_TOUCH**](wm-touchdown.md) message, you must pass the **WM\_TOUCH** messages to the utility function from your **WndProc** method.</span></span> <span data-ttu-id="bc44d-161">В следующем коде показано, как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="bc44d-161">The following code shows how you can do this.</span></span>

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="bc44d-162">Пользовательские методы, реализованные в приемнике событий, теперь должны работать.</span><span class="sxs-lookup"><span data-stu-id="bc44d-162">The custom methods that you have implemented in your event sink should now work.</span></span> <span data-ttu-id="bc44d-163">В этом примере прикосновение к окну будет перемещено.</span><span class="sxs-lookup"><span data-stu-id="bc44d-163">In this example, touching the window will move it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc44d-164">См. также</span><span class="sxs-lookup"><span data-stu-id="bc44d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc44d-165">Манипуляции</span><span class="sxs-lookup"><span data-stu-id="bc44d-165">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>


 