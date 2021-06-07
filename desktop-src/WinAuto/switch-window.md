---
title: Переключить окно (Справочник по элементу пользовательского интерфейса MSAA)
description: Окно переключения отображается каждый раз, когда пользователь нажимает клавиши ALT + TAB для переключения на другое приложение. Окно переключения содержит значок для каждого выполняемого в данный момент приложения.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443985"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="84857-104">Переключить окно (Справочник по элементу пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="84857-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="84857-105">Окно переключения отображается каждый раз, когда пользователь нажимает клавиши ALT + TAB для переключения на другое приложение.</span><span class="sxs-lookup"><span data-stu-id="84857-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="84857-106">Окно переключения содержит значок для каждого выполняемого в данный момент приложения.</span><span class="sxs-lookup"><span data-stu-id="84857-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="84857-107">Имя класса Window для окна переключения — " \# 32771".</span><span class="sxs-lookup"><span data-stu-id="84857-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="84857-108">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="84857-108">IAccessible Methods</span></span>

<span data-ttu-id="84857-109">Окно Switch поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="84857-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="84857-110">Метод</span><span class="sxs-lookup"><span data-stu-id="84857-110">Method</span></span>                                                                    | <span data-ttu-id="84857-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84857-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84857-112">**аккдодефаултактион**</span><span class="sxs-lookup"><span data-stu-id="84857-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="84857-113">Сам объект окна Switch не имеет свойства **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="84857-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="84857-114">Метод [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) для каждого элемента в окне Switch активирует указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="84857-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="84857-115">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="84857-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="84857-116">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="84857-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="84857-117">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="84857-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="84857-118">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="84857-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="84857-119">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="84857-119">IAccessible Properties</span></span>

<span data-ttu-id="84857-120">Окно Switch поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="84857-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|      <span data-ttu-id="84857-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="84857-121">Property</span></span>                                                                          |      <span data-ttu-id="84857-122">Описание</span><span class="sxs-lookup"><span data-stu-id="84857-122">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84857-123">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="84857-123">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="84857-124">Свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="84857-124">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="84857-125">**получить \_ аккдефаултактион**</span><span class="sxs-lookup"><span data-stu-id="84857-125">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="84857-126">Сам объект окна Switch не имеет свойства **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="84857-126">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="84857-127">Свойство **DefaultAction** для каждого элемента в окне Switch имеет значение Switch.</span><span class="sxs-lookup"><span data-stu-id="84857-127">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="84857-128">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="84857-128">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="84857-129">Родительский объект окна переключения не может получать фокус; фокус может получать только отдельные дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="84857-129">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="84857-130">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="84857-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="84857-131">Сам объект окна Switch не имеет свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="84857-131">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="84857-132">Свойство **Name** для каждого значка приложения в окне коммутатора совпадает с отображаемым именем приложения.</span><span class="sxs-lookup"><span data-stu-id="84857-132">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="84857-133">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="84857-133">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="84857-134">Сам объект окна Switch имеет свойство **Role** "Window \[ 32771 \] ".</span><span class="sxs-lookup"><span data-stu-id="84857-134">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="84857-135">Кроме того, каждый значок приложения в окне Switch имеет роль  свойства роли [**\_ System \_ ListItem**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="84857-135">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="84857-136">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="84857-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="84857-137">Сам объект окна Switch не поддерживает свойство **State** .</span><span class="sxs-lookup"><span data-stu-id="84857-137">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="84857-138">Значение **состояния** элементов представления списка — это [**\_ \_ фокус системы состояния**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="84857-138">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="84857-139">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="84857-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84857-140">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="84857-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




