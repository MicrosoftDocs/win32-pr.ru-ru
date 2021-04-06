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
# <a name="handling-dvd-event-notifications"></a>Обработка уведомлений о событиях DVD

Навигатор DVD отправляет уведомления в окно, указанное приложением, при возникновении определенных событий, например при смене домена DVD, при обнаружении нового уровня родительского управления, а также когда Навигатор DVD собирается ввести блок угла. Параметры события могут содержать дополнительные сведения, связанные с событием. Сообщения об ошибках и предупреждения также передаются таким образом. Приложение указывает окно, которое будет выполнять обработку уведомлений о событиях с помощью указателя [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) для вызова [**сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)следующим образом:


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



В предыдущем примере m \_ HWND — это HWND окна для получения сообщений, а \_ событием DVD-диска WM \_ является определяемое приложением сообщение (больше \_ пользователя WM), которое сообщает о том, что произошло событие DVD. Само событие извлекается приложением с помощью вызова [**имедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Так как в очереди событий в любой момент времени может находиться более одного события, приложение **должно вызвать метод in в** цикле, который повторяется до тех пор, пока не будут получены все события в очереди, как показано в следующем примере кода.


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



События DVD могут содержать дополнительные сведения в параметрах *lParam1* или *lParam2* , как показано выше, когда текущее время содержится в *lParam1*. Предыдущий пример кода относится к примеру приложения DVD в Двдкоре. cpp. Полный список всех событий DVD и их параметров см. в статье [коды уведомлений о событиях DVD](dvd-notification-codes.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 



