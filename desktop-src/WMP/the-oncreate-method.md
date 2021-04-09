---
title: Метод onCreate
description: Метод onCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Подключаемые модули проигрывателя Windows Media, метод onCreate
- подключаемые модули, метод onCreate
- подключаемые модули пользовательского интерфейса, метод onCreate
- Подключаемые модули пользовательского интерфейса, метод onCreate
- Метод onCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887747"
---
# <a name="the-oncreate-method"></a>Метод onCreate

Метод onCreate вызывается при первом создании подключаемого окна.

Для реализации этого метода используется следующий код:


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



Этот метод создает кнопку **поиска** и связывает ее с \_ идентификатором команды поиска IDC, который определен в начале файла:


```C++
#define IDC_SEARCH 2000

```



Этот идентификатор команды сопоставляется с методом onSearch в разделе схемы сообщений, описанном выше.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




