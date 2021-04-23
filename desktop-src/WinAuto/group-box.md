---
title: Box группы (Справочник по элементам пользовательского интерфейса MSAA)
description: Поле группы — это прямоугольник, который окружает набор элементов управления, таких как флажки или переключатели, и содержит определяемый приложением текст (метка).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778107"
---
# <a name="group-box-msaa-ui-element-reference"></a><span data-ttu-id="90270-103">Box группы (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="90270-103">Group Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="90270-104">В этом разделе описываются объекты **групповых полей** в целях справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="90270-104">This topic describes **Group Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="90270-105">Создание объектов **поля группы** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="90270-105">How to create **Group Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="90270-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="90270-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="90270-107">Поле группы — это прямоугольник, который окружает набор элементов управления, таких как флажки или переключатели, и содержит определяемый приложением текст (метка).</span><span class="sxs-lookup"><span data-stu-id="90270-107">A group box is a rectangle that surrounds a set of controls, such as check boxes or radio buttons, and contains an application-defined text (label).</span></span>

<span data-ttu-id="90270-108">Единственной целью поля группы является упорядочение элементов управления, относящихся к общей цели, определяемой меткой.</span><span class="sxs-lookup"><span data-stu-id="90270-108">The sole purpose of a group box is to organize controls related by a common purpose, indicated by the label.</span></span>

<span data-ttu-id="90270-109">Имя класса окон для поля группы — "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="90270-109">The window class name for a group box is "BUTTON".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="90270-110">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="90270-110">IAccessible Methods</span></span>

<span data-ttu-id="90270-111">Поле группы поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="90270-111">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="90270-112">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="90270-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="90270-113">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="90270-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="90270-114">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="90270-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="90270-115">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="90270-115">IAccessible Properties</span></span>

<span data-ttu-id="90270-116">Поле группы поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="90270-116">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="90270-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="90270-117">Property</span></span>                                                                             | <span data-ttu-id="90270-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90270-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90270-119">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="90270-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="90270-120">Свойство **ChildCount** всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="90270-120">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="90270-121">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="90270-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="90270-122">**получить \_ акккэйбоардшорткут**</span><span class="sxs-lookup"><span data-stu-id="90270-122">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="90270-123">Поля группы не имеют сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="90270-123">Group boxes do not have keyboard shortcuts.</span></span> <span data-ttu-id="90270-124">Однако если текст окна группы содержит символ амперсанда (&), то Microsoft Active Accessibility возвращает строку, отличную от NULL, как свойство **кэйбоардшорткут** .</span><span class="sxs-lookup"><span data-stu-id="90270-124">However, if the window text for the group box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="90270-125">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="90270-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="90270-126">Свойство **Name** получается из текста окна элемента управления (или заголовка), которое отображается вместе с полем группы.</span><span class="sxs-lookup"><span data-stu-id="90270-126">The **Name** property is obtained from the control's window text (or caption), which is displayed with the group box.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="90270-127">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="90270-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="90270-128">**Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="90270-128">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="90270-129">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="90270-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="90270-130">Свойство **Role** — [**\_ \_ группирование системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="90270-130">The **Role** property is [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="90270-131">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="90270-131">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="90270-132">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md):[**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="90270-132">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="90270-133">См. также</span><span class="sxs-lookup"><span data-stu-id="90270-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90270-134">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="90270-134">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





