---
title: Полоса прокрутки (Справочник по элементам пользовательского интерфейса MSAA)
description: 'Полосы прокрутки позволяют пользователю выбрать направление и расстояние для прокрутки данных в связанном окне или списке. Имя класса Window для полосы прокрутки: \ 0034; ПОЛОСА ПРОКРУТКИ \ 0034;.'
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070565"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="75571-104">Полоса прокрутки (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="75571-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="75571-105">В этом разделе описываются объекты **полоса прокрутки** для ссылки на элемент ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="75571-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="75571-106">Создание объектов **полос прокрутки** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="75571-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="75571-107">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="75571-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="75571-108">Полосы прокрутки позволяют пользователю выбрать направление и расстояние для прокрутки данных в связанном окне или списке.</span><span class="sxs-lookup"><span data-stu-id="75571-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="75571-109">Имя класса окна для полосы прокрутки — "SCROLLBAR".</span><span class="sxs-lookup"><span data-stu-id="75571-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="75571-110">Содержимое свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) зависит от того, является ли полоса прокрутки вертикальной или горизонтальной и какая из следующих частей полосы прокрутки запрашивается клиентом:</span><span class="sxs-lookup"><span data-stu-id="75571-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="75571-111">Сама полоса прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-111">The scroll bar itself</span></span>
-   <span data-ttu-id="75571-112">Кнопка со стрелкой в верхней или правой кнопке</span><span class="sxs-lookup"><span data-stu-id="75571-112">The top or right arrow button</span></span>
-   <span data-ttu-id="75571-113">Кнопка со стрелкой вниз или влево</span><span class="sxs-lookup"><span data-stu-id="75571-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="75571-114">Поле прокрутки (бегунок)</span><span class="sxs-lookup"><span data-stu-id="75571-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="75571-115">Область страницы сверху или справа</span><span class="sxs-lookup"><span data-stu-id="75571-115">The page up or page right region</span></span>
-   <span data-ttu-id="75571-116">Страница вниз или слева в области страницы</span><span class="sxs-lookup"><span data-stu-id="75571-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="75571-117">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="75571-117">IAccessible Methods</span></span>

<span data-ttu-id="75571-118">Полоса прокрутки поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="75571-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="75571-119">[**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)— сам объект полосы прокрутки и бегунок прокрутки не поддерживают метод **аккдодефаултактион** .</span><span class="sxs-lookup"><span data-stu-id="75571-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="75571-120">Для других элементов полосы прокрутки на вертикальной полосе прокрутки [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) вызывает [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea) i с сообщением [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) с параметром *wParam* со следующими значениями.</span><span class="sxs-lookup"><span data-stu-id="75571-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="75571-121">Кнопка или регион</span><span class="sxs-lookup"><span data-stu-id="75571-121">Button/Region</span></span>       | <span data-ttu-id="75571-122">Значение</span><span class="sxs-lookup"><span data-stu-id="75571-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="75571-123">Кнопка с верхней стрелкой</span><span class="sxs-lookup"><span data-stu-id="75571-123">Top arrow button</span></span>    | <span data-ttu-id="75571-124">построителя \_</span><span class="sxs-lookup"><span data-stu-id="75571-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="75571-125">Кнопка со стрелкой вниз</span><span class="sxs-lookup"><span data-stu-id="75571-125">Bottom arrow button</span></span> | <span data-ttu-id="75571-126">SB \_ линедовн</span><span class="sxs-lookup"><span data-stu-id="75571-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="75571-127">Область страницы сверху</span><span class="sxs-lookup"><span data-stu-id="75571-127">Page up region</span></span>      | <span data-ttu-id="75571-128">SB \_ PageUp</span><span class="sxs-lookup"><span data-stu-id="75571-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="75571-129">Область страницы вниз</span><span class="sxs-lookup"><span data-stu-id="75571-129">Page down region</span></span>    | <span data-ttu-id="75571-130">SB \_ PageDown</span><span class="sxs-lookup"><span data-stu-id="75571-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="75571-131">Для других элементов полосы прокрутки на горизонтальной полосе прокрутки [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) вызывает [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea) i с сообщением [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) с параметром *wParam* со следующими значениями.</span><span class="sxs-lookup"><span data-stu-id="75571-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="75571-132">Кнопка или регион</span><span class="sxs-lookup"><span data-stu-id="75571-132">Button/Region</span></span>      | <span data-ttu-id="75571-133">Значение</span><span class="sxs-lookup"><span data-stu-id="75571-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="75571-134">Кнопка со стрелкой влево</span><span class="sxs-lookup"><span data-stu-id="75571-134">Left arrow button</span></span>  | <span data-ttu-id="75571-135">SB \_ линелефт</span><span class="sxs-lookup"><span data-stu-id="75571-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="75571-136">Кнопка со стрелкой вправо</span><span class="sxs-lookup"><span data-stu-id="75571-136">Right arrow button</span></span> | <span data-ttu-id="75571-137">SB \_ линеригхт</span><span class="sxs-lookup"><span data-stu-id="75571-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="75571-138">Левая область страницы</span><span class="sxs-lookup"><span data-stu-id="75571-138">Page left region</span></span>   | <span data-ttu-id="75571-139">SB \_ пажелефт</span><span class="sxs-lookup"><span data-stu-id="75571-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="75571-140">Правая область страницы</span><span class="sxs-lookup"><span data-stu-id="75571-140">Page right region</span></span>  | <span data-ttu-id="75571-141">SB \_ пажеригхт</span><span class="sxs-lookup"><span data-stu-id="75571-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="75571-142">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="75571-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="75571-143">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="75571-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="75571-144">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="75571-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="75571-145">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="75571-145">IAccessible Properties</span></span>

