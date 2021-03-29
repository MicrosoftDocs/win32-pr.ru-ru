---
title: Метод onpain
description: Метод onpain
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Подключаемые модули проигрывателя Windows Media, метод onpain
- подключаемые модули, метод onpain
- подключаемые модули пользовательского интерфейса, метод onpain
- Подключаемые модули пользовательского интерфейса, метод onpain
- OnPaint - метод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486976"
---
# <a name="the-onpaint-method"></a>Метод onpain

Метод onpain вызывается всякий раз, когда окно подключаемого модуля должно рисовать само себя. Это происходит, когда подключаемое окно получает \_ сообщение WM Paint, которое сопоставляется с методом onpain в схеме сообщений, описанной ранее. Мастер предоставляет реализацию этого метода, который закрашивает черный фон и помещает имя подключаемого модуля в окне подключаемого модуля. Единственным изменением, необходимым для подключаемого модуля пользовательского интерфейса поиска, является удаление кода, отображающего текст.

Для реализации этого метода используется следующий код:


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Реализация Кплугинвиндов**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




