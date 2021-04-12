---
title: Размещение элемента управления проигрывателя Windows Media в приложении Windows
description: Размещение элемента управления проигрывателя Windows Media в приложении Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, программы на основе Windows
- Объектная модель проигрывателя Windows Media, программы на основе Windows
- Объектная модель, программы на основе Windows
- Проигрыватель Windows Media Mobile, программы на основе Windows
- Элемент управления ActiveX проигрывателя Windows Media, программы на основе Windows
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, программы на основе Windows
- Элемент управления ActiveX, программы на основе Windows
- Внедрение программ на основе Windows
- внедрение, программы на основе Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331451"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Размещение элемента управления проигрывателя Windows Media в приложении Windows

Для использования элемента управления ActiveX проигрывателя Windows Media (включая пользовательский интерфейс) в программе на базе Windows необходимо предоставить контейнер элементов управления ActiveX. ATL предоставляет класс **каксвиндов** для предоставления функциональных возможностей окна узла ActiveX.

Чтобы разместить элемент управления проигрывателя Windows Media с помощью класса **каксвиндов** , выполните следующие действия.

1.  Включите следующие заголовки:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Объявите переменные члена следующим образом:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Когда окно приложения будет создано, вызовите **атлаксвининит**, которое требуется при использовании главного окна ATL ActiveX.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Объявите локальные переменные для кодов возврата и, чтобы они содержали указатель на интерфейс главного окна:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Создайте главное окно:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Получение указателя интерфейса окна узла:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Создайте элемент управления проигрывателя Windows Media в окне главного приложения с помощью идентификатора класса:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Получите указатель интерфейса **ивмпплайер** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

При написании собственного кода обязательно проверьте каждый код возврата **HRESULT** на наличие ошибок.

Полный пример, демонстрирующий размещение элемента управления ActiveX проигрывателя Windows Media с помощью класса **каксвиндов** , см. в примере вмфост.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Размещение мобильного элемента управления Windows Media Player 10 в Windows CE

При разработке приложений на основе Windows CE, на которых размещается мобильный элемент управления Windows Media Player 10, необходимо установить Microsoft eMbedded Visual C++ 4,0 и пакет SDK для Pocket PC 2003 или пакет SDK для Smartphone 2003. Кроме того, в отличие от ATL для Windows, ATL для Windows CE не поддерживает модель потоков подразделений. Поэтому необходимо найти все экземпляры потоков подразделений в проекте ATL и изменить их для использования свободной потоковой обработки.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Примеры**](samples.md)
</dt> <dt>

[**Использование элемента управления проигрывателя Windows Media в программе на языке C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




