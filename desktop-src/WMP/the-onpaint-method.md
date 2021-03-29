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
# <a name="the-onpaint-method"></a><span data-ttu-id="161eb-108">Метод onpain</span><span class="sxs-lookup"><span data-stu-id="161eb-108">The OnPaint Method</span></span>

<span data-ttu-id="161eb-109">Метод onpain вызывается всякий раз, когда окно подключаемого модуля должно рисовать само себя.</span><span class="sxs-lookup"><span data-stu-id="161eb-109">The OnPaint method is called whenever the plug-in window should paint itself.</span></span> <span data-ttu-id="161eb-110">Это происходит, когда подключаемое окно получает \_ сообщение WM Paint, которое сопоставляется с методом onpain в схеме сообщений, описанной ранее.</span><span class="sxs-lookup"><span data-stu-id="161eb-110">This occurs when the plug-in window receives a WM\_PAINT message, which is mapped to the OnPaint method in the message map described earlier.</span></span> <span data-ttu-id="161eb-111">Мастер предоставляет реализацию этого метода, который закрашивает черный фон и помещает имя подключаемого модуля в окне подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="161eb-111">The wizard provides an implementation of this method that paints the background black and places the name of the plug-in in the plug-in window.</span></span> <span data-ttu-id="161eb-112">Единственным изменением, необходимым для подключаемого модуля пользовательского интерфейса поиска, является удаление кода, отображающего текст.</span><span class="sxs-lookup"><span data-stu-id="161eb-112">The only modification that is necessary for the Search UI plug-in is the removal of the code that displays the text.</span></span>

<span data-ttu-id="161eb-113">Для реализации этого метода используется следующий код:</span><span class="sxs-lookup"><span data-stu-id="161eb-113">The following code is used to implement this method:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="161eb-114">См. также</span><span class="sxs-lookup"><span data-stu-id="161eb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="161eb-115">**Реализация Кплугинвиндов**</span><span class="sxs-lookup"><span data-stu-id="161eb-115">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




