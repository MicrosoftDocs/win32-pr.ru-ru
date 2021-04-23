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
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="8c3e0-105">Обновление диспетчера анимации и рисование кадров</span><span class="sxs-lookup"><span data-stu-id="8c3e0-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="8c3e0-106">Каждый раз, когда приложение планирует раскадровку, приложение должно передать текущее время в диспетчер анимации.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="8c3e0-107">Текущее время также требуется, если диспетчеру анимации нужно обновить свое состояние и задать для всех переменных анимации соответствующие значения интерполяции.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="8c3e0-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="8c3e0-108">Overview</span></span>

<span data-ttu-id="8c3e0-109">Анимация Windows поддерживает две конфигурации: управляемую приложениями анимацию и управляемую таймером анимацию.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="8c3e0-110">Чтобы использовать управляемую приложением анимацию в приложении, необходимо обновить диспетчер анимации перед рисованием каждого кадра и использовать соответствующий механизм для рисования кадров, достаточного для анимации.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="8c3e0-111">Приложение, использующее управляемую приложением анимацию, может использовать любой механизм для определения текущего времени, но объект таймера анимации Windows возвращает точное время в единицах, принимаемых диспетчером анимации.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="8c3e0-112">Чтобы избежать ненужных рисунков, когда анимация не воспроизводится, необходимо также предоставить обработчик событий руководителя, чтобы начать перерисовку при планировании анимации и проверить, можно ли приостановить перерисовку после каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="8c3e0-113">Дополнительные сведения см. в разделе [анимация, управляемая приложением](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c3e0-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="8c3e0-114">В конфигурации, управляемой приложением, приложение может вызвать метод [**иуианиматионманажер::-Status**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) , чтобы убедиться в том, что анимации запланированы, и продолжить рисование фреймов, если они есть.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="8c3e0-115">Поскольку перерисовка останавливается при отсутствии запланированной анимации, необходимо перезапустить ее при следующем планировании анимации.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="8c3e0-116">Приложение может зарегистрировать обработчик событий диспетчера, чтобы получать уведомления, когда состояние диспетчера анимации меняется с неактивности (в данный момент анимация не запланирована) на занятие.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="8c3e0-117">Чтобы использовать в приложении анимацию, управляемую таймером, необходимо подключить диспетчер анимации к таймеру анимации и предоставить обработчик событий таймера.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="8c3e0-118">Когда диспетчер анимации подключен к таймеру, он может сообщить руководителю, когда состояние анимации должно обновляться как время выполнения.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="8c3e0-119">Приложение должно нарисовать кадр для каждого такта таймера.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="8c3e0-120">Диспетчер анимации может в свою очередь сообщить таймеру о том, что анимация воспроизводится, поэтому таймер может завершать свою работу во время бездействия, если перерисовка не требуется.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="8c3e0-121">Чтобы избежать ненужных рисунков, если анимация не воспроизводится, необходимо настроить таймер для автоматического отключения.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="8c3e0-122">Дополнительные сведения см. в разделе [анимация на основе таймера](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c3e0-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="8c3e0-123">Пример кода</span><span class="sxs-lookup"><span data-stu-id="8c3e0-123">Example Code</span></span>

-   [<span data-ttu-id="8c3e0-124">Управляемая приложением анимация</span><span class="sxs-lookup"><span data-stu-id="8c3e0-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="8c3e0-125">Управляемая таймером анимация</span><span class="sxs-lookup"><span data-stu-id="8c3e0-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="8c3e0-126">Анимация Application-Driven</span><span class="sxs-lookup"><span data-stu-id="8c3e0-126">Application-Driven Animation</span></span>

<span data-ttu-id="8c3e0-127">Следующий пример кода взят из Манажеревенсандлер. h из примеров анимации на [основе приложений](application-driven-animation-sample.md) и [макета сетки](/windows/desktop/UIAnimation/grid-layout-sample).</span><span class="sxs-lookup"><span data-stu-id="8c3e0-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="8c3e0-128">Он определяет обработчик событий диспетчера.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-128">It defines the manager event handler.</span></span>


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



<span data-ttu-id="8c3e0-129">Следующий пример кода взят из файла MainWindow. cpp из примера анимации, [управляемой приложением](application-driven-animation-sample.md)анимации Windows. см. раздел Кмаинвиндов:: Инитиализеаниматион.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="8c3e0-130">В этом примере создается экземпляр обработчика событий диспетчера с помощью метода [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) и передается в диспетчер анимации с помощью метода [**Иуианиматионманажер:: сетманажеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="8c3e0-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


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



<span data-ttu-id="8c3e0-131">Так как обработчик событий диспетчера содержит ссылку на основной объект окна, необходимо очистить обработчик событий диспетчера (передав **null** в [**сетманажеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) или диспетчер анимации следует полностью освободить до уничтожения главного окна.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="8c3e0-132">Следующий пример кода взят из файла MainWindow. cpp в примере анимации на [основе приложения](application-driven-animation-sample.md)Windows. см. метод Кмаинвиндов:: onpain.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="8c3e0-133">Он вызывает метод [**иуианиматионманажер:: OnTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) для получения времени в единицах, необходимых для метода [**Иуианиматионманажер:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .</span><span class="sxs-lookup"><span data-stu-id="8c3e0-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


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



<span data-ttu-id="8c3e0-134">Следующий пример кода взят из файла MainWindow. cpp из примеров анимации на [основе приложений](application-driven-animation-sample.md) и [макета сетки](/windows/desktop/UIAnimation/grid-layout-sample). см. метод Кмаинвиндов:: onpain.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="8c3e0-135">Предполагается, что приложение использует графический API, который автоматически синхронизируется с частотой обновления монитора (например, Direct2D с параметрами по умолчанию). в этом случае вызов функции [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) достаточно, чтобы код рисования вызывался повторно, когда найдет время на прорисовку следующего кадра.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="8c3e0-136">Вместо того, чтобы вызывать **инвалидатерект** безусловно, лучше проверить, есть ли все анимации, запланированные с помощью метода- [**Status**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span><span class="sxs-lookup"><span data-stu-id="8c3e0-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


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



### <a name="timer-driven-animation"></a><span data-ttu-id="8c3e0-137">Анимация Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="8c3e0-137">Timer-Driven Animation</span></span>

<span data-ttu-id="8c3e0-138">Следующий пример кода взят из Тимеревенсандлер. h из образца анимации на [основе таймера](timer-driven-animation-sample.md)Windows.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="8c3e0-139">В примере кода определяется обработчик событий таймера, который делает недействительным клиентскую область окна, чтобы она вызывала перерисовку после каждого обновления состояния анимации.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


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



<span data-ttu-id="8c3e0-140">Следующий пример кода взят из файла MainWindow. cpp из образца анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. раздел Кмаинвиндов:: Инитиализеаниматион.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="8c3e0-141">В этом примере создается экземпляр обработчика событий таймера с помощью метода [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) и передает его в таймер с помощью метода [**Иуианиматионтимер:: сеттимеревенсандлер**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="8c3e0-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="8c3e0-142">Так как обработчик событий таймера содержит ссылку на основной объект окна, необходимо очистить обработчик событий таймера (передав **значение NULL** в **сеттимеревенсандлер**) или таймер, полностью освобожденный до уничтожения главного окна.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


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



<span data-ttu-id="8c3e0-143">Следующий пример кода взят из файла MainWindow. cpp в примере анимации на основе [таймера](timer-driven-animation-sample.md)Windows. см. метод Кмаинвиндов:: Инитиализеаниматион.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="8c3e0-144">Он вызывает метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) объекта диспетчера анимации для получения указателя на [**иуианиматионтимерупдатехандлер**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), а затем соединяет объекты [**уианиматионманажер**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) и [**уианиматионтимер**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) , устанавливая диспетчер анимации в качестве обработчика обновления таймера с помощью метода [**иуианиматионтимер:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) .</span><span class="sxs-lookup"><span data-stu-id="8c3e0-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="8c3e0-145">Обратите внимание, что нет необходимости явно очищать это подключение. После освобождения приложением диспетчера анимации и таймера анимации соединение будет безопасно сброшено.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


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



<span data-ttu-id="8c3e0-146">Если **\_ \_ \_ \_ Отключение режима бездействия анимации пользовательского интерфейса** не используется, также необходимо включить таймер для запуска его тактов.</span><span class="sxs-lookup"><span data-stu-id="8c3e0-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="8c3e0-147">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="8c3e0-147">Previous Step</span></span>

<span data-ttu-id="8c3e0-148">Перед началом этого шага необходимо выполнить действия в статье [Создание переменных анимации](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="8c3e0-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="8c3e0-149">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="8c3e0-149">Next Step</span></span>

<span data-ttu-id="8c3e0-150">После завершения этого шага следующий шаг: [чтение значений переменных анимации](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="8c3e0-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c3e0-151">См. также</span><span class="sxs-lookup"><span data-stu-id="8c3e0-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c3e0-152">**Иуианиматионманажер::/Status**</span><span class="sxs-lookup"><span data-stu-id="8c3e0-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="8c3e0-153">**Иуианиматионманажер:: Сетманажеревенсандлер**</span><span class="sxs-lookup"><span data-stu-id="8c3e0-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="8c3e0-154">**Иуианиматионманажер:: Update**</span><span class="sxs-lookup"><span data-stu-id="8c3e0-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="8c3e0-155">**Иуианиматионтимер:: во время**</span><span class="sxs-lookup"><span data-stu-id="8c3e0-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="8c3e0-156">**Иуианиматионтимер:: Сеттимерупдатехандлер**</span><span class="sxs-lookup"><span data-stu-id="8c3e0-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="8c3e0-157">[**уианиматионманажер**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c3e0-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8c3e0-158">[**уианиматионтимер**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c3e0-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8c3e0-159">Общие сведения о анимации Windows</span><span class="sxs-lookup"><span data-stu-id="8c3e0-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 