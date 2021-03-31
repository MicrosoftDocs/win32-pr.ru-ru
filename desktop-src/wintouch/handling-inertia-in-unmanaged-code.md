---
title: Обработка инерции в неуправляемом коде
description: В этом разделе объясняется, как использовать интерфейс IInertiaProcessor для обработки инерции в неуправляемом коде.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Касание Windows, инерция
- Windows Touch, процессор манипуляции
- инерция, неуправляемый код
- инерция, интерфейс IInertiaProcessor
- инерция, процессор манипуляции
- процессор манипуляции, инерция
- Интерфейс IInertiaProcessor, неуправляемый код
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de56d06547f426de252a89ef5172df3fe4ca439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067457"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Обработка инерции в неуправляемом коде

В этом разделе объясняется, как использовать интерфейс [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) для обработки инерции в неуправляемом коде.

## <a name="overview"></a>Обзор

Чтобы использовать инерцию в неуправляемом коде, необходимо реализовать приемники событий как для обработчика манипуляции, так и для обработчика инерции. Начните с добавления поддержки манипуляции в приложение, как описано в разделе [Добавление поддержки манипуляций в неуправляемый код](adding-manipulation-support-in-unmanaged-code.md). Обратите внимание, что поддержка манипуляции требует использования сенсорных сообщений вместо сообщений жестов для передачи данных событий обработчику манипуляции. После обработки работы необходимо также реализовать второй приемник событий для событий, которые будет создавать интерфейс [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) , или потребуется изменить существующий приемник событий, чтобы он соответствовал обоим событиям, создаваемым интерфейсами **IInertiaProcessor** и [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . В этом примере проще начать с приемника событий, созданного для раздела Добавление поддержки манипуляций в неуправляемый код, и добавить второй конструктор, который работает с процессором инерции вместо обработчика манипуляции. Таким образом, реализация приемника событий может работать либо с обработчиком манипуляции, либо с обработчиком инерции. Помимо добавления второго конструктора, приемник событий будет иметь переменную, указывающую, будет ли выполняться операция на основе ввода инерции, а не входных данных.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Добавление поддержки инерции в приемник событий обработчика манипуляции

В следующем коде показан новый конструктор приемника событий, новые переменные-члены для интерфейса [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) и флаг, указывающий, является ли приемник экстраполяцией для инерции.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



После того как Заголовок класса содержит новые конструкторы и флаг, указывающий, выполняется ли экстраполяция, можно реализовать приемник событий, чтобы иметь отдельные блоки обработки для событий [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . Конструктор, принимающий **IManipulationProcessor** и **IInertiaProcessor** , должен установить для флага **фекстраполатинг** значение false, означающее, что это обработчик событий **IManipulationProcessor** . В следующем коде показано, как можно реализовать конструктор для приемника событий, использующего **IManipulationProcessor** .


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
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
```



В следующем коде показано, как можно реализовать конструктор для приемника событий, использующего [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . Этот конструктор устанавливает для флага **фекстраполатинг** значение true, указывающее, что этот экземпляр класса приемника событий будет выполнять экстраполяцию, и будет выполнять любые операции перемещения, которые были выполнены ранее событиями обработчика манипуляции.


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
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
```



> [!Note]  
> Реализация класса приемника событий из приемника событий обработчика манипуляции повторно используется в качестве приемника событий для обработчика инерции.

 

Теперь при создании этого класса **кманипулатионевентсинк** он может быть создан как приемник событий для обработчика манипуляции или как приемник событий для обработчика инерции. Если он создан как приемник событий обработчика инерции, для флага **фекстраполатинг** будет задано значение true, указывающее на то, что события манипуляции должны быть экстраполяциями.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) будет вызываться интерфейсами [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .

 

При запуске манипуляции задаются свойства интерфейса [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . В следующем коде показано, как обрабатывается событие Started.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



В этом примере для перемещения окна используются разности манипуляций. В следующем коде показано, как обрабатывается событие Дельта.


```C++
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
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



В этом примере обработка завершенных событий либо запускает, либо останавливает таймер, который будет вызывать [**процесс**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) в интерфейсе [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . В следующем коде показано, как обрабатывается завершенное событие манипуляции.


```C++
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
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



В следующем коде показано, как можно интерпретировать **сообщения \_ таймера WM** в **WndProc** , чтобы выполнять вызовы для [**обработки**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) в интерфейсе [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>Выинициализировать обработчик инерции и процессор манипуляции и инициализировать приемники событий

После изменения приемника событий для поддержки [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)вы можете инициализировать приемники событий и настроить их для запуска из приложения. В следующем коде показано, как выделяются указатели на интерфейс.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



В следующем примере кода показано, как создать экземпляр интерфейсов.


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



В следующем примере кода показано, как создать приемники событий с помощью указателей интерфейса и зарегистрировать окно для сенсорного ввода.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инерция](getting-started-with-inertia.md)
</dt> </dl>

 

 




