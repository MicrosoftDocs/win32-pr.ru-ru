---
title: Как реализовать многострочные подсказки
description: Многострочные подсказки позволяют отображать текст более чем в одной строке.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774198"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="5d976-103">Как реализовать многострочные подсказки</span><span class="sxs-lookup"><span data-stu-id="5d976-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="5d976-104">Многострочные подсказки позволяют отображать текст более чем в одной строке.</span><span class="sxs-lookup"><span data-stu-id="5d976-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="5d976-105">Они поддерживаются в [версии 4,70](common-control-versions.md) и более поздних стандартных элементах управления.</span><span class="sxs-lookup"><span data-stu-id="5d976-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="5d976-106">Приложение создает многострочную подсказку, отправляя сообщение [**ТТМ \_ сетмакстипвидс**](ttm-setmaxtipwidth.md) , указав ширину отображаемого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="5d976-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="5d976-107">Текст, превышающий эту ширину, переносится на следующую строку, а не расширяет область отображаемой области.</span><span class="sxs-lookup"><span data-stu-id="5d976-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="5d976-108">Высота прямоугольника увеличивается по мере необходимости для размещения дополнительных строк.</span><span class="sxs-lookup"><span data-stu-id="5d976-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="5d976-109">Элемент управления ToolTip автоматически заключает строки в оболочку, или можно использовать сочетание символов возврата каретки или перевода строки, \\ r \\ n, для принудительного разрыва строк в определенных местах.</span><span class="sxs-lookup"><span data-stu-id="5d976-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="5d976-110">Результирующий экран показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5d976-110">The resulting display is shown in the following illustration.</span></span>

![снимок экрана: диалоговое окно с подсказкой, содержащей текст, упорядоченный в виде многострочного абзаца](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="5d976-112">Текстовый буфер, заданный членом **сзтекст** структуры [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , может размещать только 80 символов.</span><span class="sxs-lookup"><span data-stu-id="5d976-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="5d976-113">Если необходимо использовать более длинную строку, наведите элемент **Лпсзтекст** **нмттдиспинфо** на буфер, содержащий нужный текст.</span><span class="sxs-lookup"><span data-stu-id="5d976-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="5d976-114">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="5d976-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5d976-115">Технологии</span><span class="sxs-lookup"><span data-stu-id="5d976-115">Technologies</span></span>

-   [<span data-ttu-id="5d976-116">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="5d976-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5d976-117">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5d976-117">Prerequisites</span></span>

-   <span data-ttu-id="5d976-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="5d976-118">C/C++</span></span>
-   <span data-ttu-id="5d976-119">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="5d976-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5d976-120">Инструкции</span><span class="sxs-lookup"><span data-stu-id="5d976-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="5d976-121">Реализация многострочных подсказок</span><span class="sxs-lookup"><span data-stu-id="5d976-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="5d976-122">Следующий фрагмент кода является примером простого обработчика уведомлений [ТТН \_ жетдиспинфо](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5d976-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="5d976-123">Он включает многострочную подсказку, устанавливая для прямоугольника экрана значение 150 пикселей.</span><span class="sxs-lookup"><span data-stu-id="5d976-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="5d976-124">Разрыв строки вручную вставляется после первого слова, чтобы увидеть, что разрывы строк могут быть сложными и мягкими.</span><span class="sxs-lookup"><span data-stu-id="5d976-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="5d976-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5d976-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d976-126">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="5d976-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




