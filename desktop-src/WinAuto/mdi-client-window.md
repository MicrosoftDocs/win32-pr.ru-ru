---
title: Окно клиента MDI (Справочник по элементам пользовательского интерфейса MSAA)
description: Многодокументный интерфейс (MDI) — это спецификация, определяющая стандартный пользовательский интерфейс для приложений, написанных для Windows. Приложение MDI позволяет пользователю работать с несколькими документами за раз.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986432"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="c4f48-104">Окно клиента MDI (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="c4f48-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="c4f48-105">Многодокументный интерфейс (MDI) — это спецификация, определяющая стандартный пользовательский интерфейс для приложений, написанных для Windows.</span><span class="sxs-lookup"><span data-stu-id="c4f48-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="c4f48-106">Приложение MDI позволяет пользователю работать с несколькими документами за раз.</span><span class="sxs-lookup"><span data-stu-id="c4f48-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="c4f48-107">Приложение MDI имеет три вида окон: окно фрейма, окно клиента и несколько дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="c4f48-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="c4f48-108">Окно фрейма аналогично главному окну приложения и окружено клиентским окном.</span><span class="sxs-lookup"><span data-stu-id="c4f48-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="c4f48-109">Окно клиента является дочерним по отношению к окну фрейма и служит фоном для дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="c4f48-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="c4f48-110">Клиентское окно также обеспечивает поддержку для создания дочерних окон, в которых отображаются документы, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="c4f48-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="c4f48-111">Имя класса окна для клиентского окна MDI — "Мдиклиент".</span><span class="sxs-lookup"><span data-stu-id="c4f48-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="c4f48-112">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="c4f48-112">IAccessible Methods</span></span>

<span data-ttu-id="c4f48-113">MDI-окно клиента поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="c4f48-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="c4f48-114">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="c4f48-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="c4f48-115">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="c4f48-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="c4f48-116">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="c4f48-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="c4f48-117">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="c4f48-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="c4f48-118">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="c4f48-118">IAccessible Properties</span></span>

<span data-ttu-id="c4f48-119">MDI-окно клиента поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="c4f48-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="c4f48-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="c4f48-120">Property</span></span>                                                                 | <span data-ttu-id="c4f48-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4f48-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4f48-122">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="c4f48-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="c4f48-123">Свойство **ChildCount** — это количество дочерних окон, в которых отображаются документы.</span><span class="sxs-lookup"><span data-stu-id="c4f48-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c4f48-124">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="c4f48-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c4f48-125">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="c4f48-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="c4f48-126">Свойство **Name** имеет значение "Workspace".</span><span class="sxs-lookup"><span data-stu-id="c4f48-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c4f48-127">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="c4f48-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="c4f48-128">**Родительское** свойство — это окно фрейма MDI.</span><span class="sxs-lookup"><span data-stu-id="c4f48-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="c4f48-129">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="c4f48-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="c4f48-130">Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="c4f48-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="c4f48-131">**получить \_ аккселектион**</span><span class="sxs-lookup"><span data-stu-id="c4f48-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c4f48-132">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="c4f48-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="c4f48-133">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): [**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c4f48-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c4f48-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c4f48-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f48-135">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="c4f48-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