<span data-ttu-id="75571-146">Полоса прокрутки поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="75571-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="75571-147">[**Get \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— свойство **ChildCount** для объекта полосы прокрутки — пять.</span><span class="sxs-lookup"><span data-stu-id="75571-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="75571-148">Для других элементов полосы прокрутки свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="75571-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="75571-149">[**Get \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)— сам объект полосы прокрутки и бегунок прокрутки не поддерживают свойство **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="75571-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="75571-150">Свойство **DefaultAction** для кнопок со стрелками и затененные области с обеих сторон ползунка прокрутки имеют значение "Press".</span><span class="sxs-lookup"><span data-stu-id="75571-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="75571-151">[**Get \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)— свойство **Description** зависит от части запрашиваемой полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="75571-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="75571-152">Части вертикальной полосы прокрутки имеют следующие описания.</span><span class="sxs-lookup"><span data-stu-id="75571-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="75571-153">Отделение</span><span class="sxs-lookup"><span data-stu-id="75571-153">Part</span></span>                | <span data-ttu-id="75571-154">Описание</span><span class="sxs-lookup"><span data-stu-id="75571-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="75571-155">Сама панель прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-155">Scroll bar itself</span></span>   | <span data-ttu-id="75571-156">"Используется для изменения вертикальной области просмотра"</span><span class="sxs-lookup"><span data-stu-id="75571-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="75571-157">Кнопка с верхней стрелкой</span><span class="sxs-lookup"><span data-stu-id="75571-157">Top arrow button</span></span>    | <span data-ttu-id="75571-158">"Перемещает вертикальное расположение вверх на одну строку"</span><span class="sxs-lookup"><span data-stu-id="75571-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="75571-159">Кнопка со стрелкой вниз</span><span class="sxs-lookup"><span data-stu-id="75571-159">Bottom arrow button</span></span> | <span data-ttu-id="75571-160">"Перемещает вертикальное расположение вниз на одну строку"</span><span class="sxs-lookup"><span data-stu-id="75571-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="75571-161">Бегунок прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-161">Scroll thumb</span></span>        | <span data-ttu-id="75571-162">"Обозначает текущее расположение по вертикали и может быть перемещено, чтобы изменить его напрямую"</span><span class="sxs-lookup"><span data-stu-id="75571-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="75571-163">Область страницы сверху</span><span class="sxs-lookup"><span data-stu-id="75571-163">Page up region</span></span>      | <span data-ttu-id="75571-164">"Перемещает вертикальное расположение на несколько строк"</span><span class="sxs-lookup"><span data-stu-id="75571-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="75571-165">Область страницы вниз</span><span class="sxs-lookup"><span data-stu-id="75571-165">Page down region</span></span>    | <span data-ttu-id="75571-166">"Обозначает текущее расположение по вертикали и может быть перемещено, чтобы изменить его напрямую"</span><span class="sxs-lookup"><span data-stu-id="75571-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="75571-167">Части горизонтальной полосы прокрутки имеют следующие описания.</span><span class="sxs-lookup"><span data-stu-id="75571-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="75571-168">Отделение</span><span class="sxs-lookup"><span data-stu-id="75571-168">Part</span></span>               | <span data-ttu-id="75571-169">Описание</span><span class="sxs-lookup"><span data-stu-id="75571-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="75571-170">Сама панель прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-170">Scroll bar itself</span></span>  | <span data-ttu-id="75571-171">"Используется для изменения горизонтальной области просмотра"</span><span class="sxs-lookup"><span data-stu-id="75571-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="75571-172">Кнопка со стрелкой влево</span><span class="sxs-lookup"><span data-stu-id="75571-172">Left arrow button</span></span>  | <span data-ttu-id="75571-173">"Перемещает горизонтальную точку влево на один столбец"</span><span class="sxs-lookup"><span data-stu-id="75571-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="75571-174">Кнопка со стрелкой вправо</span><span class="sxs-lookup"><span data-stu-id="75571-174">Right arrow button</span></span> | <span data-ttu-id="75571-175">' Перемещает горизонтальное расположение вправо на один столбец "</span><span class="sxs-lookup"><span data-stu-id="75571-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="75571-176">Бегунок прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-176">Scroll thumb</span></span>       | <span data-ttu-id="75571-177">"Обозначает текущее расположение по горизонтали и может быть перемещено, чтобы изменить его напрямую"</span><span class="sxs-lookup"><span data-stu-id="75571-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="75571-178">Левая область страницы</span><span class="sxs-lookup"><span data-stu-id="75571-178">Page left region</span></span>   | <span data-ttu-id="75571-179">"Перемещает горизонтальную точку влево на несколько столбцов"</span><span class="sxs-lookup"><span data-stu-id="75571-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="75571-180">Правая область страницы</span><span class="sxs-lookup"><span data-stu-id="75571-180">Page right region</span></span>  | <span data-ttu-id="75571-181">"Обозначает текущее расположение по вертикали и может быть перемещено, чтобы изменить его напрямую"</span><span class="sxs-lookup"><span data-stu-id="75571-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="75571-182">**получить \_ акчелп**</span><span class="sxs-lookup"><span data-stu-id="75571-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="75571-183">**получить \_ акчелптопик**</span><span class="sxs-lookup"><span data-stu-id="75571-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="75571-184">[**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— свойство **Name** зависит от части запрашиваемой полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="75571-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="75571-185">Части вертикальной полосы прокрутки имеют следующие имена.</span><span class="sxs-lookup"><span data-stu-id="75571-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="75571-186">Отделение</span><span class="sxs-lookup"><span data-stu-id="75571-186">Part</span></span>                | <span data-ttu-id="75571-187">Имя</span><span class="sxs-lookup"><span data-stu-id="75571-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="75571-188">Окно полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-188">Scroll bar window</span></span>   | <span data-ttu-id="75571-189">Вертикаль</span><span class="sxs-lookup"><span data-stu-id="75571-189">"Vertical"</span></span>  |
    | <span data-ttu-id="75571-190">Кнопка с верхней стрелкой</span><span class="sxs-lookup"><span data-stu-id="75571-190">Top arrow button</span></span>    | <span data-ttu-id="75571-191">"На строку вверх"</span><span class="sxs-lookup"><span data-stu-id="75571-191">"Line up"</span></span>   |
    | <span data-ttu-id="75571-192">Кнопка со стрелкой вниз</span><span class="sxs-lookup"><span data-stu-id="75571-192">Bottom arrow button</span></span> | <span data-ttu-id="75571-193">"На строку вниз"</span><span class="sxs-lookup"><span data-stu-id="75571-193">"Line down"</span></span> |
    | <span data-ttu-id="75571-194">Бегунок прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-194">Scroll thumb</span></span>        | <span data-ttu-id="75571-195">Разместить</span><span class="sxs-lookup"><span data-stu-id="75571-195">"Position"</span></span>  |
    | <span data-ttu-id="75571-196">Область страницы сверху</span><span class="sxs-lookup"><span data-stu-id="75571-196">Page up region</span></span>      | <span data-ttu-id="75571-197">"Стр."</span><span class="sxs-lookup"><span data-stu-id="75571-197">"Page up"</span></span>   |
    | <span data-ttu-id="75571-198">Область страницы вниз</span><span class="sxs-lookup"><span data-stu-id="75571-198">Page down region</span></span>    | <span data-ttu-id="75571-199">"На страницу вниз"</span><span class="sxs-lookup"><span data-stu-id="75571-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="75571-200">Части горизонтальной полосы прокрутки имеют следующие имена.</span><span class="sxs-lookup"><span data-stu-id="75571-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="75571-201">Отделение</span><span class="sxs-lookup"><span data-stu-id="75571-201">Part</span></span>               | <span data-ttu-id="75571-202">Имя</span><span class="sxs-lookup"><span data-stu-id="75571-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="75571-203">Окно полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-203">Scroll bar window</span></span>  | <span data-ttu-id="75571-204">Горизонтал</span><span class="sxs-lookup"><span data-stu-id="75571-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="75571-205">Кнопка со стрелкой влево</span><span class="sxs-lookup"><span data-stu-id="75571-205">Left arrow button</span></span>  | <span data-ttu-id="75571-206">"Столбец Left"</span><span class="sxs-lookup"><span data-stu-id="75571-206">"Column left"</span></span>  |
    | <span data-ttu-id="75571-207">Кнопка со стрелкой вправо</span><span class="sxs-lookup"><span data-stu-id="75571-207">Right arrow button</span></span> | <span data-ttu-id="75571-208">"Столбец справа"</span><span class="sxs-lookup"><span data-stu-id="75571-208">"Column right"</span></span> |
    | <span data-ttu-id="75571-209">Бегунок прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-209">Scroll thumb</span></span>       | <span data-ttu-id="75571-210">Разместить</span><span class="sxs-lookup"><span data-stu-id="75571-210">"Position"</span></span>     |
    | <span data-ttu-id="75571-211">Правая область страницы</span><span class="sxs-lookup"><span data-stu-id="75571-211">Page right region</span></span>  | <span data-ttu-id="75571-212">"Страница вправо"</span><span class="sxs-lookup"><span data-stu-id="75571-212">"Page right"</span></span>   |
    | <span data-ttu-id="75571-213">Левая область страницы</span><span class="sxs-lookup"><span data-stu-id="75571-213">Page left region</span></span>   | <span data-ttu-id="75571-214">"Страница слева"</span><span class="sxs-lookup"><span data-stu-id="75571-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="75571-215">[**Получение \_ Аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— **родительское** свойство кнопок со стрелками, бегунок прокрутки и затененная область с любой стороны бегунка — это окно полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="75571-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="75571-216">Свойство **Parent** окна полосы прокрутки является окном ( \_ окно системы ролей \_ ), которое окружает элемент управления и имеет то же имя  свойства и класса окна.</span><span class="sxs-lookup"><span data-stu-id="75571-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="75571-217">[**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— свойство **Role** зависит от части запрашиваемой полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="75571-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="75571-218">Части полосы прокрутки имеют следующие роли.</span><span class="sxs-lookup"><span data-stu-id="75571-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="75571-219">Отделение</span><span class="sxs-lookup"><span data-stu-id="75571-219">Part</span></span>                                                  | <span data-ttu-id="75571-220">Роль</span><span class="sxs-lookup"><span data-stu-id="75571-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="75571-221">Сама панель прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="75571-222">**\_ \_ полоса прокрутки системы роли**</span><span class="sxs-lookup"><span data-stu-id="75571-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="75571-223">Кнопки со стрелками сверху, вниз, влево и вправо</span><span class="sxs-lookup"><span data-stu-id="75571-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="75571-224">**\_кнопка системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="75571-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="75571-225">Бегунок прокрутки</span><span class="sxs-lookup"><span data-stu-id="75571-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="75571-226">**\_индикатор системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="75571-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="75571-227">Область сверху, Page Down, страница слева и область страницы справа</span><span class="sxs-lookup"><span data-stu-id="75571-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="75571-228">**\_кнопка системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="75571-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="75571-229">[**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— свойство **State** каждого компонента полосы прокрутки содержит сочетание следующих [значений](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="75571-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="75571-230">Состояние</span><span class="sxs-lookup"><span data-stu-id="75571-230">State</span></span>                                                                                 | <span data-ttu-id="75571-231">Значение</span><span class="sxs-lookup"><span data-stu-id="75571-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="75571-232">**\_Система состояний \_ невидима**</span><span class="sxs-lookup"><span data-stu-id="75571-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="75571-233">Для самой полосы прокрутки это означает, что указанная вертикальная или горизонтальная полоса прокрутки не существует.</span><span class="sxs-lookup"><span data-stu-id="75571-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="75571-234">При переходе на следующую страницу вверх или вниз это означает, что бегунок размещается так, что область не существует.</span><span class="sxs-lookup"><span data-stu-id="75571-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="75571-235">**\_Система состояний \_**</span><span class="sxs-lookup"><span data-stu-id="75571-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="75571-236">Для самой полосы прокрутки это означает, что размер окна изменяется таким, что заданная вертикальная или горизонтальная полоса прокрутки в данный момент не отображается.</span><span class="sxs-lookup"><span data-stu-id="75571-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="75571-237">**\_Система состояний \_ нажата**</span><span class="sxs-lookup"><span data-stu-id="75571-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="75571-238">Нажата кнопка со стрелкой или область страницы.</span><span class="sxs-lookup"><span data-stu-id="75571-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="75571-239">**\_Система состояний \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="75571-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="75571-240">Компонент отключен.</span><span class="sxs-lookup"><span data-stu-id="75571-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="75571-241">[**Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— свойство **value** для окна полосы прокрутки указывает на расположение полосы прокрутки и представляет собой строку, содержащую целое число от 0 до "100".</span><span class="sxs-lookup"><span data-stu-id="75571-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="75571-242">См. также</span><span class="sxs-lookup"><span data-stu-id="75571-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75571-243">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="75571-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 