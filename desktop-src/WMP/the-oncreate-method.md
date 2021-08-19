---
title: Метод onCreate
description: Метод onCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- подключаемые модули проигрыватель Windows Media, метод oncreate
- подключаемые модули, метод onCreate
- подключаемые модули пользовательского интерфейса, метод onCreate
- Подключаемые модули пользовательского интерфейса, метод onCreate
- Метод onCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac52b1c58c6799f89d29fb1ee24c09767fee26729e760b2b454f1a359bd57596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118112"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




