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
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Добавление поддержки манипуляции в неуправляемый код

В этом разделе объясняется, как добавить поддержку манипуляции в неуправляемый код путем реализации приемника событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

На следующем рисунке изображена архитектура манипуляции.

![Иллюстрация, показывающая сообщения касания Windows, которые передаются в обработчик манипуляции объекта, который обрабатывает события с помощью \- интерфейса иманипулатионевентс](images/manipulation-arch.png)

Сенсорные данные, полученные от сообщений [**WM \_ Touch**](wm-touchdown.md) , передаются в [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) вместе с идентификатором контакта из сообщения Touch. На основе последовательности сообщений интерфейс **IManipulationProcessor** вычисляет тип выполняемого преобразования и значения, связанные с этим преобразованием. Затем **IManipulationProcessor** создаст [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) , которые обрабатываются приемником событий. Затем приемник событий может использовать эти значения для выполнения пользовательских операций с объектом, для которого выполняется преобразование.

Чтобы добавить в приложение поддержку манипуляций, необходимо выполнить следующие действия.

1.  Реализуйте приемник событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .
2.  Создайте экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .
3.  Создайте экземпляр приемника событий и настройте события касания.
4.  Отправка данных о событиях касания обработчику манипуляции.

В этом разделе описаны шаги, которые необходимо выполнить для добавления поддержки манипуляции в приложение. Код предоставляется на каждом шаге, чтобы приступить к работе.

> [!Note]  
> Нельзя одновременно использовать манипуляции и жесты, так как жесты и сенсорные сообщения являются взаимоисключающими.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Реализация приемника событий для \_ интерфейса иманипуалтионевентс

Прежде чем можно будет создать экземпляр приемника событий, необходимо создать класс, реализующий интерфейс [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) для событий. Это ваш приемник событий. События, создаваемые интерфейсом [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) , обрабатываются приемником событий. В следующем примере кода показан заголовок для класса, который наследует интерфейс **\_ иманипулатионевентс** .

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

При наличии заголовка необходимо создать реализацию интерфейса событий, чтобы ваш класс выполнял действия, которые должен выполнять обработчик манипуляции. Следующий код представляет собой шаблон, который реализует минимальную функциональность приемника событий для интерфейса [**\_ иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

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

Обратите особое внимание на реализации методов [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)и [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) в классе. Это наиболее вероятные методы в интерфейсе, которые потребует выполнения операций на основе данных манипуляции, передаваемых в событии. Обратите внимание, что второй параметр в конструкторе является объектом, используемым в манипуляциях событий. В коде, используемом для создания образца, hWnd приложения отправляется в конструктор, чтобы его можно было перемещать и изменять его размер.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Создание экземпляра интерфейса IManipulationProcessor

В коде, где будут использоваться манипуляции, необходимо создать экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Сначала необходимо добавить поддержку для класса манипуляций. В следующем коде показано, как это можно сделать в классе.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

После создания переменной для обработчика манипуляции и включения заголовков для манипуляций необходимо создать экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Это COM-объект. Поэтому необходимо вызвать [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), а затем создать экземпляр ссылки на **IManipulationProcessor**. В следующем коде показано, как можно создать экземпляр этого интерфейса.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Создание экземпляра приемника событий и настройка событий касания

Включите определение класса приемника событий в код, а затем добавьте переменную для класса приемника событий манипуляции. Следующий пример кода включает заголовок для реализации класса и настраивает глобальную переменную для хранения приемника событий.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

После того как вы добавили переменную и включили определение для нового класса приемника событий, можно создать класс с помощью обработчика манипуляций, настроенного на предыдущем шаге. В следующем коде показано, как экземпляр этого класса будет создан из **онинитдиалог**.

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> Способ создания экземпляра приемника событий зависит от того, что вы делаете с данными манипуляции. В большинстве случаев создается приемник событий обработчика манипуляций, который не имеет того же конструктора, что и этот пример.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Отправка данных о событиях касания обработчику манипуляции

Теперь, когда у вас установлен обработчик манипуляции и приемник событий, необходимо передать данные касания обработчику манипуляции, чтобы активировать события манипуляции.

> [!Note]  
> Эта процедура описана в разделе [Начало работы с сообщениями Windows Touch](getting-started-with-multi-touch-messages.md).

Во первых, вы создадите код для декодирования сообщений [**WM \_ Touch**](wm-touchdown.md) и их отправки в интерфейс [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) для вызова событий. В следующем коде показан пример реализации, которая вызывается из метода **WndProc** и возвращает **lResult** для обмена сообщениями.

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

Теперь, когда у вас есть служебный метод для декодирования сообщения [**WM \_ Touch**](wm-touchdown.md) , необходимо передать сообщения **WM \_ Touch** функции служебной программы из метода **WndProc** . В следующем коде показано, как это можно сделать.

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

Пользовательские методы, реализованные в приемнике событий, теперь должны работать. В этом примере прикосновение к окну будет перемещено.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Манипуляции](getting-started-with-manipulations.md)
</dt> </dl>


 