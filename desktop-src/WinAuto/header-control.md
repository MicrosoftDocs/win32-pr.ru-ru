---
title: Элемент управления "заголовок" (Справочник по элементам пользовательского интерфейса MSAA)
description: Элемент управления "заголовок" отображает заголовки в верхней части столбцов данных и позволяет пользователю сортировать информацию, щелкая заголовки. Проводник Windows использует элемент управления "заголовок", когда выбрано подробное представление.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331440"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="e5893-104">Элемент управления "заголовок" (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="e5893-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="e5893-105">В этом разделе описываются объекты **элементов управления заголовков** в целях справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="e5893-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="e5893-106">Создание объектов **элементов управления "заголовок** " в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="e5893-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="e5893-107">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="e5893-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="e5893-108">Элемент управления "заголовок" отображает заголовки в верхней части столбцов данных и позволяет пользователю сортировать информацию, щелкая заголовки.</span><span class="sxs-lookup"><span data-stu-id="e5893-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="e5893-109">Проводник Windows использует элемент управления "заголовок", когда выбрано подробное представление.</span><span class="sxs-lookup"><span data-stu-id="e5893-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="e5893-110">Имя класса Window для элемента управления "заголовок" — это \_ заголовок WC, который определен как "SysHeader32" в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="e5893-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="e5893-111">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="e5893-111">IAccessible Methods</span></span>

<span data-ttu-id="e5893-112">Элемент управления "заголовок" поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="e5893-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="e5893-113">Метод</span><span class="sxs-lookup"><span data-stu-id="e5893-113">Method</span></span>                                                                    | <span data-ttu-id="e5893-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5893-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="e5893-115">**аккдодефаултактион**</span><span class="sxs-lookup"><span data-stu-id="e5893-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="e5893-116">Этот метод выполняет действие по умолчанию, щелкнув заголовок.</span><span class="sxs-lookup"><span data-stu-id="e5893-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="e5893-117">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="e5893-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="e5893-118">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="e5893-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="e5893-119">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="e5893-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="e5893-120">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="e5893-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="e5893-121">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="e5893-121">IAccessible Properties</span></span>

<span data-ttu-id="e5893-122">Элемент управления "заголовок" поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="e5893-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="e5893-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="e5893-123">Property</span></span>                                                                       | <span data-ttu-id="e5893-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5893-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5893-125">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="e5893-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="e5893-126">Свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e5893-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="e5893-127">**получить \_ аккдефаултактион**</span><span class="sxs-lookup"><span data-stu-id="e5893-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="e5893-128">Свойство **DefaultAction** — "Click".</span><span class="sxs-lookup"><span data-stu-id="e5893-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="e5893-129">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="e5893-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="e5893-130">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="e5893-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="e5893-131">Свойство **Name** совпадает с именем заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="e5893-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="e5893-132">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="e5893-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="e5893-133">**Родительское** свойство — это окно ( [**\_ \_ список системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет то же имя класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="e5893-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="e5893-134">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="e5893-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="e5893-135">Свойство **Role** имеет [**роль \_ System \_ колумнхеадер**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e5893-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="e5893-136">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="e5893-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="e5893-137">Значение свойства **State** всегда имеет [**состояние " \_ \_ только для чтения**](object-state-constants.md) ", а также может включать [**систему состояния " \_ \_ невидимая**](object-state-constants.md)".</span><span class="sxs-lookup"><span data-stu-id="e5893-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5893-138">См. также</span><span class="sxs-lookup"><span data-stu-id="e5893-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5893-139">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="e5893-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




