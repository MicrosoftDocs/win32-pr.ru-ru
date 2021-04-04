---
title: Элемент управления ToolTip (Справочник по элементам пользовательского интерфейса MSAA)
description: Элемент управления ToolTip отображает небольшое всплывающее окно, содержащее строку текста, описывающую Назначение инструмента, представленное в виде графического объекта в приложении.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888396"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="be0de-103">Элемент управления ToolTip (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="be0de-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="be0de-104">В этом разделе описываются объекты **элементов управления ToolTip** для обращения к ЭЛЕМЕНТУ ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="be0de-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="be0de-105">Создание объектов **элементов управления ToolTip** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="be0de-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="be0de-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="be0de-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="be0de-107">Элемент управления ToolTip отображает небольшое всплывающее окно, содержащее строку текста, описывающую Назначение инструмента, представленное в виде графического объекта в приложении.</span><span class="sxs-lookup"><span data-stu-id="be0de-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="be0de-108">Имя класса Window для подсказки — это класс подсказок TOOLTIP \_ , который определен как "класс подсказок \_ " в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="be0de-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="be0de-109">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="be0de-109">IAccessible Methods</span></span>

<span data-ttu-id="be0de-110">Элемент управления ToolTip поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="be0de-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="be0de-111">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="be0de-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="be0de-112">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="be0de-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="be0de-113">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="be0de-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="be0de-114">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="be0de-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="be0de-115">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="be0de-115">IAccessible Properties</span></span>

<span data-ttu-id="be0de-116">Элемент управления ToolTip поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="be0de-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="be0de-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="be0de-117">Property</span></span>                                                                 | <span data-ttu-id="be0de-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be0de-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be0de-119">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="be0de-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="be0de-120">Свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="be0de-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="be0de-121">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="be0de-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="be0de-122">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="be0de-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="be0de-123">Свойство **Name** — это текст, содержащийся в элементе управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="be0de-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="be0de-124">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="be0de-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="be0de-125">**Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="be0de-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="be0de-126">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="be0de-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="be0de-127">Свойство **Role** — [**\_ \_ Подсказка системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="be0de-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="be0de-128">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="be0de-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="be0de-129">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): [**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="be0de-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="be0de-130">См. также</span><span class="sxs-lookup"><span data-stu-id="be0de-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be0de-131">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="be0de-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





