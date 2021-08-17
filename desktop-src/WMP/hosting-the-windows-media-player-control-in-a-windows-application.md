---
title: размещение элемента управления проигрыватель Windows Media в приложении Windows
description: размещение элемента управления проигрыватель Windows Media в приложении Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- проигрыватель Windows Media, встраивание ActiveX элемента управления
- проигрыватель Windows Media объектная модель, встраивание ActiveX элемента управления
- объектная модель, встраивание элемента управления ActiveX
- проигрыватель Windows Media мобильный, внедренный элемент управления ActiveX
- проигрыватель Windows Media элемент управления ActiveX, внедрение
- проигрыватель Windows Media управление мобильными ActiveXми, внедрение
- элемент управления ActiveX, встраивание
- проигрыватель Windows Media, программы на основе Windows
- проигрыватель Windows Media объектная модель, Windows программы
- объектная модель, программы на основе Windows
- проигрыватель Windows Media мобильные приложения, программы на основе Windows
- проигрыватель Windows Media ActiveX управления, программы на основе Windows
- проигрыватель Windows Media мобильные ActiveX управления, программы на основе Windows
- ActiveX управления, программы на основе Windows
- внедрение программ на основе Windows
- внедрение, программы на основе Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3c2b4d84194376bd16842f0a9567c83fce2aa616ed4bfef4f20f7255068e8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748281"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>размещение элемента управления проигрыватель Windows Media в приложении Windows

чтобы использовать элемент управления проигрыватель Windows Media ActiveX (включая пользовательский интерфейс) в программе на базе Windows, необходимо предоставить контейнер элемента управления ActiveX. ATL предоставляет класс **каксвиндов** для предоставления ActiveX функциональных возможностей главного окна.

чтобы разместить элемент управления проигрыватель Windows Media с помощью класса **каксвиндов** , выполните следующие действия.

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

    

3.  когда окно приложения будет создано, вызовите **атлаксвининит**, которое требуется при использовании главного окна ActiveX ATL.
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

    

7.  создайте элемент управления проигрыватель Windows Media в главном окне, используя идентификатор класса:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Получите указатель интерфейса **ивмпплайер** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

При написании собственного кода обязательно проверьте каждый код возврата **HRESULT** на наличие ошибок.

полный пример, демонстрирующий размещение элемента управления проигрыватель Windows Media ActiveX с помощью класса **каксвиндов** , см. в примере вмфост.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>размещение мобильного элемента управления проигрыватель Windows Media 10 в Windows CE

при разработке приложений на базе Windows CE, где размещается мобильный элемент управления проигрыватель Windows Media 10, необходимо установить Microsoft eMbedded Visual C++ 4,0 и пакет sdk для карманный ПК 2003 или пакет sdk для Smartphone 2003. кроме того, в отличие от atl для Windows, ATL для Windows CE не поддерживает потоковую модель апартамента. Поэтому необходимо найти все экземпляры потоков подразделений в проекте ATL и изменить их для использования свободной потоковой обработки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Примеры**](samples.md)
</dt> <dt>

[**использование элемента управления проигрыватель Windows Media в программе на языке C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




