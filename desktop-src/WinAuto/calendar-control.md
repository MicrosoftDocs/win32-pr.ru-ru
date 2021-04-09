---
title: Элемент управления Calendar (Справочник по элементам пользовательского интерфейса MSAA)
description: Элементы управления "Календарь" предоставляют пользователю простой и интуитивно понятный способ выбора даты из привычного интерфейса.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888016"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="827d4-103">Элемент управления Calendar (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="827d4-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="827d4-104">В этом разделе описываются **управляющие объекты календаря** в целях справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="827d4-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="827d4-105">Создание **управляющих объектов календаря** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="827d4-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="827d4-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="827d4-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="827d4-107">Элементы управления "Календарь" предоставляют пользователю простой и интуитивно понятный способ выбора даты из привычного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="827d4-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="827d4-108">Имя класса окна для элемента управления "календарь месяца" — это \_ класс монскал, который определен как "SysMonthCal32" в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="827d4-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="827d4-109">Сведения в этом разделе относятся к элементу управления "Календарь на месяц" в версии 5 файла Коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="827d4-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="827d4-110">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="827d4-110">IAccessible Methods</span></span>

<span data-ttu-id="827d4-111">Элементы управления Calendar поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="827d4-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="827d4-112">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="827d4-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="827d4-113">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="827d4-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="827d4-114">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="827d4-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="827d4-115">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="827d4-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="827d4-116">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="827d4-116">IAccessible Properties</span></span>

<span data-ttu-id="827d4-117">Элементы управления Calendar поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="827d4-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="827d4-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="827d4-118">Property</span></span>                                                                 | <span data-ttu-id="827d4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="827d4-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="827d4-120">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="827d4-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="827d4-121">Свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="827d4-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="827d4-122">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="827d4-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="827d4-123">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="827d4-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="827d4-124">Свойство **Name** получается из статического текстового элемента управления, который помечает элемент управления Calendar.</span><span class="sxs-lookup"><span data-stu-id="827d4-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="827d4-125">При создании элементов управления разработчики сервера должны убедиться, что статический текстовый элемент управления непосредственно предшествует элементу управления, который он помечает в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="827d4-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="827d4-126">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="827d4-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="827d4-127">**Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="827d4-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="827d4-128">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="827d4-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="827d4-129">Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="827d4-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="827d4-130">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="827d4-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="827d4-131">Свойство **State** представляет собой сочетание одной или нескольких следующих значений: системная [](object-state-constants.md)[**\_ \_ невидимая**](object-state-constants.md) система состояний \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ системе \_ состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="827d4-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="827d4-132">См. также</span><span class="sxs-lookup"><span data-stu-id="827d4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827d4-133">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="827d4-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





