---
title: Обновление диспетчера анимации и рисование кадров
description: Каждый раз, когда приложение планирует раскадровку, приложение должно передать текущее время в диспетчер анимации.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- Анимация объектов анимации Windows, обновление
- Анимация по объектам таймера анимации Windows, подключение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070104"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>Обновление диспетчера анимации и рисование кадров

Каждый раз, когда приложение планирует раскадровку, приложение должно передать текущее время в диспетчер анимации. Текущее время также требуется, если диспетчеру анимации нужно обновить свое состояние и задать для всех переменных анимации соответствующие значения интерполяции.

## <a name="overview"></a>Обзор

Анимация Windows поддерживает две конфигурации: управляемую приложениями анимацию и управляемую таймером анимацию.

Чтобы использовать управляемую приложением анимацию в приложении, необходимо обновить диспетчер анимации перед рисованием каждого кадра и использовать соответствующий механизм для рисования кадров, достаточного для анимации. Приложение, использующее управляемую приложением анимацию, может использовать любой механизм для определения текущего времени, но объект таймера анимации Windows возвращает точное время в единицах, принимаемых диспетчером анимации. Чтобы избежать ненужных рисунков, когда анимация не воспроизводится, необходимо также предоставить обработчик событий руководителя, чтобы начать перерисовку при планировании анимации и проверить, можно ли приостановить перерисовку после каждого кадра. Дополнительные сведения см. в разделе [анимация, управляемая приложением](scenic-animation-api-overview.md).

В конфигурации, управляемой приложением, приложение может вызвать метод [**иуианиматионманажер::-Status**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) , чтобы убедиться в том, что анимации запланированы, и продолжить рисование фреймов, если они есть. Поскольку перерисовка останавливается при отсутствии запланированной анимации, необходимо перезапустить ее при следующем планировании анимации. Приложение может зарегистрировать обработчик событий диспетчера, чтобы получать уведомления, когда состояние диспетчера анимации меняется с неактивности (в данный момент анимация не запланирована) на занятие.

Чтобы использовать в приложении анимацию, управляемую таймером, необходимо подключить диспетчер анимации к таймеру анимации и предоставить обработчик событий таймера. Когда диспетчер анимации подключен к таймеру, он может сообщить руководителю, когда состояние анимации должно обновляться как время выполнения. Приложение должно нарисовать кадр для каждого такта таймера. Диспетчер анимации может в свою очередь сообщить таймеру о том, что анимация воспроизводится, поэтому таймер может завершать свою работу во время бездействия, если перерисовка не требуется. Чтобы избежать ненужных рисунков, если анимация не воспроизводится, необходимо настроить таймер для автоматического отключения. Дополнительные сведения см. в разделе [анимация на основе таймера](scenic-animation-api-overview.md).

## <a name="example-code"></a>Пример кода

-   [Управляемая приложением анимация](#application-driven-animation)
-   [Управляемая таймером анимация](#timer-driven-animation)

### <a name="application-driven-animation"></a>Анимация Application-Driven

Следующий пример кода взят из Манажеревенсандлер. h из примеров анимации на [основе приложений](application-driven-animation-sample.md) и [макета сетки](/windows/desktop/UIAnimation/grid-layout-sample). Он определяет обработчик событий диспетчера.


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



Следующий пример кода взят из файла MainWindow. cpp из примера анимации, [управляемой приложением](application-driven-animation-sample.md)анимации Windows. см. раздел Кмаинвиндов:: Инитиализеаниматион. В этом примере создается экземпляр обработчика событий диспетчера с помощью метода [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) и передается в диспетчер анимации с помощью метода [**Иуианиматионманажер:: сетманажеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



Так как обработчик событий диспетчера содержит ссылку на основной объект окна, необходимо очистить обработчик событий диспетчера (передав **null** в [**сетманажеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) или диспетчер анимации следует полностью освободить до уничтожения главного окна.

Следующий пример кода взят из файла MainWindow. cpp в примере анимации на [основе приложения](application-driven-animation-sample.md)Windows. см. метод Кмаинвиндов:: onpain. Он вызывает метод [**иуианиматионманажер:: OnTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) для получения времени в единицах, необходимых для метода [**Иуианиматионманажер:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



Следующий пример кода взят из файла MainWindow. cpp из примеров анимации на [основе приложений](application-driven-animation-sample.md) и [макета сетки](/windows/desktop/UIAnimation/grid-layout-sample). см. метод Кмаинвиндов:: onpain. Предполагается, что приложение использует графический API, который автоматически синхронизируется с частотой обновления монитора (например, Direct2D с параметрами по умолчанию). в этом случае вызов функции [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) достаточно, чтобы код рисования вызывался повторно, когда найдет время на прорисовку следующего кадра. Вместо того, чтобы вызывать **инвалидатерект** безусловно, лучше проверить, есть ли все анимации, запланированные с помощью метода- [**Status**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a>Анимация Timer-Driven

Следующий пример кода взят из Тимеревенсандлер. h из образца анимации на [основе таймера](timer-driven-animation-sample.md)Windows. В примере кода определяется обработчик событий таймера, который делает недействительным клиентскую область окна, чтобы она вызывала перерисовку после каждого обновления состояния анимации.


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



Следующий пример кода взят из файла MainWindow. cpp из образца анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. раздел Кмаинвиндов:: Инитиализеаниматион. В этом примере создается экземпляр обработчика событий таймера с помощью метода [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) и передает его в таймер с помощью метода [**Иуианиматионтимер:: сеттимеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) . Так как обработчик событий таймера содержит ссылку на основной объект окна, необходимо очистить обработчик событий таймера (передав **значение NULL** в **сеттимеревенсандлер**) или таймер, полностью освобожденный до уничтожения главного окна.


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



Следующий пример кода взят из файла MainWindow. cpp в примере анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. метод Кмаинвиндов:: Инитиализеаниматион. Он вызывает метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) объекта диспетчера анимации для получения указателя на [**иуианиматионтимерупдатехандлер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), а затем соединяет объекты [**уианиматионманажер**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) и [**уианиматионтимер**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) , устанавливая диспетчер анимации в качестве обработчика обновления таймера с помощью метода [**иуианиматионтимер:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) . Обратите внимание, что нет необходимости явно очищать это подключение. После освобождения приложением диспетчера анимации и таймера анимации соединение будет безопасно сброшено.


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



Если **\_ \_ \_ \_ Отключение режима бездействия анимации пользовательского интерфейса** не используется, также необходимо включить таймер для запуска его тактов.

## <a name="previous-step"></a>Предыдущий шаг

Перед началом этого шага необходимо выполнить действия в статье [Создание переменных анимации](create-animation-variables.md).

## <a name="next-step"></a>Следующий шаг

После завершения этого шага следующий шаг: [чтение значений переменных анимации](updating---application-driven-animation.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Иуианиматионманажер::/Status**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**Иуианиматионманажер:: Сетманажеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**Иуианиматионманажер:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**Иуианиматионтимер:: во время**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**Иуианиматионтимер:: Сеттимерупдатехандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**уианиматионманажер**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**уианиматионтимер**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Общие сведения о анимации Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 