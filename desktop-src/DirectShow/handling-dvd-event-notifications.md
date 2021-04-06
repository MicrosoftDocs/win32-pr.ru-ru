---
description: Обработка уведомлений о событиях DVD
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: Обработка уведомлений о событиях DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990254"
---
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="4f1b4-103">Обработка уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="4f1b4-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="4f1b4-104">Навигатор DVD отправляет уведомления в окно, указанное приложением, при возникновении определенных событий, например при смене домена DVD, при обнаружении нового уровня родительского управления, а также когда Навигатор DVD собирается ввести блок угла.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="4f1b4-105">Параметры события могут содержать дополнительные сведения, связанные с событием.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="4f1b4-106">Сообщения об ошибках и предупреждения также передаются таким образом.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="4f1b4-107">Приложение указывает окно, которое будет выполнять обработку уведомлений о событиях с помощью указателя [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) для вызова [**сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4f1b4-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="4f1b4-108">В предыдущем примере m \_ HWND — это HWND окна для получения сообщений, а \_ событием DVD-диска WM \_ является определяемое приложением сообщение (больше \_ пользователя WM), которое сообщает о том, что произошло событие DVD.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="4f1b4-109">Само событие извлекается приложением с помощью вызова [**имедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="4f1b4-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="4f1b4-110">Так как в очереди событий в любой момент времени может находиться более одного события, приложение **должно вызвать метод in в** цикле, который повторяется до тех пор, пока не будут получены все события в очереди, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



<span data-ttu-id="4f1b4-111">События DVD могут содержать дополнительные сведения в параметрах *lParam1* или *lParam2* , как показано выше, когда текущее время содержится в *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="4f1b4-112">Предыдущий пример кода относится к примеру приложения DVD в Двдкоре. cpp.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="4f1b4-113">Полный список всех событий DVD и их параметров см. в статье [коды уведомлений о событиях DVD](dvd-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4f1b4-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f1b4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4f1b4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f1b4-115">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="4f1b4-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



