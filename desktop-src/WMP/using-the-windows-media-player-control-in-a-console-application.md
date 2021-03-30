---
title: Использование элемента управления проигрывателя Windows Media в консольном приложении
description: Использование элемента управления проигрывателя Windows Media в консольном приложении
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Проигрыватель Windows Media, консольные приложения
- Объектная модель проигрывателя Windows Media, консольные приложения
- Объектная модель, консольные приложения
- Проигрыватель Windows Media Mobile, консольные приложения
- Элемент управления ActiveX проигрывателя Windows Media, консольные приложения
- Мобильный элемент управления ActiveX проигрывателя Windows Media, консольные приложения
- Элемент управления ActiveX, консольные приложения
- внедрение консольного приложения
- внедрение, консольные приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330704"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Использование элемента управления проигрывателя Windows Media в консольном приложении

Экземпляр COM-объекта проигрывателя Windows Media можно создать напрямую с помощью **CoCreateInstance**. При этом объект **Player** не отображает пользовательский интерфейс. Однако объект по-прежнему полезен для задач, не требующих пользовательского интерфейса, таких как работа с библиотекой, воспроизведение цифровых звуковых файлов или доступ к свойствам проигрывателя.

В следующем примере кода показана простая консольная программа, которая отображает версию проигрывателя Windows Media в окне сообщения. В примере кода используется библиотека ATL для использования смарт-указателей и класса String **CComBSTR** .


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование элемента управления проигрывателя Windows Media в программе на языке C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




