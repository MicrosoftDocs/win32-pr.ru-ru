---
title: Элемент управления "строка состояния" (Справочник по элементу пользовательского интерфейса MSAA)
description: Строки состояния отображают сведения о состоянии в горизонтальном окне в нижней части окна приложения.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332232"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="4baa0-103">Элемент управления "строка состояния" (Справочник по элементу пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="4baa0-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="4baa0-104">В этом разделе описываются **управляющие объекты строки состояния** для ссылки на элемент ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="4baa0-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="4baa0-105">Создание объектов **элементов управления "строка состояния** " в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="4baa0-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="4baa0-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="4baa0-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="4baa0-107">Строки состояния отображают сведения о состоянии в горизонтальном окне в нижней части окна приложения.</span><span class="sxs-lookup"><span data-stu-id="4baa0-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="4baa0-108">Строки состояния часто делятся на части, называемые панелями, и каждая панель отображает различные сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="4baa0-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="4baa0-109">Кроме того, строки состояния могут содержать объекты различных типов, включая кнопки и индикаторы выполнения.</span><span class="sxs-lookup"><span data-stu-id="4baa0-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="4baa0-110">Имя класса окна для элемента управления "строка состояния" — СТАТУСКЛАССНАМЕ, которое определено как "мсктлс \_ statusbar32" в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="4baa0-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="4baa0-111">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="4baa0-111">IAccessible Methods</span></span>

<span data-ttu-id="4baa0-112">Строки состояния поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4baa0-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="4baa0-113">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="4baa0-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="4baa0-114">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="4baa0-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="4baa0-115">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="4baa0-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="4baa0-116">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="4baa0-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="4baa0-117">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="4baa0-117">IAccessible Properties</span></span>

<span data-ttu-id="4baa0-118">Строки состояния поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4baa0-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="4baa0-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="4baa0-119">Property</span></span>                                                                 | <span data-ttu-id="4baa0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4baa0-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4baa0-121">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="4baa0-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="4baa0-122">Свойство **ChildCount** — это число панелей в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="4baa0-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="4baa0-123">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="4baa0-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="4baa0-124">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="4baa0-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="4baa0-125">Сам объект строки состояния не имеет свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="4baa0-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="4baa0-126">Свойство **Name** каждой панели в строке состояния совпадает с отображаемым текстом.</span><span class="sxs-lookup"><span data-stu-id="4baa0-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="4baa0-127">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="4baa0-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="4baa0-128">**Родительским** свойством объекта строки состояния является окно ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет то же имя класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4baa0-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="4baa0-129">**Родительским** свойством панелей в строке состояния является объект строки состояния.</span><span class="sxs-lookup"><span data-stu-id="4baa0-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="4baa0-130">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="4baa0-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="4baa0-131">Свойство **Role** для самого объекта строки состояния — это [**\_ System \_ StatusBar системного**](object-roles.md)состояния.</span><span class="sxs-lookup"><span data-stu-id="4baa0-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="4baa0-132">Текст, отображаемый в строке состояния, имеет [**роль \_ System \_ статиктекст**](object-roles.md) в качестве свойства **роли** .</span><span class="sxs-lookup"><span data-stu-id="4baa0-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="4baa0-133">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="4baa0-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="4baa0-134">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): [**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="4baa0-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="4baa0-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="4baa0-135">Notes</span></span>

<span data-ttu-id="4baa0-136">Поскольку сочетания клавиш не поддерживаются для элементов управления "строка состояния" или "текстовые области" в строках состояния, [**Get \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4baa0-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4baa0-137">См. также</span><span class="sxs-lookup"><span data-stu-id="4baa0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4baa0-138">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="4baa0-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





