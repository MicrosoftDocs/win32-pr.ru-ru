---
title: Реализация In-Place подсказок
description: Подсказки на месте используются для вывода текстовых строк для объектов, которые были обрезаны. Иллюстрация см. в разделе о элементах управления ToolTip.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070882"
---
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="a6af4-104">Реализация In-Place подсказок</span><span class="sxs-lookup"><span data-stu-id="a6af4-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="a6af4-105">Подсказки на месте используются для вывода текстовых строк для объектов, которые были обрезаны.</span><span class="sxs-lookup"><span data-stu-id="a6af4-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="a6af4-106">Иллюстрация см. в разделе [о элементах управления ToolTip](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a6af4-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="a6af4-107">Разность между обычными и встроенными подсказками размещается.</span><span class="sxs-lookup"><span data-stu-id="a6af4-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="a6af4-108">По умолчанию при наведении указателя мыши на область с связанной с ней подсказкой подсказка отображается рядом с областью.</span><span class="sxs-lookup"><span data-stu-id="a6af4-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="a6af4-109">Однако подсказки являются окнами, и их можно размещать в любом месте, вызвав [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="a6af4-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="a6af4-110">Создание подсказок на месте заключается в размещении окна подсказки, чтобы оно находилось в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="a6af4-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a6af4-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="a6af4-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a6af4-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="a6af4-112">Technologies</span></span>

-   [<span data-ttu-id="a6af4-113">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="a6af4-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a6af4-114">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a6af4-114">Prerequisites</span></span>

-   <span data-ttu-id="a6af4-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="a6af4-115">C/C++</span></span>
-   <span data-ttu-id="a6af4-116">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="a6af4-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a6af4-117">Инструкции</span><span class="sxs-lookup"><span data-stu-id="a6af4-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="a6af4-118">Размещение подсказки In-Place</span><span class="sxs-lookup"><span data-stu-id="a6af4-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="a6af4-119">При размещении подсказки на месте необходимо отследить три прямоугольника:</span><span class="sxs-lookup"><span data-stu-id="a6af4-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="a6af4-120">Прямоугольник, который окружает весь текст метки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="a6af4-121">Прямоугольник, который окружает текст подсказки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="a6af4-122">Текст подсказки идентичен полному тексту метки, и обычно имеет тот же размер и шрифт.</span><span class="sxs-lookup"><span data-stu-id="a6af4-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="a6af4-123">Поэтому два текстовых прямоугольника обычно имеют одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="a6af4-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="a6af4-124">Прямоугольник окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-124">The tooltip window rectangle.</span></span> <span data-ttu-id="a6af4-125">Этот прямоугольник немного больше, чем прямоугольник текста подсказки, который он заключает.</span><span class="sxs-lookup"><span data-stu-id="a6af4-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="a6af4-126">Три прямоугольника показаны на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="a6af4-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="a6af4-127">Скрытая часть текста метки обозначается серым фоном.</span><span class="sxs-lookup"><span data-stu-id="a6af4-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![на схеме показана длинная строка, половина которой имеет серый фон, то есть та же строка в более крупном прямоугольнике окна подсказки.](images/inplace.png)

<span data-ttu-id="a6af4-129">Чтобы создать подсказку на месте, необходимо разместить прямоугольник текста подсказки таким образом, чтобы он накладывается на текстовую рамку метки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="a6af4-130">Процедура выровняйте два прямоугольника относительно проста:</span><span class="sxs-lookup"><span data-stu-id="a6af4-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="a6af4-131">Определите прямоугольник текста метки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="a6af4-132">Поместите окно подсказки таким образом, чтобы прямоугольник текста подсказки накладывается на текстовую рамку метки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="a6af4-133">На практике обычно достаточно Выровняйте верхний левый угол двух текстовых прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="a6af4-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="a6af4-134">Попытка изменить размер прямоугольника текста подсказки в точности соответствует текстовому прямоугольнику метки может вызвать проблемы с отображением всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="a6af4-135">Проблема с этой простой схемой заключается в том, что невозможно разместить прямоугольник текста подсказки напрямую.</span><span class="sxs-lookup"><span data-stu-id="a6af4-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="a6af4-136">Вместо этого необходимо разместить прямоугольник окна подсказки достаточно далеко над и слева от текстового прямоугольника метки, чтобы углы двух текстовых прямоугольников совпадали.</span><span class="sxs-lookup"><span data-stu-id="a6af4-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="a6af4-137">Иными словами, необходимо знать смещение между прямоугольником окна подсказки и вложенным текстовым прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="a6af4-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="a6af4-138">Как правило, нет простого способа определить это смещение.</span><span class="sxs-lookup"><span data-stu-id="a6af4-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="a6af4-139">Реализация In-Place подсказок</span><span class="sxs-lookup"><span data-stu-id="a6af4-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="a6af4-140">В следующем фрагменте кода показано, как использовать сообщение [**ТТМ \_ аджустрект**](ttm-adjustrect.md) в обработчике ТТН, чтобы отобразить подсказку на месте. [ \_](ttn-show.md)</span><span class="sxs-lookup"><span data-stu-id="a6af4-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="a6af4-141">Приложение указывает, что текст метки усекается путем задания для закрытой переменной *фмистрингистрункатед* значения **true**.</span><span class="sxs-lookup"><span data-stu-id="a6af4-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="a6af4-142">Обработчик вызывает определяемую приложением функцию **жетмитемрект** для получения текстового прямоугольника метки.</span><span class="sxs-lookup"><span data-stu-id="a6af4-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="a6af4-143">Этот прямоугольник передается элементу управления ToolTip с помощью **ТТМ \_ аджустрект**, который возвращает соответствующий прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="a6af4-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="a6af4-144">Затем вызывается [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) для позиционирования подсказки на метке.</span><span class="sxs-lookup"><span data-stu-id="a6af4-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



<span data-ttu-id="a6af4-145">В этом примере не изменяется размер подсказки, а только ее ее расположение.</span><span class="sxs-lookup"><span data-stu-id="a6af4-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="a6af4-146">Два текстовых прямоугольника вычисляются по левому верхнему краю, но не обязательно с одинаковыми размерами.</span><span class="sxs-lookup"><span data-stu-id="a6af4-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="a6af4-147">На практике разница обычно мала, и этот подход рекомендуется для большинства целей.</span><span class="sxs-lookup"><span data-stu-id="a6af4-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="a6af4-148">Хотя вы можете, в принципе, использовать [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) для изменения размера, а также изменить расположение подсказки, это может привести к непредсказуемым последствиям.</span><span class="sxs-lookup"><span data-stu-id="a6af4-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6af4-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6af4-149">Remarks</span></span>

<span data-ttu-id="a6af4-150">Стандартные элементы управления [версии 5,80](common-control-versions.md) упрощают использование подсказок на месте путем добавления нового сообщения, [**ТТМ \_ аджустрект**](ttm-adjustrect.md).</span><span class="sxs-lookup"><span data-stu-id="a6af4-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="a6af4-151">Отправьте это сообщение с координатами текстового прямоугольника метки, на который должна накладываться всплывающая подсказка, и возвращает координаты соответствующего прямоугольника окна подсказок с соответствующим положением.</span><span class="sxs-lookup"><span data-stu-id="a6af4-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6af4-152">См. также</span><span class="sxs-lookup"><span data-stu-id="a6af4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6af4-153">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="a6af4-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 