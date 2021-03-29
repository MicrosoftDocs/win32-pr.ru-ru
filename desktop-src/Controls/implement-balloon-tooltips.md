---
title: Как реализовать всплывающие подсказки
description: Всплывающие подсказки похожи на стандартные подсказки, но отображаются в виде мультипликационного стиля \ 0034; \ 0034; с ресурсом, указывающим на средство.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774204"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="ff9b4-103">Как реализовать всплывающие подсказки</span><span class="sxs-lookup"><span data-stu-id="ff9b4-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="ff9b4-104">Всплывающие подсказки аналогичны стандартным всплывающим подсказкам, но отображаются в виде всплывающей подсказки, указывающей на средство.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="ff9b4-105">Всплывающие подсказки могут быть либо однострочными, либо многострочными.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="ff9b4-106">Они создаются и обрабатываются во многом так же, как стандартные подсказки.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="ff9b4-107">На следующем рисунке показано расположение по умолчанию для области и прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="ff9b4-108">Если средство слишком близко к верхней части экрана, подсказка отображается ниже и справа от прямоугольника средства.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="ff9b4-109">Если средство слишком близко к правой части экрана, применяются аналогичные принципы, но всплывающая подсказка отображается слева от прямоугольника средства.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![снимок экрана: диалоговое окно; всплывающая подсказка с одной строкой текста появляется над и справа от целевого объекта](images/tt-balloon.png)

<span data-ttu-id="ff9b4-111">Можно изменить положение по умолчанию, установив флаг **TTF \_ центертип** в элементе **уфлагс** структуры всплывающей подсказки [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ff9b4-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="ff9b4-112">В этом случае область обычно указывает на центр нижнего края прямоугольника инструмента, и текстовая рамка отображается непосредственно под инструментом.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="ff9b4-113">Область подключается к текстовому прямоугольнику в центре верхнего края.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="ff9b4-114">Если средство слишком близко к нижней части экрана, то текстовая рамка центрируется над инструментом, а область подключается к центру нижнего края.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="ff9b4-115">На следующем рисунке показана всплывающая подсказка, расположенная по центру инструмента.</span><span class="sxs-lookup"><span data-stu-id="ff9b4-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![снимок экрана: диалоговое окно; всплывающая подсказка с одной строкой текста отображается в центре целевого объекта](images/tt-ballooncenter.png)

<span data-ttu-id="ff9b4-117">Если необходимо указать, где находятся точки, установите флаг **TTF \_ Track** в элементе **уфлагс** структуры ToolTip [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ff9b4-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="ff9b4-118">Затем необходимо указать координату, отправив сообщение [**ТТМ \_ траккпоситион**](ttm-trackposition.md) с координатами x и y в значении *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ff9b4-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="ff9b4-119">Если также установлен параметр **TTF \_ центертип** , то он по-прежнему указывает на расположение, указанное в сообщении **\_ траккпоситион ТТМ** .</span><span class="sxs-lookup"><span data-stu-id="ff9b4-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ff9b4-120">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="ff9b4-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ff9b4-121">Технологии</span><span class="sxs-lookup"><span data-stu-id="ff9b4-121">Technologies</span></span>

-   [<span data-ttu-id="ff9b4-122">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="ff9b4-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ff9b4-123">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ff9b4-123">Prerequisites</span></span>

-   <span data-ttu-id="ff9b4-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff9b4-124">C/C++</span></span>
-   <span data-ttu-id="ff9b4-125">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="ff9b4-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ff9b4-126">Инструкции</span><span class="sxs-lookup"><span data-stu-id="ff9b4-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="ff9b4-127">Реализация всплывающих подсказок</span><span class="sxs-lookup"><span data-stu-id="ff9b4-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="ff9b4-128">В следующем примере кода показано, как реализовать центрированную всплывающую подсказку с помощью стиля элемента управления "всплывающая подсказка **TTS \_** ".</span><span class="sxs-lookup"><span data-stu-id="ff9b4-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a><span data-ttu-id="ff9b4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ff9b4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff9b4-130">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="ff9b4-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="ff9b4-131">**Стили всплывающих подсказок**</span><span class="sxs-lookup"><span data-stu-id="ff9b4-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




