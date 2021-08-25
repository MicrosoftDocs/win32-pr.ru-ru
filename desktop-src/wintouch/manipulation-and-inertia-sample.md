---
title: Пример манипуляции и инерции
description: в примере манипуляции и инерции показано, как добавить поддержку сенсорного ввода Windows в собственные приложения на основе Windows, использующие API-интерфейс Windows Touch.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows Сенсорный ввод, примеры кода
- Windows Сенсорный ввод, пример кода
- Windows Сенсорный ввод, манипуляции
- Windows Сенсорный ввод, инерция
- Windows Пример сенсорного управления, манипулирования и инерции
- Пример манипуляции и инерции
- Windows Сенсорный ввод, _IManipulationEventSink интерфейс
- Windows Сенсорный ввод, интерфейс IManipulationProcessor
- Windows Сенсорный ввод, интерфейс IInertiaProcessor
- манипуляции, пример кода
- манипуляции, примеры кода
- манипуляции, интерфейс _IManipulationEventSink
- манипуляции, интерфейс IManipulationProcessor
- инерция, пример кода
- инерция, примеры кода
- инерция, интерфейс IInertiaProcessor
- Интерфейс _IManipulationEventSink
- Интерфейс IManipulationProcessor, примеры кода
- Интерфейс IManipulationProcessor, пример кода
- Интерфейс IInertiaProcessor, примеры кода
- Интерфейс IInertiaProcessor, пример кода
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 8b6471362d30b6efc9dfa0c4f07df70f014c8cb72866c92bbb04c9eb33463410
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840602"
---
# <a name="manipulation-and-inertia-sample"></a>Пример манипуляции и инерции

в примере манипуляции и инерции показано, как добавить поддержку сенсорного ввода Windows в собственные приложения на основе Windows, использующие API-интерфейс Windows Touch. Пример реализует базовые возможности API для включения перевода, вращения и масштабирования объектов и применения к ним свойств инерции. в примере также показано, как присвоить Windows сенсорным приложениям обычную поддержку мыши. На следующем рисунке показано, как выглядит пример при его запуске.

![снимок экрана, на котором показаны два поля с градиентами в примере манипуляции и инерции](images/manip-inertia-sample.png)

поля с градиентами могут управляться независимо пользователем при запуске приложения с компьютера, который поддерживает Windows Touch.

## <a name="register-the-touch-window"></a>Регистрация сенсорного окна

прежде чем вы сможете получить сенсорный ввод, сначала необходимо уведомить систему о том, что приложение является приложением Windows touch, вызвав следующую функцию:

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>Реализация интерфейса _IManipulationEventSink

Приемник событий [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) содержит три функции: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)и [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted). Эти функции обратного вызова используются интерфейсом [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и интерфейсом [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) для возврата значений, вычисленных процессорами после вызова функций [**процесстиме**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**процессупвистиме**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**процессдовнвистиме**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)и [**процессмовевистиме**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) . В следующем примере кода показан пример реализации интерфейса **_IManipulationEvents** .

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>Создание COM-объектов и Настройка интерфейсов IManipulationProcessor и IInertiaProcessor

API предоставляет реализацию интерфейсов [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . Необходимо создать экземпляр и сослаться на COM-объекты из приемника событий [**иманипулатионевентс**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) , который был реализован ранее.

## <a name="handle-wm_touch-messages"></a>Обработайте сообщения WM_TOUCH

Входные данные должны быть извлечены из [**WM_TOUCH**](wm-touchdown.md) сообщений, а затем должны быть обработаны для передачи надлежащего обработчика манипуляции.

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> Чтобы использовать функцию [**скринтоклиент**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , в приложении должна быть поддержка высокого разрешения. Дополнительные сведения о поддержке высокого DPI см. в разделе о [высоком уровне dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) в MSDN.

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>Передача структур ТАУЧИНПУТ соответствующему процессору

После извлечения данных из [**WM_TOUCH**](wm-touchdown.md) сообщений с помощью функции [**жеттаучинпутинфо**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) передавайте данные в обработчик манипуляции, вызвав функции [**процессупвистиме**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**Процессдовнвистиме**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)или [**процессмовевистиме**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) в зависимости от набора **dwFlag** , заданного в структуре [**таучинпут**](/windows/win32/api/winuser/ns-winuser-touchinput) .

> [!Note]  
> При поддержке нескольких манипуляций необходимо создать новый обработчик манипуляций, если для отправки данных в правильный объект [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) необходимо использовать **ДВИД** , определенный в структуре [**таучинпут**](/windows/win32/api/winuser/ns-winuser-touchinput) .

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>Настройка инерции в ManipulationCompleted

После вызова метода [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) объект [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) должен задать значения для объекта [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) , связанного с **IManipulationProcessor** , для вызова инерции. В следующем примере кода показано, как настроить объект **IInertiaProcessor** из метода **IManipulationProcessor** **ManipulationCompleted**.

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>Очистка COM-объектов

При закрытии приложения необходимо очистить COM-объекты. В следующем коде показано, как можно освободить ресурсы, выделенные в примере.

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>Связанные темы

пример [многофункциональной манипуляции](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [манипулирования и инерции](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows примеры сенсорного ввода](windows-touch-samples.md)