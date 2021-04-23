---
title: Всплывающее меню (Справочник по элементам пользовательского интерфейса MSAA)
description: Во всплывающем меню отображается список команд меню.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888732"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="0b68d-103">Всплывающее меню (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="0b68d-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="0b68d-104">В этом разделе описываются объекты **всплывающего меню** в справочнике по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="0b68d-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="0b68d-105">Создание объектов **всплывающего меню** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="0b68d-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="0b68d-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="0b68d-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="0b68d-107">Во всплывающем меню отображается список команд меню.</span><span class="sxs-lookup"><span data-stu-id="0b68d-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="0b68d-108">Microsoft Active Accessibility создает всплывающий объект меню при открытии пункта меню в строке меню.</span><span class="sxs-lookup"><span data-stu-id="0b68d-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="0b68d-109">Кроме того, Microsoft Active Accessibility создает всплывающие меню для контекстных меню, которые отображаются, когда пользователь щелкает правой кнопкой мыши элемент пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0b68d-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="0b68d-110">Имя класса окон для всплывающего меню — " \# 32768".</span><span class="sxs-lookup"><span data-stu-id="0b68d-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="0b68d-111">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="0b68d-111">IAccessible Methods</span></span>

<span data-ttu-id="0b68d-112">Всплывающее меню поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="0b68d-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="0b68d-113">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="0b68d-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="0b68d-114">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="0b68d-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="0b68d-115">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="0b68d-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="0b68d-116">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="0b68d-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="0b68d-117">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="0b68d-117">IAccessible Properties</span></span>

<span data-ttu-id="0b68d-118">Всплывающее меню поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="0b68d-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="0b68d-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="0b68d-119">Property</span></span>                                                                 | <span data-ttu-id="0b68d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b68d-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b68d-121">**получить \_ аккчилд**</span><span class="sxs-lookup"><span data-stu-id="0b68d-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="0b68d-122">Извлекает [**IDispatch**](idispatch-interface.md) для указанного элемента меню.</span><span class="sxs-lookup"><span data-stu-id="0b68d-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="0b68d-123">Идентификаторы дочерних элементов меню нумеруются последовательно сверху вниз, начиная с единицы.</span><span class="sxs-lookup"><span data-stu-id="0b68d-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0b68d-124">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="0b68d-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="0b68d-125">Свойство **ChildCount** — это число пунктов меню в меню, включая разделители меню.</span><span class="sxs-lookup"><span data-stu-id="0b68d-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0b68d-126">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="0b68d-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0b68d-127">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="0b68d-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="0b68d-128">Свойство **имя** всплывающего меню совпадает с именем меню.</span><span class="sxs-lookup"><span data-stu-id="0b68d-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="0b68d-129">Свойство **Name** контекстного меню — «context».</span><span class="sxs-lookup"><span data-stu-id="0b68d-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="0b68d-130">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="0b68d-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="0b68d-131">**Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает всплывающее меню и имеет **то же имя** свойства и класса окна, что и всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="0b68d-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0b68d-132">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="0b68d-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="0b68d-133">Свойство **Role** имеет [**роль \_ System \_ менупопуп**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0b68d-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0b68d-134">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="0b68d-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="0b68d-135">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): [**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="0b68d-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="0b68d-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b68d-136">Notes</span></span>

-   <span data-ttu-id="0b68d-137">Объекты всплывающего меню не активируют события [**\_ \_ создания объектов событий**](event-constants.md) и [**\_ \_ уничтожения объектов событий**](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="0b68d-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="0b68d-138">Меню с несколькими столбцами не поддерживают флаги [**навдир \_ Left**](navigation-constants.md) или [**навдир \_ right**](navigation-constants.md) метода [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .</span><span class="sxs-lookup"><span data-stu-id="0b68d-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="0b68d-139">Системные события и системные [**\_ \_ менупопупенд**](event-constants.md) событий событий [**\_ \_ менупопупстарт**](event-constants.md) не отправляются постоянно.</span><span class="sxs-lookup"><span data-stu-id="0b68d-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="0b68d-140">Это известная проблема, которая решена.</span><span class="sxs-lookup"><span data-stu-id="0b68d-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b68d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="0b68d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b68d-142">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="0b68d-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="0b68d-143">**Строка меню**</span><span class="sxs-lookup"><span data-stu-id="0b68d-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="0b68d-144">**Пункт меню**</span><span class="sxs-lookup"><span data-stu-id="0b68d-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





