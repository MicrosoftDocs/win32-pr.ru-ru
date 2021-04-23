---
title: Элемент управления Slider (Справочник по элементам пользовательского интерфейса MSAA)
description: Элемент управления "ползунок", который также называется элементом управления "линейка", позволяет пользователю выбирать из диапазона значений, перемещая ползунок. Элементы управления громкостью в операционной системе Windows представляют собой ползунки.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068546"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="dab65-104">Элемент управления Slider (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="dab65-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="dab65-105">В этом разделе описываются **управляющие** объекты, предназначенные для ссылок на элементы ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="dab65-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="dab65-106">Создание **управляющих объектов-ползунков** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="dab65-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="dab65-107">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="dab65-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="dab65-108">Элемент управления "ползунок", который также называется элементом управления "линейка", позволяет пользователю выбирать из диапазона значений, перемещая ползунок.</span><span class="sxs-lookup"><span data-stu-id="dab65-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="dab65-109">Элементы управления громкостью в операционной системе Windows представляют собой ползунки.</span><span class="sxs-lookup"><span data-stu-id="dab65-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="dab65-110">Имя класса Window для элемента управления Slider имеет класс TRACKBAR \_ , который определен как "мсктлс \_ TrackBar" в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="dab65-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="dab65-111">Содержимое свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) зависит от того, является ли ползунок вертикальным или горизонтальным и какая из следующих частей элемента управления Slider запрашивается клиентом:</span><span class="sxs-lookup"><span data-stu-id="dab65-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="dab65-112">Окно Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-112">Slider window</span></span>
-   <span data-ttu-id="dab65-113">Бегунок</span><span class="sxs-lookup"><span data-stu-id="dab65-113">Slider thumb</span></span>
-   <span data-ttu-id="dab65-114">Затененная область выше (или до</span><span class="sxs-lookup"><span data-stu-id="dab65-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="dab65-115">Затененная область ниже (или справа от ползунка) бегунка</span><span class="sxs-lookup"><span data-stu-id="dab65-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="dab65-116">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="dab65-116">IAccessible Methods</span></span>

<span data-ttu-id="dab65-117">Элемент управления "ползунок" поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="dab65-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="dab65-118">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="dab65-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="dab65-119">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="dab65-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="dab65-120">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="dab65-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="dab65-121">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="dab65-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="dab65-122">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="dab65-122">IAccessible Properties</span></span>

<span data-ttu-id="dab65-123">Элемент управления "ползунок" поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="dab65-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="dab65-124">**получить \_ аккчилд**</span><span class="sxs-lookup"><span data-stu-id="dab65-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="dab65-125">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="dab65-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="dab65-126">**получить \_ аккдескриптион**</span><span class="sxs-lookup"><span data-stu-id="dab65-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="dab65-127">**получить \_ акчелп**</span><span class="sxs-lookup"><span data-stu-id="dab65-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="dab65-128">**получить \_ акчелптопик**</span><span class="sxs-lookup"><span data-stu-id="dab65-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="dab65-129">[**Get \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)— свойство **кэйбоардшорткут** является клавишей доступа ползунка, которая представляет собой подчеркнутый символ в тексте метки для ползунка.</span><span class="sxs-lookup"><span data-stu-id="dab65-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="dab65-130">Возвращаемая строка содержит символ клавиши доступа, добавленный к строке "Alt +".</span><span class="sxs-lookup"><span data-stu-id="dab65-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="dab65-131">[**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— свойство **Name** зависит от части запрашиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="dab65-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="dab65-132">Части вертикального ползунка имеют следующие имена:</span><span class="sxs-lookup"><span data-stu-id="dab65-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="dab65-133">Элемент Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-133">Slider part</span></span>                    | <span data-ttu-id="dab65-134">Имя</span><span class="sxs-lookup"><span data-stu-id="dab65-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="dab65-135">Окно Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-135">Slider window</span></span>                  | <span data-ttu-id="dab65-136">Элемент управления "статический текст", используемый в качестве метки</span><span class="sxs-lookup"><span data-stu-id="dab65-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="dab65-137">Бегунок</span><span class="sxs-lookup"><span data-stu-id="dab65-137">Slider thumb</span></span>                   | <span data-ttu-id="dab65-138">Разместить</span><span class="sxs-lookup"><span data-stu-id="dab65-138">"Position"</span></span>                          |
    | <span data-ttu-id="dab65-139">Затененный участок над бегунком ползунка</span><span class="sxs-lookup"><span data-stu-id="dab65-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="dab65-140">"Стр."</span><span class="sxs-lookup"><span data-stu-id="dab65-140">"Page up"</span></span>                           |
    | <span data-ttu-id="dab65-141">Затененная область под бегунком ползунка</span><span class="sxs-lookup"><span data-stu-id="dab65-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="dab65-142">"На страницу вниз"</span><span class="sxs-lookup"><span data-stu-id="dab65-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="dab65-143">Части горизонтального ползунка имеют следующие имена:</span><span class="sxs-lookup"><span data-stu-id="dab65-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="dab65-144">Элемент Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-144">Slider part</span></span>                              | <span data-ttu-id="dab65-145">Имя</span><span class="sxs-lookup"><span data-stu-id="dab65-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="dab65-146">Окно Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-146">Slider window</span></span>                            | <span data-ttu-id="dab65-147">Элемент управления "статический текст", используемый в качестве метки</span><span class="sxs-lookup"><span data-stu-id="dab65-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="dab65-148">Бегунок</span><span class="sxs-lookup"><span data-stu-id="dab65-148">Slider thumb</span></span>                             | <span data-ttu-id="dab65-149">Разместить</span><span class="sxs-lookup"><span data-stu-id="dab65-149">"Position"</span></span>                          |
    | <span data-ttu-id="dab65-150">Затененная область слева от бегунка</span><span class="sxs-lookup"><span data-stu-id="dab65-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="dab65-151">"Страница слева"</span><span class="sxs-lookup"><span data-stu-id="dab65-151">"Page left"</span></span>                         |
    | <span data-ttu-id="dab65-152">Затененная область справа от бегунка</span><span class="sxs-lookup"><span data-stu-id="dab65-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="dab65-153">"Страница вправо"</span><span class="sxs-lookup"><span data-stu-id="dab65-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="dab65-154">[**Get \_ Аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— **родительское** свойство кнопок со стрелками, бегунок прокрутки и затененная область с любой стороны бегунка — это ползунок.</span><span class="sxs-lookup"><span data-stu-id="dab65-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="dab65-155">Свойство **Parent** окна Slider является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна.</span><span class="sxs-lookup"><span data-stu-id="dab65-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="dab65-156">[**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— свойство **Role** зависит от части запрашиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="dab65-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="dab65-157">Элемент Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-157">Slider part</span></span>                                     | [<span data-ttu-id="dab65-158">Роль</span><span class="sxs-lookup"><span data-stu-id="dab65-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="dab65-159">Окно Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-159">Slider window</span></span>                                   | [<span data-ttu-id="dab65-160">**\_ \_ ползунок системы роли**</span><span class="sxs-lookup"><span data-stu-id="dab65-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="dab65-161">Бегунок</span><span class="sxs-lookup"><span data-stu-id="dab65-161">Slider thumb</span></span>                                    | [<span data-ttu-id="dab65-162">**\_индикатор системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="dab65-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="dab65-163">Затененные области с любой стороны бегунка</span><span class="sxs-lookup"><span data-stu-id="dab65-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="dab65-164">**\_кнопка системы \_ роли**</span><span class="sxs-lookup"><span data-stu-id="dab65-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="dab65-165">[**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[значения](object-state-constants.md) для свойства **State** зависят от части запрашиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="dab65-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="dab65-166">Элемент Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-166">Slider Part</span></span>                                     | <span data-ttu-id="dab65-167">Возможные значения состояния</span><span class="sxs-lookup"><span data-stu-id="dab65-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="dab65-168">Окно Slider</span><span class="sxs-lookup"><span data-stu-id="dab65-168">Slider window</span></span>                                   | <span data-ttu-id="dab65-169">[**Состояние \_ Системная \_ невидимая**](object-state-constants.md) система \| [**состояний \_ \_ недоступна**](object-state-constants.md) система состояний с \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ фокусом**](object-state-constants.md) системы состояния, \| [**\_ \_ нормальное состояние системы**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="dab65-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="dab65-170">Бегунок</span><span class="sxs-lookup"><span data-stu-id="dab65-170">Slider thumb</span></span>                                    | <span data-ttu-id="dab65-171">Ноль (0), это означает, что объект является видимым [**, \_ или \_ система состояния "**](object-state-constants.md) \| [**\_ \_ недоступная**](object-state-constants.md) система состояния" не имеет \| [**\_ \_ нормальной системы состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="dab65-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="dab65-172">Затененные области с любой стороны бегунка</span><span class="sxs-lookup"><span data-stu-id="dab65-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="dab65-173">Ноль (0), это означает, что объект является видимым [**, \_ или \_ система состояния "**](object-state-constants.md) \| [**\_ \_ недоступная**](object-state-constants.md) система состояния" не имеет \| [**\_ \_ нормальной системы состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="dab65-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="dab65-174">[**Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— свойство **value** для ползунка указывает положение бегунка и представляет собой строку, содержащую целое число от 0 до "100".</span><span class="sxs-lookup"><span data-stu-id="dab65-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab65-175">См. также</span><span class="sxs-lookup"><span data-stu-id="dab65-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab65-176">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="dab65-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="dab65-177">**Полоса прокрутки**</span><span class="sxs-lookup"><span data-stu-id="dab65-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




